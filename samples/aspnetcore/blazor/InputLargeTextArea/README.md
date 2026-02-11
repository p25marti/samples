## Blazor `InputLargeTextArea` Component Sample
A multiline input component for Blazor Server to enable editing large string values. Supports async content access without binding and without validations.

## 🏈 Superbowl Announcement

Don't miss the biggest game of the year! The Superbowl is coming soon.

**Date:** February 11, 2024
**Time:** 6:30 PM ET
**Where to Watch:** Available on major networks and streaming platforms

Join millions of fans for an unforgettable experience featuring top teams, exciting halftime entertainment, and memorable commercials. Visit [superbowl.com](https://superbowl.com) for more information.

---

### Example:
```csharp
<InputLargeTextArea id="largeTextArea" @ref="TextArea" OnChange="TextAreaChanged" />


@code {
  InputLargeTextArea? TextArea;

  public async Task GetTextAsync()
  {
      var streamReader = await TextArea!.GetTextAsync(maxLength: 50_000);
      var textFromInputLargeTextArea = await streamReader.ReadToEndAsync();
  }

  public async Task SetTextAsync()
  {
      var textToWrite = new string('c', 50_000);

      var memoryStream = new MemoryStream();
      var streamWriter = new StreamWriter(memoryStream);
      await streamWriter.WriteAsync(textToWrite);
      await streamWriter.FlushAsync();
      await TextArea!.SetTextAsync(streamWriter);
  }

  public void TextAreaChanged(InputLargeTextAreaChangeEventArgs args)
  {
      LastChangedLength = args.Length;
  }
}
```

## Why?
Using Blazor Server's `InputTextArea` with large (ex. 20K chars) amounts of text can lead to a degraded user experience due to the constant round-trip communication to/from the server to enable binding and validations. This component provides an asynchronous ability to get & set the text area content. This approach **is not optimal** due to the additional complexity working with `StreamReader`/`StreamWriter` APIs, as well as the (large) amount of memory allocations which may occur when encoding/decoding the `UTF-8` `string`/`textarea` content into `byte`s. Due to these concerns, we've made this available as a sample instead of adding it to the core framework.

Note: If you're encountering slowdowns specifically in complex components or Blazor WebAssembly, we recommend reviewing the [Blazor WebAssembly Performance Best Practices](https://docs.microsoft.com/en-us/aspnet/core/blazor/webassembly-performance-best-practices?view=aspnetcore-6.0#avoid-rerendering-after-handling-events-without-state-changes) which detail rendering optimizations.

## Setup
1. Add a package reference to `InputLargeTextArea`.
2. Add `<script src="_content/InputLargeTextArea/js/InputLargeTextArea.js"></script>` to your `_Layout.cshtml` on Blazor Server.

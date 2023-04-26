# youtube-dl-js-wrapper

`youtube-dl-js-wrapper` is a JavaScript package that provides a wrapper for the popular `youtube-dl` command-line tool, allowing you to download and extract information from YouTube videos in your Node.js projects.

## Installation

You can install `youtube-dl-js-wrapper` using NPM:

```
npm install youtube-dl-js-wrapper
```

## Usage

Here is an example of how to use `youtube-dl-js-wrapper` to download a YouTube video and extract information about it:

```javascript
const downloadYoutube = require('youtube-dl-js-wrapper');

downloadYoutube('https://www.youtube.com/watch?v=6xKWiCMKKJg', {
  dumpSingleJson: true,
  noCheckCertificates: true,
  noWarnings: true,
  preferFreeFormats: true,
  addHeader: [
    'referer:youtube.com',
    'user-agent:googlebot'
  ]
}).then(output => console.log(output));
```

This example downloads a video from YouTube with the specified URL and outputs its information in a single JSON object. Several options are passed to customize the download, such as disabling certificate checks, suppressing warnings, preferring free formats, and adding custom headers to the request. The `output` variable is logged to the console, which contains the output of the `youtube-dl` command.

## Notes

- `youtube-dl-js-wrapper` is a wrapper for the `youtube-dl` command-line tool, which means that you must have `youtube-dl` installed on your system for this package to work.
- This package uses the `child_process` module to run `youtube-dl` as a child process. As a result, it may not work correctly on all platforms. If you encounter any issues, please file a bug report on the GitHub page.
- This package is intended for personal use only. Downloading copyrighted material may be illegal in your country.

## Contributing

Contributions to `youtube-dl-js-wrapper` are welcome! Please submit pull requests or open issues on the GitHub page.

## License

`youtube-dl-js-wrapper` is licensed under the [MIT License](https://opensource.org/licenses/MIT).
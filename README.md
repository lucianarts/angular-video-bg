# angular-video-bg

angular-video-bg is an [Angular.js](http://angularjs.org/) YouTube video background player directive. It stresses simplicity and performance.

![angular-video-bg Screenshot](https://raw.github.com/kanzelm3/angular-video-bg/master/screenshot.png)

## Demo

You can see a demo of the directive here: [Angular YouTube Video Background](http://kanzelm3.github.io/angular-video-bg/)

## Download

* [Version 0.1.8](https://github.com/kanzelm3/angular-video-bg/archive/0.1.8.zip)

You can also install the package using [Bower](http://bower.io).

```sh
bower install angular-video-bg
```

Or add it to your bower.json file:

```javascript
dependencies: {
  "angular-video-bg": "~0.1.8"
}
```

*No dependencies (besides Angular) are required!*

## The Basics

To use the library, include the JS file on your index page, then include the module in your app:

```javascript
app = angular.module('myApp', ['angularVideoBg'])
```

The directive itself is simply called *video-bg*. The only required attribute is videoId, which should be a YouTube
video ID.

```html
<video-bg video-id="video.id"></video-bg>
```

## Inline Options

There are a number of options that be configured inline with attributes. Here are a few:

| Option               | Default             | Description                                                                                 |
| -------------------- | ------------------- | ------------------------------------------------------------------------------------------- |
| ratio                | 16/9                | Aspect ratio for the supplied videoId.                                                      |
| loop                 | true                | If set to false, video will not automatically replay when it reaches the end.               |
| mute                 | true                | If set to false, the video's sound will play.                                               |
| start                | null                | Video start time in seconds. If set, video will play from that point instead of beginning.  |
| end                  | null                | Video end time in seconds. If set, video will play until that point and stop (or loop).     |
| content-z-index      | 99                  | If set, will replace the z-index of content within the directive.                           |
| allow-click-events   | false               | If set to true, users will be able to click video to pause/play it.                         |

**Example:**

```html
<video-bg video-id="video.id" ratio="4/3" loop="false" mute="false" start="30" content-z-index="500" allow-click-events="true"></video-bg>
```

## Browser Support

Should work in Chrome, Firefox, Safari, Opera and IE 9+ but have only tested in Chrome, Firefox and Safari so far.

## Contributing

Contributions are welcome. Please be sure to document your changes.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

To get the project running, you'll need [NPM](https://npmjs.org/) and [Bower](http://bower.io/). Run `npm install` and `bower install` to install all dependencies. Then run `grunt serve` in the project directory to watch and compile changes.

If you create new unit test, you can run `grunt test` to execute all of the unit tests. Try to write tests if you contribute.

## Potential Features down the road

* Add support for HTML5 videos instead of just YouTube videos.
* Dynamically change video being played.
* Add support for YouTube playlists.

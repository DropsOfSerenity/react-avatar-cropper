# react-avatar-cropper

[![Reviewed by Hound](https://img.shields.io/badge/Reviewed_by-Hound-8E64B0.svg)](https://houndci.com)

React Avatar Cropper aims to be an out of the box solution to solve the avatar cropping problem for 99% of common use cases. Most of the time you want a modal to pop up, allow the user to crop their uploaded image, and then you want to receive that base64 data to display and send to the server. React Avatar Cropper takes care of this use case.

Taking heavy inspiration from slack's and facebook's user photo cropper, react-avatar-cropper is here to make it easy.


## Demo

There is a demo on http://dropsofserenity.github.io/react-avatar-cropper/

## Installation

In your project

```shell
npm install --save react-avatar-cropper
```
react-avatar-cropper also depends on react obviously :) and react-bootstrap for modal functionality. To install run the following.

```shell
npm install --save react
npm install --save react-bootstrap
```

## Usage

Usage is fairly simple, you can check the /example folder on github for a slightly more complex use case (the use case you see above in the demo). AvatarCropper simple takes a width and a height to determine what size avatar you would like. AvatarCropper then takes an image property where you can pass an external image, a user uploaded data URI or whatever you would like. An onRequestHide function is passed to the underlying modal so you can decide how to dismiss the modal. Lastly onCrop callback function is required, and gives you back the cropped Image, for you to do with as you wish.

```js
// require the component...
var AvatarCropper = require("react-avatar-cropper");

// and in the render function of wherever you please...
render: function() {
  return (
    <AvatarCropper
      onRequestHide={this.handleRequestHide}
      onCrop={this.handleCrop}
      image={this.state.img}
      width={400}
      height={400}
    />
  );
}
```

## Example

There is an example of this common use case on the page for this plugin.
Most importantly we pass the cropped DataURI back through your provided
onCrop function.

Check out http://dropsofserenity.github.io/react-avatar-cropper/ for more examples and info.

## Contributing

Feel free to place issues on the issue tracker or place a pull request
regarding any functionality. I would like to keep this package limited
to providing a great solution for the wide 99% use case that people have
for avatar croppers.

-----------------------

Thanks for looking! <3

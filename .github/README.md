<div align="center">
Custom build of <a href="https://tools.suckless.org/slock/">slock</a>, a display locker for <a href="https://www.x.org/wiki/">X</a> that aims to be minimal, fast, and lightweight.
</div>
<p></p>
<div align="center">
    	<a href="https://github.com/kelvin-van-vuuren/slock#about">About</a>
  <span> • </span>
       	<a href="https://github.com/kelvin-van-vuuren/slock#features">Features</a>
  <span> • </span>
	<a href="https://github.com/kelvin-van-vuuren/slock#Install">Install</a>
  <span> • </span>
	<a href="https://github.com/kelvin-van-vuuren/slock#Usage">Usage</a>
  <p></p>
</div>

https://user-images.githubusercontent.com/54939625/226586165-a95ae9f0-aba2-4bc2-9981-6b60cd5c84df.mp4

### About
[Slock](https://tools.suckless.org/slock/), or the "Simple X display locker", is a display locker for [X](https://www.x.org/wiki/) that aims to be minimal, fast, and lightweight. The software is written by [suckless](https://suckless.org) and adheres to the [suckless philosophy](https://suckless.org/philosophy). As a result, the base distribution of this software comes with a very minimal set of features. This fork extends the functionality and appearance of the program through the use of [patches](https://tools.suckless.org/slock/patches/) and [other changes to the codebase](https://github.com/kelvin-van-vuuren/slock/commits/main).

### Features
* [**Blur screen**](https://tools.suckless.org/slock/patches/dwmlogoandblurscreen/): blur screen when locked.
* [**dwm logo**](https://tools.suckless.org/slock/patches/dwmlogoandblurscreen/): show dwm logo over blurred screen.
* [**Xresources**](https://tools.suckless.org/slock/patches/xresources/): get colours via [Xresources](https://en.wikipedia.org/wiki/X_resources).
* [**Control clear**](https://tools.suckless.org/slock/patches/control-clear/): Stop failure colour from being shown if control key is pressed while the
buffer is empty.
* [**Alternate colours**](https://tools.suckless.org/slock/patches/alternate-colors/): Toggle screen color between two shades of blue during password input to get some feedback.

### Install
Clone this repo and install with ``rm -rf config.h && sudo make clean install``. Configuration is done via [config.def.h](https://github.com/kelvin-van-vuuren/slock/blob/main/config.def.h) so any changes will require the program to be recompiled and installed to take effect.

### Usage
Invoke the ``slock`` command. To get out of it, enter your password. If the password is incorrect, the logo will become red. As the password is entered, the screen colour will toggle between two shades of blue. See my [dotfiles](https://github.com/kelvin-van-vuuren/dotfiles/blob/main/.config/x11/xprofile#L6) for an example of how slock can be automatically invoked after a period of inactivity via [xautolock](https://wiki.archlinux.org/title/Session_lock#xautolock).

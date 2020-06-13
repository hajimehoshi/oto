# Oto (音)

[![GoDoc](https://godoc.org/github.com/hajimehoshi/oto?status.svg)](http://godoc.org/github.com/hajimehoshi/oto)

A low-level library to play sound. This package offers `io.WriteCloser` to play PCM sound.

## Platforms

* Windows
* macOS
* Linux
* FreeBSD
* OpenBSD
* Android
* iOS
* Web browsers ([GopherJS](https://github.com/gopherjs/gopherjs) and WebAssembly)

## Prerequisite

### macOS

Oto requies `AudioToolbox.framework`, but this is automatically linked.

### iOS

Oto requies these frameworks:

* `AVFoundation.framework`
* `AudioToolbox.framework`

Add them to "Linked Frameworks and Libraries" on your Xcode project.

### Linux

libasound2-dev is required. On Ubuntu or Debian, run this command:

```sh
apt install libasound2-dev
```

In most cases this command must be run by root user or through `sudo` command.

#### Building for Linux i386

Along with `GOARCH`, set `CGO_ENABLED=1`. If you're on amd64, make sure to install 32-bit libasound. On Arch, enable multilib by uncommenting the [multilib] section in `/etc/pacman.conf`

### FreeBSD

OpenAL is required. Install openal-soft:

```sh
pkg install openal-soft
```

### OpenBSD

OpenAL is required. Install openal:

```sh
pkg_add -r openal
```

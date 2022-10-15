# AirplaneJS



[![Build status](https://travis-ci.org/watson/airplanejs.svg?branch=master)](https://travis-ci.org/AslanCoder)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/aslancoder)

## Prerequisites

### Hardware

This software requires an [RTL-SDR USB dongle with an RTL2832U
chip][az-search] in order run. Here's a few that I like:

- [RTL-SDR.com dongle with 2x telescopic antennas][az-d1]
- [Very tiny and cheap no-name RTL2832U dongle with an antenna][az-d2]
- Or just [search Amazon for RTL2832U dongles][az-search]

*Disclaimer: I'm trying out the Amazon Affiliate Program to support my
free open source work. So if you decide to buy an RTL-SDR dongle using
one of the links above I'll be grateful (the search link should work as
well).*

For more information about buying RTL-SDR dongles, check out the
[RTL-SDR.com blog buyers
guide](https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/).

### Software

This software also requires that you have [Node.js](https://nodejs.org)
and [librtlsdr](https://github.com/steve-m/librtlsdr) installed on your
system. You can install librtlsdr with most package managers which will
ensure you have the right dependencies.

Homebrew (macOS):

```
brew install librtlsdr
```

Debian based Linux distros:

```
apt-get install librtlsdr-dev
```

## Usage

The easiest way to run AirplaneJS is using the `npx` command that you'll
have availble if you have Node.js 8+ installed. Simply plug in your
RTL-SDR dongle and type:

```
npx airplanejs
```

This will download and run AirplaneJS without any hassle.

When AirplaneJS successfully have connected to the USB dongle, your
default browser should automatically open to
[http://localhost:3000](http://localhost:3000).

Alternatively install the module globally like in the old days:

1. Install AirplaneJS globally:
   ```
   npm install airplanejs -g
   ```
1. Run AirplaneJS:
   ```
   airplanejs
   ```

### Options

The following options are available when running `airplanejs`:

- `--help` - Show help (alias: `-h`)
- `--version` - Output AirplaneJS version (alias: `-v`)
- `--device <index>` - Select RTL dongle (alias: `-d`, default: `0`)
- `--frequency <hz>` - Set custom frequency (alias: `-f`, default: `1090000000`)
- `--gain <gain>` - Set custom tuner gain (alias: `-g`)
- `--auto-gain` - Disable manual tuner gain (default: off)
- `--enable-agc` - Use Automatic Gain Control (default: off)
- `--port <port>` - Set custom HTTP server port (alias: `-p`, default: `3000`)
- `--no-browser` - Disable automatic opening of default browser





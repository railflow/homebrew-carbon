# Homebrew tap for Carbon

[Carbon](https://heypaste.app) is a clipboard manager for macOS and Windows:
press Cmd+V again to paste an older copy.

## Install

```sh
brew tap railflow/carbon
brew install --cask carbon-clipboard
```

Upgrade with `brew upgrade --cask carbon-clipboard`. Uninstall with
`brew uninstall --cask carbon-clipboard` (add `--zap` to remove settings and history).

Requires macOS 11 Big Sur or later. One universal app for Apple Silicon and Intel.

## First launch

Carbon is not notarized yet, so macOS blocks the first launch. Control-click
Carbon in Applications and choose **Open**, or open System Settings > Privacy &
Security and click **Open Anyway**. Then grant **Accessibility** permission when
asked; Carbon needs it to detect repeated Cmd+V presses and paste.

## How this tap is updated

The cask in `Casks/carbon-clipboard.rb` is written by Carbon's release workflow
for every stable version. Installers are downloaded from
`https://downloads.heypaste.app/releases/v<version>/` and checked against the
SHA-256 in the cask. Do not edit the cask by hand; changes are overwritten by
the next release.

Download without Homebrew: https://heypaste.app/download/mac

# Google Home Mobile SDK Sample Applications for Matter

This is a fork of Google's [sample-apps-for-matter-android](https://github.com/google-home/sample-apps-for-matter-android), maintained to try the Google Home Mobile SDK with real Matter devices.

The "[Google Home Application (GHA)](https://play.google.com/store/apps/details?id=com.google.android.apps.chromecast.app)"
is Google's flagship application for interacting with smart home
devices that are part of the Google ecosystem.

Google also offers the [Google Home Mobile SDK](https://developers.home.google.com/mobile-sdk) 
for developers interested in building their own Android applications to interact with
smart home devices.

This repository features a suite of "Google Home Mobile SDK Sample Applications for Matter"
that provide concrete examples of how to
use the [Google Home Mobile SDK](https://developers.home.google.com/mobile-sdk).

These sample applications can be used as the starting point to build your
smart home application for Matter devices.
They can also be used as learning tools to better understand key Matter concepts, as well as tools
to debug and troubleshoot interactions with Matter devices.

These sample applications have been developed to cater to the following use-case 
scenarios.

**Third-Party Ecosystem (3p-ecosystem)**
If your organization supports its own ecosystem of smart devices, then the "3p-ecosystem"
sample application is for you. It leverages the commissioning, device sharing, and discovery
APIs offered in the [Google Home Mobile SDK](https://developers.home.google.com/mobile-sdk).
Note that the sample application provides supports only for a demo fabric based on the Matter SDK.
If you plan to make your application available in production, then you will have to deal
with the complexity of managing in a secure fashion your own Matter fabric.

Note: This application used to be known as GHSAFM. It has been renamed GHSAFM-3p-ecosystem.

See [3p-ecosystem sample app](3p-ecosystem/).

## Changes in this fork

- The `3p-ecosystem` app continues commissioning when the SDK's test attestation verifier rejects a production device. This allows testing with consumer Matter products, including devices that can be shared to Google Home. Attestation failures are bypassed, not validated; use this build for experimentation.
- The app compiles and targets Android 16 (API 36).
- GitHub Actions builds the `default` and `targetcommissioner` debug APKs. Each APK is uploaded as an individual, unzipped Actions artifact. Push a `v*` tag to build the APKs and attach them as plain `.apk` assets to a GitHub Release.

## Download APKs

Download individual APK files from the [latest GitHub Actions run](https://github.com/sam0737/sample-apps-for-matter-android/actions/workflows/android_build.yml) or from the [Releases page](https://github.com/sam0737/sample-apps-for-matter-android/releases). Actions artifacts are retained for 14 days; release assets remain attached to their release.

## Clone the repository

```console
$ git clone https://github.com/sam0737/sample-apps-for-matter-android.git
```

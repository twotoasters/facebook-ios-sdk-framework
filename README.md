# Facebook iOS SDK Framework

*Unofficial* build of the Facebook iOS SDK Framework

## Build Process

This is how I build the framework in this repo.

Clone the official facebook ios sdk repo

`git clone git@github.com:facebook/facebook-ios-sdk.git`

Checkout an official tagged version

`git checkout sdk-version-3.1.1`

Run the build script for framework

`./scripts/build_framework.sh`

Delete all current framework files in *unofficial* framework repo

`git rm -r FacebookSDK.framework`

Move the built framework to *unofficial* framework repo

`cp -r build/FacebookSDK.framework ../facebook-ios-sdk-framework`

Commit with facebook-ios-sdk version number and commit that I built from

`git commit -am "Version 3.1.1 built with commit 2a030e795aed343e7614e149a5ebdfa78b223a72"`

Tag the build with the facebook-ios-sdk version number

`git tag -a v3.1.1 -m "Version 3.1.1"`
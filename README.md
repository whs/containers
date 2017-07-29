# whs's containers collection

Unsatisfied with the maintenance of containers on Docker Hub, I decided to maintain the containers I use myself.

## How often is this updated?

I have a Google Spreadsheet that pull latest version of the apps from [Fedora Anitya](http://release-monitoring.org/) or NPM, which I check around twice a month and update everything at once.

Apps that I no longer use may get removed or leave unmaintained.

## Is this stable?

No!

I run this in my lab environment, so I make no guarantee on its stability. Moreover, I aim to provide latest version of everything and if that means I have to use alpine:edge then so be it.

## Why are you not compiling the binary/check the signature in the build process?

These are quick 'n dirty. Feel free to submit patches though.

## License

Dockerfiles and any related files in this repository is licensed under the [MIT license](LICENSE).

The application packaged in Docker (which might be included here) could be in a different license. Please check the application's site for more details.

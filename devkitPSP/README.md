# devkitPSP

The bare minimum to build PSP homebrews.

## Usage

```sh
docker run --rm -it -v $(pwd):/source greatwizard/devkitpsp
```

### Examples

devkitPro is installed in `/opt/devkitPro` with examples for the PSP in the `devkitPSP/psp/sdk/samples` directory.
You can find several folders to demonstrate how to use various capabilities of the Switch.
To build an example, `cd` into its directory and run `make`.

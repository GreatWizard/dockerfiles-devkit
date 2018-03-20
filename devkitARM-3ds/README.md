# devkitARM-3ds

Everything needed to build GBA, NDS, GP32 and 3DS homebrews.

It includes the following libraries build from source:

* [ctrulib](https://github.com/smealum/ctrulib)
* [citro3d](https://github.com/fincs/citro3d)

## Usage

```sh
docker run --rm -it -v $(pwd):/source greatwizard/devkitarm-3ds
```

### Examples

devkitPro is installed in `/opt/devkitPro` with examples for the GBA, the NDS, the GP32 and the 3DS in the `examples` directory.
You can find several folders to demonstrate how to use various capabilities of the systems.
To build an example, `cd` into its directory and run `make`.

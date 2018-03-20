# devkitPPC

The bare minimum to build GameCube and Wii homebrews.

## Usage

```sh
docker run --rm -it -v $(pwd):/source greatwizard/devkitppc
```

### Examples

devkitPro is installed in `/opt/devkitPro` with examples for the GameCube and the Wii in the `examples` directory.
You can find several folders to demonstrate how to use various capabilities of the systems.
To build an example, `cd` into its directory and run `make`.

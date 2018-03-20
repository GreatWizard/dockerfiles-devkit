# devkitARM

The bare minimum to build GBA, NDS, GP32 and 3DS homebrews.

## Usage

```sh
docker run --rm -it -v $(pwd):/source greatwizard/devkitarm
```

### Examples

devkitPro is installed in `/opt/devkitPro` with examples for the GBA, the NDS, the GP32 and the 3DS in the `examples` directory.
You can find several folders to demonstrate how to use various capabilities of the systems.
To build an example, `cd` into its directory and run `make`.

## Credits

Base code come from [cromo's dockerfile repo](https://github.com/cromo/dockerfiles/tree/master/devkitARM).

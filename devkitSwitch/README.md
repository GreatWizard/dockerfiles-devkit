# devkitSwitch

Combination of devkitA64 and devkitARM.
Lets you build [Atmosphere](https://github.com/Atmosphere-NX/Atmosphere)

## Usage

```sh
docker run --rm -it -v $(pwd):/source devkitswitch
```

### Examples

devkitPro is installed in `/opt/devkitPro` with examples for the Switch in the `examples/switch` directory.
You can find several folders to demonstrate how to use various capabilities of the Switch.
To build an example, `cd` into its directory and run `make`.

# Forge Mixin 1.7.10 example

This is a minimal example mod demonstrating how to get Forge and Mixins to work in 1.7.10. Mixin versions below 0.8 work, and 0.8 also works with certain drawbacks.

It demonstrates Mixins in 2 ways:
1. Injects a method into the constructor of `SoundManager`, which prints a message. This demonstrates injectors.
2. Prints a message every tick the player is in a web, accessing a non-public field of `Entity` in the process. This demonstrates accessors.

## Running in an IDE

In order for mixins to work in an IDE, use the following program arguments:

```--tweakClass org.spongepowered.asm.launch.MixinTweaker --mixin example.mixin.json```

### Running in Eclipse
ForgeGradle 1.2 doesn't generate launch configurations for Eclipse. To get them, download the 1.12.2 MDK and run `gradlew eclipse`. Then copy the generated `.launch` files into your project and correct the paths in them. It's convoluted, but it's the best way I know.

## Examples of other 1.7.10 mods using mixins:
* https://github.com/ForgeEssentials/ForgeEssentials/tree/1.7.10/develop
* https://github.com/DarkShadow44/SereneSeasons/tree/1.7.10_backport

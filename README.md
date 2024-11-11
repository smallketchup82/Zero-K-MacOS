# Zero-K-MacOS
Parallels Desktop Ubuntu ARM64 virtual machines with Zero-K pre-installed.

## Notes
- While the repository is named Zero-K-MacOS, it is not limited to MacOS. The steps used to create the virtual machines can be used on any system that runs ARM
- The launcher will look as though it's not doing anything, and is frozen, but this is fine and just a result of the translation. The game will start eventually, so give it time. Only give up if it's been more than 15 minutes.
- Steam login support is a WIP. For now its unsupported and it's up to you to get it working.
- Due to media libraries not being emulated, animated effects (such as bullets, fire, etc.) will not be rendered

## Technical Details
The virtual machines are built on top of Parallel's Ubuntu ARM64 virtual machine.

For the most part, the virtual machines are stock Ubuntu ARM64 installations with Box64 pre-installed.

Zero-K is grabbed from the semi-portable [itch.io](https://zerok.itch.io/zero-k) releases and extracted to the desktop. The game is run by doing `box64 Zero-K.bin.x86_64` which will start the game and use Box64 to translate the x86_64 calls to ARM64.

## Instructions
Make sure you have Parallels Desktop installed on your system. You can download it from [here](https://www.parallels.com/products/desktop/).

1. You can find the latest virtual machine image [here](https://github.com/smallketchup82/Zero-K-MacOS/releases/latest). Follow the instructions in the release description for extracting it
2. Open Parallels Desktop and click on `File` -> `Open...` and select the virtual machine that you downloaded.
3. The virtual machine will now be added to Parallels Desktop. Right click on the package and click on `Open Package`. This will unpack the virtual machine.
4. Once the virtual machine is unpacked, you can start it by double clicking on the package.
5. The virtual machine will now boot up. By default the password is `sugondese`. You can change this by running `passwd` in the terminal.
6. You'll be greeted with the desktop environment. You can now start Zero-K by double clicking on the icon on the desktop. You can read the README file on the desktop for more information, but for the most part it's a copy of this.
7. Enjoy playing Zero-K!

## Manually setting it up
If you want to set this up outside of a Virtual Machine, don't trust the pre-installed releases, or just want to set it up manually for fun, folow this guide. You need to have Desktop ARM64 Ubuntu already set up and running.

1. Install Box64 using the [pre-compiled binaries](https://github.com/ptitSeb/box64/blob/main/docs/COMPILE.md#pre-build-packages)
2. Restart your system
3. Download Zero-K from the [itch.io portable releases](https://zerok.itch.io/zero-k)
4. Run `sudo apt install libsdl2-2.0-0 libopenal1 libcurl4`
5. To run it you can do `box64 Zero-K.bin.x86_64` in terminal. If this works, you can stop here. If it doesn't, keep going.
6. Run `sudo apt install mono-complete libmono-system-windows-forms4.0-cil libcurl4 libmono-system-runtime-serialization4.0-cil libmono-system-net-http4.0-cil libgtk-3-dev`
7. Try running it with the same command, or try `mono Zero-K.exe`. If both of these fail, you're on your own.

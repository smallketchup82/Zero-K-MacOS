# Zero-K-MacOS
Parallels Desktop Ubuntu ARM64 virtual machines with Zero-K pre-installed.

## Notes
- While the repository is named Zero-K-MacOS, it is not limited to MacOS. The steps used to create the virtual machines can be used on any system that runs ARM
- The launcher will look as though it's not doing anything, and is frozen, but this is fine and just a result of the translation. The game will start eventually, so give it time. Only give up if it's been more than 15 minutes.
- Steam login support is a WIP. For now its unsupported and it's up to you to get it working.

## Technical Details
The virtual machines are built on top of Parallel's Ubuntu ARM64 virtual machine.

For the most part, the virtual machines are stock Ubuntu ARM64 installations with Box64, Box86, and Mono-complete installed.

Zero-K is grabbed from the semi-portable itch.io releases and extracted to the desktop. The game is run by doing `mono Zero-K.exe` which will start the game and use Box64 to translate the x86_64 calls to ARM64.

## Instructions
Make sure you have Parallels Desktop installed on your system. You can download it from [here](https://www.parallels.com/products/desktop/).

1. You can find the latest virtual machine image [here](https://github.com/smallketchup82/Zero-K-MacOS/releases/latest). Follow the instructions in the release description for extracting it
2. Open Parallels Desktop and click on `File` -> `Open...` and select the virtual machine that you downloaded.
3. The virtual machine will now be added to Parallels Desktop. Right click on the package and click on `Open Package`. This will unpack the virtual machine.
4. Once the virtual machine is unpacked, you can start it by double clicking on the package.
5. The virtual machine will now boot up. By default the password is `sugondese`. You can change this by running `passwd` in the terminal.
6. You'll be greeted with the desktop environment. You can now start Zero-K by double clicking on the icon on the desktop. You can read the README file on the desktop for more information, but for the most part it's a copy of this.
7. Enjoy playing Zero-K!

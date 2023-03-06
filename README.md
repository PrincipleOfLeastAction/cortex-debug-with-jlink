# cortex-debug-with-jlink
Debug embedded applications in VS Code example settings.

Copy settings.json into your VS code settings.

Put launch.json in .vscode folder in your project and navigate to the ELF file that your project generates. (Make sure to compile with -g).
Make sure you select the correct device. The example uses Pi Pico with RP2040 chip. There's 2 variants here, RP2040_M0_0 and RP2040_M0_1 but I find the \_1 variant doesn't work when hooking up to the 
debugger ¯\\_(ツ)\_/¯

Now, connect SWDIO and SWCLK to your device.

Go to debug tab in your VS Code and run Cortex Debug.

If something breaks, add the following to the Cortex Debug launch configuration in launch.json. It'll show more details in the terminal and debug console.

```
"showDevDebugOutput": "raw"
```

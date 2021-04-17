#web-vr

## Examples

- link: https://threejs.org/examples/webxr_vr_ballshooter.html
- git repository: https://github.com/mrdoob/three.js

## Installing simple http server

1. Install node.js with npm or yarn
1. For installing http-server from terminal execute: `npm install --global http-server`
1. For launching http-server from terminal execute: `npx http-server [path-to-root-server-folder]`

## Debug Quest VR Browser Content
1. Enable USB Debugging on Oculus Quest
    1.   `adb device`
   should show list of attached devices
    1. `scrcpy -c 1096:1240:174:150` should show screen content
1. Enable Wi-Fi Debugging
    1. Determine the IP address for the device
    `adb shell ip route`
    1. Set adb TCP port `adb tcpip 5555`
    1. Connect device to the debugger `adb connect <ip-address>:5555`
    1. To stop using the Wi-Fi connection, issue the following ADB command from the OS shell:
    `adb disconnect`
1. Start a Remote Debugging Session with Chrome Developer Tools
    1. On the device, browse to your site in Oculus Browser
    1. Launch Google Chrome on PC.
    1. Navigate to `chrome://inspect/#devices`
    1. Find your device, which will be followed by a set of Oculus browser tabs currently open on the device.
    1. Click **inspect** link under to the Oculus Browser tab you wish to debug.
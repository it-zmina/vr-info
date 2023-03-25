#web-vr

## Examples

- link: https://threejs.org/examples/webxr_vr_ballshooter.html
- git repository: https://github.com/mrdoob/three.js

## Tools
- WebXR extension for Chrome: https://chrome.google.com/webstore/detail/webxr-api-emulator/mjddjgeghkdijejnciaefnkjmkafnnje
- adb -- USB or WiFi remote debugger: `sudo apt intall adb`

## Installing simple http server

1. Install node.js with npm or yarn
1. For installing http-server from terminal execute: `npm install --global http-server`
1. For launching http-server from terminal execute: `npx http-server [path-to-root-server-folder]`

## Debug Quest VR Browser Content
1. Enable USB Debugging on Oculus Quest
    1.   `adb devices`
   should show list of attached devices
    1. `scrcpy -c 1096:1240:174:150` should show screen content
1. Enable Wi-Fi Debugging
    1. Determine the IP address for the device
    `adb shell ip route`
    1. Set adb TCP port `adb tcpip 5555`
    1. Connect device to the debugger `adb connect <ip-address>:5555` or `adb connect $(adb shell ip route | awk 'NR==1{print $9}')`
    3. To stop using the Wi-Fi connection, issue the following ADB command from the OS shell:
    `adb disconnect`
1. Start a Remote Debugging Session with Chrome Developer Tools
    1. On the device, browse to your site in Oculus Browser
    1. Launch Google Chrome on PC.
    1. Navigate to `chrome://inspect/#devices`
    1. Find your device, which will be followed by a set of Oculus browser tabs currently open on the device.
    1. Click **inspect** link under to the Oculus Browser tab you wish to debug.

## Great WebXR examples

* [https://www.xrdinosaurs.com](https://www.xrdinosaurs.com)
* [https://aframe.io/a-painter](https://aframe.io/a-painter)
* [https://arvr.google.com/blocks](https://arvr.google.com/blocks)
* [https://xrswim.com/education](https://xrswim.com/education)

## Interesting WebXR articles
    
* [Augmented reality measure with WebXR and Three.JS](https://medium.com/@annika.wollschlaeger/augmented-reality-measure-with-webxr-and-three-js-a0c8355eb91a)
* [Immersive Web Weekly](https://immersivewebweekly.com/?fbclid=IwAR1V0JnNJ05K7Zev7V0CtzJ4H6go_bF99kB_zuKvZYlrBxZFAJYedZJI_5E)    
* [How I sold an $18 million condo in 2 weeks with VR](https://www.inman.com/2020/07/27/how-i-sold-an-18-million-condo-in-2-weeks-with-vr/)    
* [NHS staff are given some of the best training in the world thanks to technology](https://news.microsoft.com/en-gb/2020/07/29/nhs-staff-are-given-some-of-the-best-training-in-the-world-thanks-to-technology/)    
* [10 features of VR games that could improve educational VR design](https://www.vrfocus.com/2020/04/10-features-of-vr-games-that-could-improve-educational-vr-design/)    

## Github repos that will help your development

* [https://github.com/jeeliz/jeelizFaceFilter">https://github.com/jeeliz/jeelizFaceFilter](https://github.com/jeeliz/jeelizFaceFilter">https://github.com/jeeliz/jeelizFaceFilter)
* [https://github.com/ErikSom/threejs-vr-console-debugger">https://github.com/ErikSom/threejs-vr-console-debugger](https://github.com/ErikSom/threejs-vr-console-debugger">https://github.com/ErikSom/threejs-vr-console-debugger)
* [href="https://github.com/toji/xr-dinosaurs">https://github.com/toji/xr-dinosaurs](href="https://github.com/toji/xr-dinosaurs">https://github.com/toji/xr-dinosaurs)    

## YouTube and Twitter XR videos

* [Networked Hand Tracking](href="https://youtu.be/Akw7fVgmcLc)    
* [Hand gesture confirmation](https://twitter.com/i/status/1270315700163354624)    
* [WebXR Voxels - (Minecraft type app)](https://youtu.be/iDv4hUC3XYY)    
* [Foxr Run! Game](https://youtu.be/RRb-fGjKebI)
* [VR for training](https://youtu.be/5LLSeJkJHME)
* [Beat Saber like game](https://twitter.com/i/status/1288430274716598273)
* [Hand tracking keyboard](https://twitter.com/i/status/1296342759117164544)

# GR3/3X Shutdown Image Tool

[简体中文](README.md) | **English**


A standalone webpage for creating shutdown images and SD card installation packages for RICOH GR III / GR IIIx.

Open `index.html` in Safari or Chrome, select the correct camera variant and firmware, choose an image, and download the installation ZIP. The page includes an anniversary example, an optional camera-text preview, and collapsible restore / disable-Script options. The preview overlay is excluded from the downloaded image.

Supported selections: GR IIIx Standard / HDF / Urban (official firmware 1.60), and GR III Standard / HDF / Street / ING / Diary (official firmware 2.10). The installation workflow has been camera-tested on a standard GR IIIx 1.60; other variants and the latest anniversary image have not been camera-tested. GR IV packages are unavailable.

Format the SD card in the camera first, then copy the extracted entry file, `DEVELOP.MOD`, `IMAGE.JPG` and `script` folder to its root. Follow the enclosed bilingual instructions for the staged MENU + Power / normal-start procedure. Formatting erases all card files: save your photographs first. Do not interrupt installation or format the card midway.

“Black space at bottom” reserves a black area for camera text. “Fill to bottom” lets the camera text overlay the image. The anniversary example already reserves space for the text. Use the provided restore option to restore the shutdown screen; reinstalling official firmware may leave the modified image intact.

The HTML includes all necessary code and assets and requires no build or installation. No firmware BIN is distributed in this repository.

**Disclaimer:** This project is open-source technical research and is not an official RICOH feature. Firmware flashing and script operations involve risks; you are responsible for the consequences. This tool and its generated files are intended solely for personal learning, research and discussion among enthusiasts. Any commercial use for profit is strictly prohibited. Trademarks and original camera artwork remain the property of their respective owners. Third-party notices are retained; no additional rights to those assets are implied.

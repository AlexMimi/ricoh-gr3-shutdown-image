# GR3/3X 关机画面 · Shutdown Image Tool

为 RICOH GR III / GR IIIx 制作自定义关机图片和 SD 卡安装包的独立网页。

**在线使用：https://holowave.cc/gr**

上传 JPG、PNG 或 WebP，或使用内置 20 周年图。网页适配图片并生成 ZIP 安装包；预览可显示相机关机计数和固件版本，遮罩不会写入最终图片。

## 支持范围

| 系列 | 机型 | 对应官方固件 |
| --- | --- | --- |
| GR IIIx | 标准版、HDF、Urban Edition | 1.60 |
| GR III | 标准版、HDF、Street Edition、ING Edition、Diary Edition | 2.10 |

普通 GR IIIx 1.60 的安装流程已由项目使用者实机测试；其他机型未完成实机测试。更新后的 20 周年图尚未实机测试。GR IV 系列暂不提供安装包。

## 使用

1. 下载 `index.html`，用 Safari 或 Chrome 打开，或使用在线网页。
2. 选择准确的机型和对应固件版本。上传自己的图片，或使用内置示例。
3. 下载并解压安装包。先在相机内格式化 SD 卡，再将入口文件、`DEVELOP.MOD`、`IMAGE.JPG` 和 `script` 文件夹复制到卡根目录。
4. 按包内说明执行相机操作：MENU + 电源开启 Script，正常开机写入图片，再 MENU + 电源切换图片槽位，最后正常开关机确认并在相机内格式化卡。

格式化会删除 SD 卡中的全部文件，请先保存自己的照片。安装过程中不要格式化或中断写入。网页内的“关闭 Script”和“恢复关机画面”提供折叠下载选项。

**底部留黑**给相机文字留出黑色区域；**底部填满**覆盖整个画面，相机文字会叠在图片上。20 周年示例已预留底部文字区域，无需切换“底部留黑”。

恢复关机图片请使用网页里的对应恢复选项。实机测试发现，重新安装官方固件不一定恢复被修改的关机图片。

## 项目结构

`index.html` 包含界面、图片编码器、SD 卡包生成器、示例及恢复图片，可独立运行，无需安装依赖。仓库不包含固件 BIN。

图片处理和安装包生成在浏览器中执行。关机文字遮罩仅作示意，实际显示受相机设置影响。网页提供中文和英文，安装包内说明为双语。

## 免责声明

本项目为开源技术研究，非理光（RICOH）官方功能。刷机与固件脚本操作存在一定风险，请自行承担操作后果；本工具及生成文件仅供个人学习研究与爱好者交流使用，严禁用于任何商业牟利行为。

相机商标和原厂图片属于其各自权利人。第三方编码器声明保留在源码中；见 [THIRD_PARTY.md](THIRD_PARTY.md)。本仓库未附加 MIT 等许可，不应推断对第三方素材具有额外授权。

---

## English

A standalone webpage for creating shutdown images and SD card installation packages for RICOH GR III / GR IIIx.

**Live tool: https://holowave.cc/gr**

Open `index.html` in Safari or Chrome, select the correct camera variant and firmware, choose an image, and download the installation ZIP. The page includes an anniversary example, an optional camera-text preview, and collapsible restore / disable-Script options. The preview overlay is excluded from the downloaded image.

Supported selections: GR IIIx Standard / HDF / Urban (official firmware 1.60), and GR III Standard / HDF / Street / ING / Diary (official firmware 2.10). The installation workflow has been camera-tested on a standard GR IIIx 1.60; other variants and the latest anniversary image have not been camera-tested. GR IV packages are unavailable.

Format the SD card in the camera first, then copy the extracted entry file, `DEVELOP.MOD`, `IMAGE.JPG` and `script` folder to its root. Follow the enclosed bilingual instructions for the staged MENU + Power / normal-start procedure. Formatting erases all card files: save your photographs first. Do not interrupt installation or format the card midway.

“Black space at bottom” reserves a black area for camera text. “Fill to bottom” lets the camera text overlay the image. The anniversary example already reserves space for the text. Use the provided restore option to restore the shutdown screen; reinstalling official firmware may leave the modified image intact.

The HTML includes all necessary code and assets and requires no build or installation. No firmware BIN is distributed in this repository.

**Disclaimer:** This project is open-source technical research and is not an official RICOH feature. Firmware flashing and script operations involve risks; you are responsible for the consequences. This tool and its generated files are intended solely for personal learning, research and discussion among enthusiasts. Any commercial use for profit is strictly prohibited. Trademarks and original camera artwork remain the property of their respective owners. Third-party notices are retained; no additional rights to those assets are implied.

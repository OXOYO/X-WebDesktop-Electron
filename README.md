# X-WebDesktop-Electron

> 基于Vue & Electron 的 WebDesktop 系统

# Version

| FrontEnd | API | Electron |
| :-------- | :-------- | :-------- |
| [3.x](https://github.com/OXOYO/X-WebDesktop-Vue/tree/master) | [3.x](https://github.com/OXOYO/X-WebDesktop-Api-Koa/tree/master) | [3.x](https://github.com/OXOYO/X-WebDesktop-Electron/tree/master) |
| [2.0.0](https://github.com/OXOYO/X-WebDesktop-Vue/tree/2.0.0) | [2.0.0](https://github.com/OXOYO/X-WebDesktop-Api-Koa/tree/2.0.0) | [2.0.0](https://github.com/OXOYO/X-WebDesktop-Electron/tree/2.0.0) |
| [1.0.1](https://github.com/OXOYO/X-WebDesktop-Vue/tree/1.0.1) | [1.0.1](https://github.com/OXOYO/X-WebDesktop-Api-Koa/tree/1.0.1) | - |
| [1.0.0](https://github.com/OXOYO/X-Desktop-Vue/tree/master) | - | - |

# Download for Windows

[3.x](https://github.com/OXOYO/X-WebDesktop-Electron/blob/master/build/X-WebDesktop%20Setup%203.0.3.exe?raw=true)

#### Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:9080
npm run dev

# build electron application for production
npm run build

# run unit & end-to-end tests
npm test


# lint all JS/Vue component files in `src/`
npm run lint

```

#### setup制作

#### 使用 `Niuniu_NSIS_SetupSkin` 制作安装界面

1.拷贝 `/build/` 目录下打包生成的 `X-WebDesktop Setup *.*.*.exe` 文件到 `/setup/Niuniu_NSIS_SetupSkin/FilesToInstall/` 目录下；

2.将 `/build/win-unpacked` 目录下的所有文件压缩为 `app.7z` 并拷贝到 `/setup/Niuniu_NSIS_SetupSkin/SetupScripts/X-WebDesktop/` 目录下；

3.执行 `/setup/Niuniu_NSIS_SetupSkin/` 目录下 `build.bat` 或 `build-nozip.bat` 脚本，生成好的安装程序将输出到 `/setup/Niuniu_NSIS_SetupSkin/Output/` 目录下。


  ***注意：** `/setup/Niuniu_NSIS_SetupSkin/SetupScripts/X-WebDesktop/skin/` 目录下为安装界面布局、图片，可以修改 `xml` 或替换图片改变安装界面布局。*

#### 使用 `VNISEdit` 制作安装界面

[win7下nsis打包exe安装程序教程](https://blog.csdn.net/arvin0/article/details/56482370)

------

This project was generated with [electron-vue](https://github.com/SimulatedGREG/electron-vue) using [vue-cli](https://github.com/vuejs/vue-cli). Documentation about the original structure can be found [here](https://simulatedgreg.gitbooks.io/electron-vue/content/index.html).

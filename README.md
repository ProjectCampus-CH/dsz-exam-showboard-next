<div align="center">

# <image src="resources/icon.png" height="28"/> ExamShowboard-Next

> 考试看板 Next —— 下一代考试看板

[![stars](https://img.shields.io/github/stars/MKStoler4096/dsz-exam-showboard-next?label=Stars)](https://github.com/MKStoler4096/dsz-exam-showboard-next/stargazers)
[![forks](https://img.shields.io/github/forks/MKStoler4096/dsz-exam-showboard-next?label=Forks)](https://github.com/MKStoler4096/dsz-exam-showboard-next/forks)
[![Watchers](https://img.shields.io/github/watchers/MKStoler4096/dsz-exam-showboard-next?style=social)](https://github.com/MKStoler4096/dsz-exam-showboard-next/watchers)
[![Downloads](https://img.shields.io/github/downloads/MKStoler4096/dsz-exam-showboard-next/total?style=social&label=Downloads&logo=github)](https://github.com/MKStoler4096/dsz-exam-showboard-next/releases)
[![GitHub Issues](https://img.shields.io/github/issues-search/MKStoler4096/dsz-exam-showboard-next?query=is%3Aopen&style=social-square&logo=github&label=Issues&color=%233fb950)](https://github.com/MKStoler4096/dsz-exam-showboard-next/issues)
[![GitHub Discussions](https://img.shields.io/github/discussions/MKStoler4096/dsz-exam-showboard-next?style=flat&logo=Github&label=Discussions)](https://github.com/MKStoler4096/dsz-exam-showboard-next/discussions)
[![Created At](https://img.shields.io/github/created-at/MKStoler4096/dsz-exam-showboard-next)](https://github.com/MKStoler4096/dsz-exam-showboard-next)
[![Github Last Commit](https://img.shields.io/github/last-commit/MKStoler4096/dsz-exam-showboard-next)](https://github.com/MKStoler4096/dsz-exam-showboard-next/commits/master)
[![GitHub Language Count](https://img.shields.io/github/languages/count/MKStoler4096/dsz-exam-showboard-next)](https://github.com/MKStoler4096/dsz-exam-showboard-next)
[![GitHub Top Language](https://img.shields.io/github/languages/top/MKStoler4096/dsz-exam-showboard-next)](https://github.com/MKStoler4096/dsz-exam-showboard-next)
[![LICENSE](https://img.shields.io/badge/License-GPL--3.0-red.svg 'LICENSE')](LICENSE)
[![QQ群](https://img.shields.io/badge/-QQ%E7%BE%A4%EF%BD%9C901670561-blue?style=flat&logo=TencentQQ&logoColor=white)](https://qm.qq.com/q/zDiEipHsaI)

一款显示当前时间与考试详细信息的看板类软件

| 下载 | [Releases](https://github.com/MKStoler4096/dsz-exam-showboard-next/releases) | [Actions](https://github.com/MKStoler4096/dsz-exam-showboard-next/actions) |
| ---- | ---------------------------------------------------------------------------- | -------------------------------------------------------------------------- |

![WelcomePage](/.Screenshots/WelcomePage.jpg)
![ExamPage](/.Screenshots/ExamPage.jpg)

</div>

> [!tip]
> 
> **本软件使用`Vue` + `TypeScript` + `JavaScript`制作，使用`Node.js` + `Electron`完善系统级功能并打包。**

## 功能

- 起始页展示`打开配置`、`直接进入看板`按钮
- 看板页面
  - 上方展示`考试标题`、`信息`
  - 左侧展示`当前时间`、`当前科目`、`考试时间`、`考试状态`
  - 右侧展示考试科目列表，包括`科目`、`开始`、`结束`、`状态`
  - 考试结束前15分钟黄字提醒
  - 集控功能（早期测试）

## 开始使用

- 下载安装程序并运行

默认安装在`AppData\Local\Programs\dsz-exam-showboard`

- 编写`json`配置文件

新建文件`exam_config.json`，模板如下

```json
{
  "examName": "考试名称",
  "message": "信息",
  "examInfos": [
    {
      "name": "科目",
      "start": "2024-10-01T07:00:00",
      "end": "2024-10-01T08:00:00"
    },
    {
      "name": "科目",
      "start": "2024-10-01T09:00:00",
      "end": "2024-10-01T10:00:00"
    }
  ]
}
```

- 打开软件，进入起始页面，点击`打开配置`按钮，选择配置文件，下次可点击`直接进入看板`按钮，将继续使用上次加载的配置。

- 集控

仿照 `ClassIsland` 的集控方法，把上面提到的 `exam_config.json` 传上去，获得 `raw` 直链粘贴回文本框并保存即可。

## 遇到问题

💡 如果您遇到`Bug`，或需要提出`优化`建议或新的`功能`，请提交[`Issues`](https://github.com/MKStoler4096/dsz-exam-showboard-next/issues)或在[`Discussions`](https://github.com/MKStoler4096/dsz-exam-showboard-next/discussions)中讨论。

👥 您也可以加入[`QQ群｜901670561`](https://qm.qq.com/q/zDiEipHsaI)获取帮助或交流讨论。

🛠️ 欢迎为本软件进行改进或编写新功能提交[`Pull Request`](https://github.com/MKStoler4096/dsz-exam-showboard-next/pulls)

## 开发

### 推荐开发环境

- [VSCode](https://code.visualstudio.com/)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)

> [!IMPORTANT]
> 
> **必须使用Yarn包管理。Node版本要求为20。**

### 工程构建

#### 配置

```bash
$ yarn
```

#### 开发

```bash
$ yarn dev
# 如果无法显示，可以尝试使用下面的命令（不支持热重载）：
$ yarn start
```

> [!note]
>
> **如果dev模式页面不显示或按钮点击无效等问题，请连续刷新至少3次后再进行操作。build后没有此问题。**

#### 生成

```bash
# For windows
$ yarn build:win

# For macOS
$ yarn build:mac

# For Linux
$ yarn build:linux
```

### 开发进度

- 正在[`master`](https://github.com/MKStoler4096/dsz-exam-showboard-next/commits/master)分支上维护`1.2-Yesod`版本。

- 正在[`dev`](https://github.com/MKStoler4096/dsz-exam-showboard-next/commits/dev)分支上开发`1.3-HOD`版本。

## Stars 历史

[![Stargazers over time](https://starchart.cc/ProjectCampus-CH/exam-showboard-next.svg?variant=adaptive)](https://starchart.cc/ProjectCampus-CH/exam-showboard-next)

<div align="center">

如果这个项目对您有帮助，请点亮 Star [⭐](#dsz-exam-showboard-next)

</div>

# dotnet-learn-01

## 安裝 dotnet-sdk

[Install dotnet-sdk Ubuntu](https://docs.microsoft.com/zh-tw/dotnet/core/install/linux-ubuntu)

## 安裝 vscode C# 語言支援

[C#](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)

[C# XML Documentation](https://marketplace.visualstudio.com/items?itemName=k--kato.docomment)

## 專案建立

1 建立資料夾

```shell=
mkdir ~/$project_name
cd ~/$project_name
```

2 建立 cli 專案內容

```shell=
dotnet new console
```

3 加入要使用的 Package

```shell=
dotnet add package Figgle
```

## 分析資料夾

1. 結構

- bin 用來放 build 或 publish 出來得檔案
- obj 存放 dependency
- $project_name.csproj 用來紀錄檔案設定的 profile 
- *.cs 檔案執行內容

2. 執行進入點

```c#=
namespace dotnet_learn_01
{
  class Program 
  {
    static void Main(string[] args) 
    {
      Console.WriteLine(Figgle.FiggleFonts.Standard.Render("Hi, sharon"));    
    }
  }
}
```
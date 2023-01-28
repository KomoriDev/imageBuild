# imageBuild

该功能是使用超分辨率来对图像进行重建，可以简单理解成让图片变大变清晰。

![version](https://img.shields.io/pypi/v/imageBuild?style=for-the-badge)  
![license](https://img.shields.io/pypi/l/imageBuild?logoColor=%2397CA00&style=flat-square)

## 效果

重建前 与 重建后  

<img src="https://mute23-code.github.io/blogImage/imageBuild-demo/demo.jpg" width="200">
<img src="https://mute23-code.github.io/blogImage/imageBuild-demo/demo(build).jpg" width="200">


## 食用方法 - Hugging Face

> **简单介绍下 Hugging Face**  
> 中文名：拥抱脸 ，英文名就和这个表情包一样🤗同样的名字。  
> Hugging Face 在国内应用非常广泛，入门者可以用它快速用得上科研大牛们训练出的超牛模型，你甚至不需要知道什么是GPT，BERT就可以用他的模型了

Hugging Face 官网：[https://huggingface.co/](https://huggingface.co/)

### 安装拥抱脸

* 使用 pip 安装  
（不建议从 pip 安装，推荐将源码部署在 [huggingface](https://huggingface.co/) 中使用，简单快捷）
```
pip install imageBuild
```
* 从 Github 安装
```
git clone https://github.com/mute23-code/imageBuild.git
```

* 从 HuggingFace 安装
```
git clone https://huggingface.co/mute23/imageBuild
```
别忘了切换文件夹 `cd imageBuild`


### 下载 huggingface hub Cli
```cmd
pip install huggingface_hub
```

## 登录
```cmd
huggingface-cli login
```

## 创建存储库
和 Github 差不多，不多赘述  
[点此创建](huggingface.co/new)

## 添加存储库

```git
git lfs install
```

## 推送
```git
git add .
git commit -f "first commit"
git push
```

到此，你的图像重建的工具就搭建完成了，拥抱脸贴心的为你准备了api，你也可以通过它实现图像重建。不过，由于使用api，线上算力存在限制，所以调用的是较小的模型，导致线上的模型似乎没有本地推断那么好，事实上，效果差距还是很大的。想要获得更好的重建效果，还是得靠你刚才搭建的程序
```
API = "https://hf.space/embed/{你的id名}/{你的仓库名}/api/predict/"
```

## 鸣谢

* [`xinntao/Real-ESRGAN`](https://github.com/xinntao/Real-ESRGAN) 超分辨率原理便是基于该仓库
* [`ppxxxg22/nonebot_plugin_RealESRGAN`](https://github.com/ppxxxg22/nonebot_plugin_RealESRGAN) 提供了封装后的执行文件

## 许可证

由于 `Real-ESRGAN` 使用了 [BSD 3-Clause](https://choosealicense.com/licenses/bsd-3-clause/) 许可证，本项目也同样使用该许可  
**注意！BSD许可证禁止在未经书面同意的情况下使用版权所有者或其贡献者的名义来推广衍生产品。**
```
BSD 3-Clause License

Copyright (c) 2023, mute.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```
# 使用GAN生成动漫人物头像

使用GAN生成动漫人物头像的代码借鉴于  https://github.com/carpedm20/DCGAN-tensorflow

代码的训练是在Google colab上完成的，要使用Google colab必须要会科学上网，还要要创建一个Google账号。
只要在Google colab上运行 anime.ipynb 这个文件就可以开始训练代码了。

## 这里需要注意的是：
Google colab上默认的TensorFlow版本和scipy版本太高了
代码中用到的TensorFlow版本尽量要在1.18以下，这里用的是1.14版本，SciPy使用的是版本是1.2.1。

运行
```
!python main.py --dataset face --input_height 96 --input_width 96 --output_height 48 --output_width 48 --crop --train --epoch 300 --input_fname_pattern "*.jpg"
```
开始训练

这里的各种参数详见 main.py,需要注意的是 face 是动漫人物的图片，它的路径是 /data/face，其中文件夹data和主文件main.py在同一目录下。

由于网速的原因代码并没有训练完。
这是训练了3个epoch后生成的图片

![3epoch](https://github.com/C-Black-Cat/GAN_test/blob/main/train_03_0193.png)

将300个epoch训练完后结果会更加理想



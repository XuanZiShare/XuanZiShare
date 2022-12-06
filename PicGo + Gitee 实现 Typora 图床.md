# PicGo + Gitee 实现 Typora 图床

## 需要软件

1. Gitee 开源仓库
2. PicGo 上传工具
3. Typora 上传测试

---



## 第一步：创建 Gitee 开源仓库并获取秘钥

1. Gitee官网链接：https://gitee.com

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061014914.png" alt="搜狗截图20221206094027" style="zoom: 40%;" />

2. 创建仓库

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061015249.png" alt="搜狗截图20221206094202" style="zoom: 50%;" />

3. 将仓库开源，可以让他人访问图片

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061221251.png" style="zoom:67%;" />

4. 勾选协议

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061024637.png" alt="搜狗截图20221206094303" style="zoom:67%;" />

4. 获取 Gitee 私人秘钥

   直接打开下面链接获取秘钥：https://gitee.com/profile/personal_access_tokens

   建议先复制到文档里,秘钥只出现一次

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061025333.png" alt="搜狗截图20221206094702" style="zoom:67%;" />

5. 到这里Gitee的搭建就已经完成了下面开始下载 PicGo 实现自动上传图片

---



## 第二步：下载 PicGo 软件

1. 到 PicGo 的 GitHub 官方下载：https://github.com/Molunerfinn/PicGo

   推荐使用 GitHub 链接比较稳定，别的也都可以

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061029827.png" alt="搜狗截图20221206095116" style="zoom:67%;" />

2. 下滑找到`.exe`程序下载

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061222393.jpeg" style="zoom:67%;" />

3. 推荐使用 IDM 下载比较快

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061033520.png" alt="搜狗截图20221206095353" style="zoom:67%;" />

4. 安装 PicGo 软件

![搜狗截图20221206095925](https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061033381.png)

5. 插件设置中搜索`gitee`下载插件

   ！！！注意下载下面的插件

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061034458.png" alt="搜狗截图20221206100039" style="zoom:67%;" />

6. 如果提示安装`Node.js`他会自动打开官网

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061036239.png" alt="搜狗截图20221206100053" style="zoom:67%;" />

7. 推荐下载左边的长期稳定版

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061038150.png" alt="搜狗截图20221206100121" style="zoom: 50%;" />

8. 一直点击下一步到`Finish`安装完成

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061039545.png" alt="搜狗截图20221206100312" style="zoom: 67%;" />

9. 安装完成后记得重启`PicGo`后，再次搜索安装

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061040659.png" alt="搜狗截图20221206100442" style="zoom:67%;" />

---



## 第三步：配置 PicGo 地址

1. 打开图床设置 > Gitee

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061043880.png" alt="搜狗截图20221206100518" style="zoom:67%;" />

2. 填写地址

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061044175.png" alt="搜狗截图20221206100728" style="zoom:67%;" />

3. `repo`为 Gitee 仓库地址

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061045803.png" alt="搜狗截图20221206100612" style="zoom:67%;" />

4. `token`为先前辅助的 Gitee 秘钥

5. `path`图片上传路径，根目录不写就行

6. 记得将 Gitee 设置为默认图床

7. 推荐在 PicGo 设置中打开时间戳重命名以防图片命名冲突

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061053999.png" alt="搜狗截图20221206101129" style="zoom:67%;" />


8. 重启 PicGo 刷新配置

9. 到这里 PicGo 的配置就已经完成了下面进入 Typora 设置自动上传图片

---



## 第四步：设置 Typora 自动上传图片

1. 进入Typora偏好设置 > 图像 安装我的设置进行调试，注意PicGo路径要写上exe程序

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061056848.png" alt="搜狗截图20221206100902" style="zoom:67%;" />

2. 重启`Typora`后，点击左下角验证图片上传

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061100274.png" alt="搜狗截图20221206101007" style="zoom:67%;" />

3. 验证成功，恭喜你已经完成了`PicGo + Gitee 实现 Typora 图床`完整设置，可以愉快的往文章里插入图片了

4. 进入 Gitee 仓库就可以看到 Typora 的验证图片和我们自己上传的图片了

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/HTML/202212061104962.png" alt="搜狗截图20221206101256" style="zoom:67%;" />

---

> 附言：Gitee中上传的图片不能大于`1MB`
>
> 如果 Typora 验证失败请检查自己 PicGo 地址是否配置正确，并`重启Typora和PicGo`

> 玄子2022年12月6日
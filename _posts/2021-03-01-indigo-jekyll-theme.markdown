<!-----
title: ":ramen: Indigo, minimalist jekyll theme"
layout: post
date: 2016-01-23 22:10
tag: jekyll
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: johndoe
externalLink: false
----->

<!-----
title: "系统框架"
layout: post
date: 2021-03-01 22:10
tag: jekyll
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: johndoe
externalLink: false
----->



---
title: "系统框架"
layout: post
date: 2021-03-01 22:10
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
externalLink: false
---

![Screenshot](https://raw.githubusercontent.com/sergiokopplin/indigo/gh-pages/assets/assets/images/jekyll-logo-light-solid.png)


系统框架如图所示，分为三个主要模块：
① 硬件端：通过红外检测等手段判断图像采集的时间以进行图像采集，同时采集温度湿度等环境信息，实现数据的上传。
② 云端：实现数据的分类，对图像进行识别，将识别结果与环境信息发送至用户端进行应用。
③ 用户端：根据图像识别结果获取的冰箱内容，提供美食智能推荐，过期提醒等服务，根据传感器采集信息提供冰箱环境实时监控与异常报警等功能。


###开门检测模块
通过红外测距模块测量模块至冰箱门的距离。在静息状态下，测距结果将稳定在一个范围区间内。检测到距离超过稳定区间范围则表示门已打开，进入图像获取阶段。图像获取的触发方式可采用查询方式与中断方式实现，查询方式可以简化电路结构，中断方式可以提供更低的功耗。具体选择手段暂定。

###物品拿出放入识别模块
方法一：
在检测到门已打开后，以一定时间间隔进行图像获取，判断放入或取出的物品种类。
![Screenshot](https://raw.githubusercontent.com/sergiokopplin/indigo/gh-pages/assets/assets/images/open1.png)


方法二：检测到门已打开后，等待至测距结果返回正常值，则表示门已关闭，此时对于置物平台进行拍照，将识别结果与历史结果进行对比，得出物品的增加或减少结果。
![Screenshot](https://raw.githubusercontent.com/sergiokopplin/indigo/gh-pages/assets/assets/images/open2.png)



###云端模块
云端在接受到数据后，如果包含图片数据，则进行图像识别，将识别结果和传感器数据发送至用户端，否则仅发送传感器数据。

① 功耗：与硬件端的数据采集频率成正相关，因此需要确定合理的采集频率，以实现功耗与响应时间的平衡。
② 准确率：受照明条件、图像清晰程度影响。
③ 响应时间：可分为云端数据处理与用户端应用两部分。

<!-----

What has inside?

- Gulp
- BrowserSync
- Stylus
- SVG
- Travis
- No JS
- [98/100](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fsergiokopplin.github.io%2Findigo%2F)

---

[Check it out](https://sergiokopplin.github.io/indigo/) here.
If you need some help, just [tell me](https://github.com/sergiokopplin/indigo/issues).
-->
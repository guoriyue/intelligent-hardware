---
title: ":ramen: 通信与软件框图"
layout: post
date: 2020-05-02 20:10
tag: jekyll
projects: true
author: Mingfei
externalLink: false
---

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

## 通信协议
我们的通信内容包括树莓派与服务器之间的通信，以及用户端与服务器之间的通信。

![Screenshot](https://github.com/guoriyue/intelligent_hardware/tree/master/assets/images/CommuS.png)

我们详细介绍一下树莓派与服务器之间的通信。
树莓派在连接至服务器后，每次发送数据前进行请求并告知服务器本次发送的数据类型，收到服务器确认后进行数据发送，服务器在接收到数据类型信息后开始数据接收并进行相关处理。对于“data”型数据，存入本地文本，对于“image”型数据，进行图像识别，并将识别结果存入本地。
在图片数据的传输过程中，因为每次接收具有上限，所以服务器端需要进行多次接收，。

## 软件


![Screenshot](https://github.com/guoriyue/intelligent_hardware/tree/master/assets/images/ruanK.png)
这是软件部分的流程图，我们从图像识别之后的结果开始。如果图像识别成功，会自动填入物品的名称和图片，然后物品会被放入**存储冰箱内物品的列**中，并且开始计时。如果图像识别失败，则需要用户手动填入物品的名称和图片，再将物品放入**存储冰箱内物品的列表**中。因为图像识别可能无法识别物品的时间，因此用户需要在app端手动填入。
物品进入**存储冰箱内物品的列表**之后，开始计时。当过期之后，app会向用户发过期预警。当没有过期的时候，app会提醒用户保质期还有多长时间，并且根据未过期的食物向用户推荐菜谱。


![Screenshot](https://github.com/guoriyue/intelligent_hardware/tree/master/assets/images/yongJ.png)
这是用户界面的示意图，预计会有两个如图的列表，分别是食物列表和食谱列表。


<!-----
title: ":ramen: 系统框架"
layout: post
date: 2020-03-01 22:10
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
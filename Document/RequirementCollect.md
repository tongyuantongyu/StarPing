# 需求获取记录

## 需求获取方法

1. 人类学调查  
2. 可用性调查
3. 模型探究

我们设计的系统是一个偏向专业化的系统，项目的来源便是我（队长）本身的一个需求。因而我本身就对整个项目的需求背景十分熟悉，且在平时使用已有工具的过程中，我就积累了许多关于既有方案存在的不足，因而较为熟悉项目的需求。

人类学调查部分，我搜集了在相关的论坛等网站上关于这类话题的讨论，以了解用户遇到的真实问题和他们期待的解决方法。

可用性调查部分，源于我自己在这个过程中使用各种工具的经验，一方面它们为我提供了思路和基础构思，另一方面我也从实际的应用当中体会到了它们存在的不足。

模型探究部分，则是对网页逻辑的探索。这是一个面相用户的网站，网站上的各种操作需要有符合用户操作的逻辑。因此我们使用了模型探究来设计用户交互的模式。

## 需求获取过程

### 人类学调查

在这一个部分中，我搜集了相关论坛上用户的讨论，找出了广泛存在的几个问题。

1. 不知道如何评价服务质量，仅根据价格/宣传便选购了服务，结果效果很不理想。  
2. 针对偶发性的问题，缺少必要的信息导致难以判断原因。  
3. 服务质量受时间影响波动大，服务质量在晚高峰时段出现明显下滑。  

### 可用性调查

这一部分主要是我自身对服务质量评判的经验谈。

要评判网络连接质量，一般需要以下几个步骤:  
1. 使用系统的ping工具观察到目标服务器的延迟。（需要评判的有三个因素：绝对数字、延迟的上下波动程度以及未收到响应的数据包个数）  
2. 使用系统的路由追踪工具（windows下的tracert、linux下的traceroute和mtr）观察连接到服务器途径的路由节点以及每一个节点的响应延迟。
3. 如有必要，还可以测试文件下载速度。

上述过程需要连续多天在不同时段、不同网络条件下测试，才能得出准确的服务质量。网络故障时常是区域性、隐性的，不会直接造成服务完全断线，被uptime工具记录下来，但是却会对用户体验造成影响，这些都是不自行测试无法判明的细节问题。  

现在存在一个叫做smokeping的程序，可以完成持续性的延迟测试，但存在几个问题。

1. 仅支持记录到目标的延迟，当回溯故障时无法回顾路由信息分析故障原因。  
2. 设计思路较老，大多数图表渲染在服务端运行，服务器负载很高，数据更新时界面抖动也影响浏览体验。  
3. 网页界面没有移动端适配，在手机等移动设备上浏览十分不便。  
4. 程序依赖多，配置复杂，不适合在嵌入式等特殊系统环境下进行部署。  

### 模型探究

我们使用模型探究的方法分析用户界面的设计。我们通过对现有的各种网站的操作逻辑和界面进行分析，基于对用户习惯和其它方面的考虑，用户界面的设计要满足以下三个要求。

1. 要方便用户查看数据，减少不必要的操作。  
2. 要对多种屏幕尺寸做适配，在桌面端和移动端都有良好的体验。  
3. 要合理呈现数据，使用惰性加载的方式，减轻对服务器和用户设备的负担。

## 需求排序

由于本系统需要长时间运行，且需要频繁重复进行测试，故在功能选择上我们排除掉了对网络资源需求较高的文件下载速度测试，而把注意力集中在基于ICMP数据包的延迟和路由记录上，以免对测试节点和被测目标造成过大的负担。

用户界面部分我们根据团队开发的可用时间，调低了前端管理系统的开发优先级，优先保证数据展现功能的实现。

最终我们将需求分为了三类。一级需求是基本功能，系统运转必须包含这些功能。二级需求是尽量完成的需求，否则我们的系统没有特色亮点。三级需求是可以考虑的需求，试项目进度可以考虑实现其中的部分。

以下是需求分类：

### 一级需求：必须完成

ICMP数据包收发及计时  
基于HTTP的数据上报  
数据库设计  
存储上报数据  
数据API  
延迟波动图绘制  
路由追踪结果表格显示  

### 二级需求：尽力完成

动态获取监测目标  
数据缓存及上报重试  
基于其他手段的数据上报  
Planet端高跨平台性  
监测目标及监测节点管理接口  
数据API安全保护及反爬取限制  
响应式用户界面  
单页式网页应用构建  

### 三级需求：考虑实现

支持非TCP/UDP模式下的Ping操作  
合并旧数据，增大记录时间间隔，减小数据大小
网页管理界面

<hr>

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。
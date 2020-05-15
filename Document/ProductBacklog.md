# Product Backlog

产品（项目）名称: StarPing  
产品负责人: None Team  
总工作量: 93.00  
注释: 以一周(7天)视为Sprint的一个周期  


| PBI_ID | 优先级 | Backlog类型 | 功能模块 | 功能性/非功能性 | 用户故事（产品Backlog条目描述） | 验收条件（满意条件） | 复杂度 | Sprint | "初始工作量估计(用户故事点)" | 调整系数 | "调整后工作量估计(用户故事点)" | 状态 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| PBI_01 | 10 | 新需求 | Planet | 功能性 | 向127.0.0.1发送ICMP Echo数据包，并在规定时间内接收。 | 在1ms内100%收到响应数据包。 | 6 | Sprint1 | 8 | 1 | 8 | 未完成 |
| PBI_02 | 9 | 新需求 | Planet | 功能性 | 向多个IP发送正常/TTL极小的数据包，根据响应获得对应目标IP。 | 获得对应目标IP地址。 | 6 | Sprint1 | 6 | 1.5 | 9 | 未完成 |
| PBI_03 | 8 | 新需求 | Planet | 功能性 | 将PBI_01与PBI_02测得的结果数据通过HTTP POST传出。 | 成功通过POST传出数据。 | 4 | Sprint1 | 6 | 1 | 6 | 未完成 |
| PBI_04 | 7 | 新需求 | Star (Backend) | 功能性 | 根据系统规格设计数据库。 | 成功设计数据库，通过基本测试。 | 4 | Sprint1 | 7 | 1 | 7 | 未完成 |
| PBI_05 | 7 | 新需求 | Star (Backend) | 功能性 | Star接收来自Planet传来的数据，并存入数据库。 | 数据成功存入数据库。 | 1 | Sprint1 | 2 | 1 | 2 | 未完成 |
| --- |
| PBI_11 | 9 | 新需求 | Star (Backend) | 功能性 | 根据收到的API参数，Star返回对应的数据。 | 成功传出数据。 | 4 | Sprint2 | 4 | 1 | 4 | 未完成 |
| PBI_12 | 8 | 新需求 | Star (Backend) | 功能性 | 增删Planet节点和测试目标。 | 改变节点和测试目标后，系统正常运转。 | 7 | Sprint2 | 10 | 2 | 20 | 未完成 |
| PBI_13 | 8 | 新需求 | Star (Backend) | 功能性 | Star能够检查请求是否合法，自动过滤非法请求，并限制请求速度。 | 成功通过安全性检测。 | 3 | Sprint2 | 5 | 1 | 5 | 未完成 |
| PBI_14 | 7 | 新需求 | Star (Backend) | 功能性 | 自动将超过一个月的旧数据合并计算为时间跨度更大的数据。 | 系统成功合成数据并存入数据库。 | 2 | Sprint2 | 3 | 1 | 3 | 未完成 |
| --- |
| PBI_22 | 9 | 新需求 | Star (Frontend) | 功能性 | 根据后端提供的数据绘制出延迟曲线。 | 成功接收数据并可视化显示波动图。 | 7 | Sprint3 | 10 | 1.5 | 15 | 未完成 |
| PBI_23 | 9 | 新需求 | Star (Frontend) | 功能性 | 将后端提供的路由追踪数据以表格形式呈现。 | 成功接收数据并可视化显示表格。 | 3 | Sprint3 | 4 | 1 | 4 | 未完成 |
| PBI_24 | 8 | 新需求 | Star (Frontend) | 功能性 | 动态向后端发送HTTP请求获取数据。 | 成功发送HTTP请求。 | 3 | Sprint3 | 4 | 1 | 4 | 未完成 |
| PBI_25 | 8 | 新需求 | Star (Frontend) | 功能性 | 周期请求后端获取新数据更新图表。 | 在规定周期内成功请求、接收、更新数据。 | 2 | Sprint3 | 3 | 1 | 3 | 未完成 |

<hr>

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。
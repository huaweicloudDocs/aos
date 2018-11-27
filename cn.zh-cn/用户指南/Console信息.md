# Console信息<a name="aos_01_9022"></a>

Console字段描述服务管理控制台相关信息，管理控制台用于管理服务实例，一般会带UI界面，方便使用者直观的管理服务实例。

Console程序包即服务控制台镜像包，如果在Service.yml中没有填写ConsolePkg的URL地址，则用户需要单独提供该镜像包。该镜像包将会被上传至镜像仓库，并作为ConsolePkg的地址。

如果Service.yml没有写ConsolePkg的地址，也不独立提供Console镜像包，则认为该服务不需要启动独立的Console控制台，而是每个服务实例有自己的Console界面。

```
Console:
  Source: Broker/Service
  ConsolePkg: ConsoleImageName   #Console镜像包地址
  Entry: /provision/path
  Port: 18081                    #程序监听端口
  CDM: cd /home/app;nodejs console   #可选
  MemoryLimit：500               #限制broker启动时内存使用量
```

Console信息各字段说明请参见[表1](#zh-cn_topic_0109933550_table93812916588)。

**表 1**  Console字段说明

<a name="zh-cn_topic_0109933550_table93812916588"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933550_row16381494585"><th class="cellrowborder" valign="top" width="28.199999999999996%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933550_p3381139125811"><a name="zh-cn_topic_0109933550_p3381139125811"></a><a name="zh-cn_topic_0109933550_p3381139125811"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="71.8%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933550_p1338199195816"><a name="zh-cn_topic_0109933550_p1338199195816"></a><a name="zh-cn_topic_0109933550_p1338199195816"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933550_row238219145813"><td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933550_p12382109165818"><a name="zh-cn_topic_0109933550_p12382109165818"></a><a name="zh-cn_topic_0109933550_p12382109165818"></a>Source</p>
</td>
<td class="cellrowborder" valign="top" width="71.8%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933550_p438210915818"><a name="zh-cn_topic_0109933550_p438210915818"></a><a name="zh-cn_topic_0109933550_p438210915818"></a>描述服务管理控制软件包的出处。</p>
<a name="zh-cn_topic_0109933550_ul17382395582"></a><a name="zh-cn_topic_0109933550_ul17382395582"></a><ul id="zh-cn_topic_0109933550_ul17382395582"><li>值为Broker，则认为Console与Broker程序是合设的。即一个程序同时完成Broker与Console功能。</li><li>值为Service，则认为Console是由每个服务实例独立提供的。即每个实例有自己的管理控制台，而不是一个独立控制台程序管理所有的实例。</li><li>Console为独立程序，则该字段可以不填，由ConsolePkg字段指定。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0109933550_row1138229195819"><td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933550_p038213975812"><a name="zh-cn_topic_0109933550_p038213975812"></a><a name="zh-cn_topic_0109933550_p038213975812"></a>ConsolePkg</p>
</td>
<td class="cellrowborder" valign="top" width="71.8%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933550_p33822925810"><a name="zh-cn_topic_0109933550_p33822925810"></a><a name="zh-cn_topic_0109933550_p33822925810"></a>表示服务管理控制台为独立程序，并指定镜像包地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933550_row738314912582"><td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933550_p1038309145813"><a name="zh-cn_topic_0109933550_p1038309145813"></a><a name="zh-cn_topic_0109933550_p1038309145813"></a>Entry</p>
</td>
<td class="cellrowborder" valign="top" width="71.8%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933550_p6383119155816"><a name="zh-cn_topic_0109933550_p6383119155816"></a><a name="zh-cn_topic_0109933550_p6383119155816"></a>控制台入口相对URL路径。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933550_row738319912581"><td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933550_p14383179135817"><a name="zh-cn_topic_0109933550_p14383179135817"></a><a name="zh-cn_topic_0109933550_p14383179135817"></a>Port</p>
</td>
<td class="cellrowborder" valign="top" width="71.8%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933550_p838349195816"><a name="zh-cn_topic_0109933550_p838349195816"></a><a name="zh-cn_topic_0109933550_p838349195816"></a>用于指定Console程序监听的端口，是在容器内监听的端口。若填空则默认为18081端口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933550_row13565323267"><td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933550_p16937182152818"><a name="zh-cn_topic_0109933550_p16937182152818"></a><a name="zh-cn_topic_0109933550_p16937182152818"></a>CDM</p>
</td>
<td class="cellrowborder" valign="top" width="71.8%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933550_p169371625288"><a name="zh-cn_topic_0109933550_p169371625288"></a><a name="zh-cn_topic_0109933550_p169371625288"></a>Console的启动命令（如果为独立程序的话），为可选字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933550_row195174810378"><td class="cellrowborder" valign="top" width="28.199999999999996%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933550_p74951910101611"><a name="zh-cn_topic_0109933550_p74951910101611"></a><a name="zh-cn_topic_0109933550_p74951910101611"></a>MemoryLimit</p>
</td>
<td class="cellrowborder" valign="top" width="71.8%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933550_p1072194095317"><a name="zh-cn_topic_0109933550_p1072194095317"></a><a name="zh-cn_topic_0109933550_p1072194095317"></a>限制Console启动的内存，为可选字段。</p>
<p id="zh-cn_topic_0109933550_p14377174625315"><a name="zh-cn_topic_0109933550_p14377174625315"></a><a name="zh-cn_topic_0109933550_p14377174625315"></a>默认值为：1024M。</p>
<p id="zh-cn_topic_0109933550_p154951310141613"><a name="zh-cn_topic_0109933550_p154951310141613"></a><a name="zh-cn_topic_0109933550_p154951310141613"></a>若Broker已经规定了内存使用量，Console的内存限制值将和Broker的内存限制值相同，此时memorylimit的重复赋值无效。</p>
</td>
</tr>
</tbody>
</table>


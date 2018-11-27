# Broker信息<a name="aos_01_9021"></a>

指定Broker相关信息。

```
Broker: #Broker相关信息
  Address: http://XXX     # 第三方部署的 broker 地址，若填了值，则AOS上不再部署 broker
  BrokerPkg: BrokerImageName  #Broker包地址
  Port: 18081  #程序监听端口（容器内）
  DashboardPattern: /index.php?username={user_name} #无broker时，实例界面入口
  CMD: cd /home/app;./broker  #可选
  MemoryLimit：500  #限制broker启动时内存使用量
  Volume: [/host/path, /container/path] #可选
  CustomerTag:
    nettype: 2
```

Broker信息各字段说明请参见[表1](#zh-cn_topic_0109933549_table721281819310)。

**表 1**  Broker字段说明

<a name="zh-cn_topic_0109933549_table721281819310"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933549_row202120185318"><th class="cellrowborder" valign="top" width="32.89%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933549_p52126189315"><a name="zh-cn_topic_0109933549_p52126189315"></a><a name="zh-cn_topic_0109933549_p52126189315"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="67.11%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933549_p1421313187316"><a name="zh-cn_topic_0109933549_p1421313187316"></a><a name="zh-cn_topic_0109933549_p1421313187316"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933549_row208881787121"><td class="cellrowborder" valign="top" width="32.89%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933549_p12888198201213"><a name="zh-cn_topic_0109933549_p12888198201213"></a><a name="zh-cn_topic_0109933549_p12888198201213"></a>Address</p>
</td>
<td class="cellrowborder" valign="top" width="67.11%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933549_p1988811851217"><a name="zh-cn_topic_0109933549_p1988811851217"></a><a name="zh-cn_topic_0109933549_p1988811851217"></a>Broker地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933549_row1421319189313"><td class="cellrowborder" valign="top" width="32.89%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933549_p15213101893113"><a name="zh-cn_topic_0109933549_p15213101893113"></a><a name="zh-cn_topic_0109933549_p15213101893113"></a>BrokerPkg</p>
</td>
<td class="cellrowborder" valign="top" width="67.11%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933549_p721381833112"><a name="zh-cn_topic_0109933549_p721381833112"></a><a name="zh-cn_topic_0109933549_p721381833112"></a>Broker镜像包地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933549_row3214141883110"><td class="cellrowborder" valign="top" width="32.89%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933549_p42151618193111"><a name="zh-cn_topic_0109933549_p42151618193111"></a><a name="zh-cn_topic_0109933549_p42151618193111"></a>Port</p>
</td>
<td class="cellrowborder" valign="top" width="67.11%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933549_p1321513181312"><a name="zh-cn_topic_0109933549_p1321513181312"></a><a name="zh-cn_topic_0109933549_p1321513181312"></a>用于指定Broker程序监听的端口，是在容器内监听的端口。可选，如果不填默认为18081端口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933549_row4215191813112"><td class="cellrowborder" valign="top" width="32.89%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933549_p1821561812314"><a name="zh-cn_topic_0109933549_p1821561812314"></a><a name="zh-cn_topic_0109933549_p1821561812314"></a>DashboardPattern</p>
</td>
<td class="cellrowborder" valign="top" width="67.11%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933549_p192151818123116"><a name="zh-cn_topic_0109933549_p192151818123116"></a><a name="zh-cn_topic_0109933549_p192151818123116"></a>表示服务实例的界面的URL相对路径，主要给无需开发Broker场景使用。</p>
<p id="zh-cn_topic_0109933549_p12160183317"><a name="zh-cn_topic_0109933549_p12160183317"></a><a name="zh-cn_topic_0109933549_p12160183317"></a>本字段的路径中，大括号内的值表示待定，真实的值会在实例启动后，由实际值替换。其值会从credential中获取。因此要求{key}中的key必须在credential中存在。</p>
<p id="zh-cn_topic_0109933549_p1216121813119"><a name="zh-cn_topic_0109933549_p1216121813119"></a><a name="zh-cn_topic_0109933549_p1216121813119"></a>例如：DashboardPattern: /index.php?username={<em id="zh-cn_topic_0109933549_i22169181314"><a name="zh-cn_topic_0109933549_i22169181314"></a><a name="zh-cn_topic_0109933549_i22169181314"></a>user_name</em>}</p>
<p id="zh-cn_topic_0109933549_p2021681814311"><a name="zh-cn_topic_0109933549_p2021681814311"></a><a name="zh-cn_topic_0109933549_p2021681814311"></a>生成的实例credential为: {"<em id="zh-cn_topic_0109933549_i92166188318"><a name="zh-cn_topic_0109933549_i92166188318"></a><a name="zh-cn_topic_0109933549_i92166188318"></a>user_name</em>": "t00148181"}</p>
<p id="zh-cn_topic_0109933549_p1921616189318"><a name="zh-cn_topic_0109933549_p1921616189318"></a><a name="zh-cn_topic_0109933549_p1921616189318"></a>那么最终生成的实例入口地址为：/index.php?username=t00148181</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933549_row14494161071615"><td class="cellrowborder" valign="top" width="32.89%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933549_p74951910101611"><a name="zh-cn_topic_0109933549_p74951910101611"></a><a name="zh-cn_topic_0109933549_p74951910101611"></a>MemoryLimit</p>
</td>
<td class="cellrowborder" valign="top" width="67.11%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933549_p1295636135311"><a name="zh-cn_topic_0109933549_p1295636135311"></a><a name="zh-cn_topic_0109933549_p1295636135311"></a>限制Broker启动的内存，为可选字段。</p>
<p id="zh-cn_topic_0109933549_p154951310141613"><a name="zh-cn_topic_0109933549_p154951310141613"></a><a name="zh-cn_topic_0109933549_p154951310141613"></a>默认值为：1024M。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933549_row19216918113116"><td class="cellrowborder" valign="top" width="32.89%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933549_p52161318103118"><a name="zh-cn_topic_0109933549_p52161318103118"></a><a name="zh-cn_topic_0109933549_p52161318103118"></a>CMD</p>
</td>
<td class="cellrowborder" valign="top" width="67.11%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933549_p8216181813318"><a name="zh-cn_topic_0109933549_p8216181813318"></a><a name="zh-cn_topic_0109933549_p8216181813318"></a>启动Broker的方法（启动命令），为可选字段。</p>
</td>
</tr>
</tbody>
</table>


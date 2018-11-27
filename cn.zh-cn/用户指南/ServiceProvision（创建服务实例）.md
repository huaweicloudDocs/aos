# ServiceProvision（创建服务实例）<a name="aos_01_9024"></a>

该字段描述新建一个服务实例所需要的相关信息。

```
ServiceProvision:
  Source: Broker/Console
  Path: /provision/path
  SkipApproval: false #默认需要审批
  Parameters:
    Key1: 
      type: string
    Key_2: 
      type: string
```

ServiceProvision各字段说明请参见[表1](#zh-cn_topic_0109933552_table1314253217597)。

**表 1**  ServiceProvision字段说明

<a name="zh-cn_topic_0109933552_table1314253217597"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933552_row814383211594"><th class="cellrowborder" valign="top" width="28.000000000000004%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933552_p51431832175919"><a name="zh-cn_topic_0109933552_p51431832175919"></a><a name="zh-cn_topic_0109933552_p51431832175919"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="72%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933552_p161432032165916"><a name="zh-cn_topic_0109933552_p161432032165916"></a><a name="zh-cn_topic_0109933552_p161432032165916"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933552_row914314320590"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933552_p161431632175911"><a name="zh-cn_topic_0109933552_p161431632175911"></a><a name="zh-cn_topic_0109933552_p161431632175911"></a>Source</p>
</td>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933552_p114333216598"><a name="zh-cn_topic_0109933552_p114333216598"></a><a name="zh-cn_topic_0109933552_p114333216598"></a>指明新建服务实例的界面由服务提供。</p>
<a name="zh-cn_topic_0109933552_ul1714353275911"></a><a name="zh-cn_topic_0109933552_ul1714353275911"></a><ul id="zh-cn_topic_0109933552_ul1714353275911"><li>值为Broker，则认为新建实例的界面与Broker程序是合设的。即创建新实例的界面由Broker提供。</li><li>值为Console，则认为新建实例的界面与Console程序是合设的。即创建新实例的界面由Console提供。</li><li>如果没有，则认为创建新实例的界面，由AOS提供。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0109933552_row5144123213591"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933552_p131443329595"><a name="zh-cn_topic_0109933552_p131443329595"></a><a name="zh-cn_topic_0109933552_p131443329595"></a>Path</p>
</td>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933552_p4144133210597"><a name="zh-cn_topic_0109933552_p4144133210597"></a><a name="zh-cn_topic_0109933552_p4144133210597"></a>新建实例页面的相对URL路径。</p>
<a name="zh-cn_topic_0109933552_ul13144183205912"></a><a name="zh-cn_topic_0109933552_ul13144183205912"></a><ul id="zh-cn_topic_0109933552_ul13144183205912"><li>Broker的地址+Path</li><li>Console的地址+Path</li><li>服务实例地址+Path</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0109933552_row1956002214519"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933552_p14561122218453"><a name="zh-cn_topic_0109933552_p14561122218453"></a><a name="zh-cn_topic_0109933552_p14561122218453"></a>SkipApproval</p>
</td>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933552_p1756182284512"><a name="zh-cn_topic_0109933552_p1756182284512"></a><a name="zh-cn_topic_0109933552_p1756182284512"></a>指明新建实例是否需要管理员审批。默认情况下，订购服务都需审批。在有自动化需求，或者实例是私有的情况下，可以考虑设置为免审批服务。</p>
<a name="zh-cn_topic_0109933552_ul73411684720"></a><a name="zh-cn_topic_0109933552_ul73411684720"></a><ul id="zh-cn_topic_0109933552_ul73411684720"><li>false：需要审批。</li><li>true：不需要审批。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0109933552_row15144103235918"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933552_p8144173275918"><a name="zh-cn_topic_0109933552_p8144173275918"></a><a name="zh-cn_topic_0109933552_p8144173275918"></a>Parameters</p>
</td>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933552_p01441032155914"><a name="zh-cn_topic_0109933552_p01441032155914"></a><a name="zh-cn_topic_0109933552_p01441032155914"></a>指明新建服务实例时，需要填写的信息。该信息会传递给Broker用于控制启动实例。</p>
<div class="note" id="zh-cn_topic_0109933552_note114523215598"><a name="zh-cn_topic_0109933552_note114523215598"></a><a name="zh-cn_topic_0109933552_note114523215598"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933552_p5145183211599"><a name="zh-cn_topic_0109933552_p5145183211599"></a><a name="zh-cn_topic_0109933552_p5145183211599"></a>当界面由AOS提供，并且出现该字段时，才会生效。</p>
</div></div>
</td>
</tr>
</tbody>
</table>


# Plans（服务套餐）<a name="aos_01_9025"></a>

用于控制实例规格的大小，会在订购服务实例界面展示。

该字段由多个套餐描述组成，每个套餐包含如下内容：

```
Plans: #服务套餐相关信息
  - Name: small    #没带Blueprint字段，则会使用DefaultTemplateName的Blueprint文件
    Description: this is small plan, only with 4G memory
    Metadata: 
      Key1: 
        type: string
        alias: 关键数值1
      Key_3: 
        type: string
        alias: 关键数值3
  - Name: large
    Description: this is large plan, with 32G memory
    Metadata: 
      Key1: 
        type: string
      Key_2: 
        type: string
        alias: 关键数值2
        default: value2
        read_only: false    
        optional: false
        check: true
        changed: false
        range_min: 0
        range_max: 20
    Blueprint: "PlanTemplateName:1,0" #可选，如果不存在，则使用DefaultTemplateName
    MeteringItems: #可选，指定计量&计费因子
      - ItemName: BDI #收费项目
        Specification: large #收费规格
        Accumulate: [key1] #额外累计项。指定Metadata中的字段为计费累计项
      - ItemName: VM
```

Plans各字段说明请参见[表1](#zh-cn_topic_0109933555_table17682596010)。

**表 1**  Plans字段说明

<a name="zh-cn_topic_0109933555_table17682596010"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933555_row968115920015"><th class="cellrowborder" valign="top" width="27.439999999999998%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933555_p26865919015"><a name="zh-cn_topic_0109933555_p26865919015"></a><a name="zh-cn_topic_0109933555_p26865919015"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="72.56%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933555_p36810595011"><a name="zh-cn_topic_0109933555_p36810595011"></a><a name="zh-cn_topic_0109933555_p36810595011"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933555_row468759709"><td class="cellrowborder" valign="top" width="27.439999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933555_p186917591602"><a name="zh-cn_topic_0109933555_p186917591602"></a><a name="zh-cn_topic_0109933555_p186917591602"></a>Name</p>
</td>
<td class="cellrowborder" valign="top" width="72.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933555_p8691959602"><a name="zh-cn_topic_0109933555_p8691959602"></a><a name="zh-cn_topic_0109933555_p8691959602"></a>套餐名。</p>
<div class="note" id="zh-cn_topic_0109933555_note1369159403"><a name="zh-cn_topic_0109933555_note1369159403"></a><a name="zh-cn_topic_0109933555_note1369159403"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933555_p46917591501"><a name="zh-cn_topic_0109933555_p46917591501"></a><a name="zh-cn_topic_0109933555_p46917591501"></a>如果套餐名为custom，表示自定义，在订购时，所有参数是可以由购买者调整。其他套餐名，购买者只能查询具体参数值，不能修改参数值。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0109933555_row7699599011"><td class="cellrowborder" valign="top" width="27.439999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933555_p126915597010"><a name="zh-cn_topic_0109933555_p126915597010"></a><a name="zh-cn_topic_0109933555_p126915597010"></a>Description</p>
</td>
<td class="cellrowborder" valign="top" width="72.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933555_p1069459307"><a name="zh-cn_topic_0109933555_p1069459307"></a><a name="zh-cn_topic_0109933555_p1069459307"></a>套餐详情。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933555_row176914596015"><td class="cellrowborder" valign="top" width="27.439999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933555_p16692598010"><a name="zh-cn_topic_0109933555_p16692598010"></a><a name="zh-cn_topic_0109933555_p16692598010"></a>Metadata</p>
</td>
<td class="cellrowborder" valign="top" width="72.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933555_p12694591017"><a name="zh-cn_topic_0109933555_p12694591017"></a><a name="zh-cn_topic_0109933555_p12694591017"></a>套餐中可以设置调整的信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933555_row186915591202"><td class="cellrowborder" valign="top" width="27.439999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933555_p137013595012"><a name="zh-cn_topic_0109933555_p137013595012"></a><a name="zh-cn_topic_0109933555_p137013595012"></a>Blueprint</p>
</td>
<td class="cellrowborder" valign="top" width="72.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933555_p107012592003"><a name="zh-cn_topic_0109933555_p107012592003"></a><a name="zh-cn_topic_0109933555_p107012592003"></a>指定套餐应用使用的Blueprint文件名及版本号。</p>
<p id="zh-cn_topic_0109933555_p1170125915020"><a name="zh-cn_topic_0109933555_p1170125915020"></a><a name="zh-cn_topic_0109933555_p1170125915020"></a>如果没有指定，则会按以下规则查找并使用Blueprint文件：blueprint.套餐名.yml，版本号默认为1.0。</p>
<p id="zh-cn_topic_0109933555_p070159008"><a name="zh-cn_topic_0109933555_p070159008"></a><a name="zh-cn_topic_0109933555_p070159008"></a>Blueprint目录下用于存放服务程序的启动模板，一个模板可以控制程序的所有启动依赖，包括使用的VM资源，网络配置，组件间启动先后顺序等。Blueprint规范符合TOSCA模型。</p>
<p id="zh-cn_topic_0109933555_p87015596016"><a name="zh-cn_topic_0109933555_p87015596016"></a><a name="zh-cn_topic_0109933555_p87015596016"></a>Blueprint目录下可以同时存在多个Blueprint文件，命名必须为ServiceName.套餐名.yml，表示支持不同的套餐可以使用不同的Blueprint文件，如果不是额外设置，默认所有套餐都是有同一个Blueprint文件。</p>
<div class="note" id="zh-cn_topic_0109933555_note87016592006"><a name="zh-cn_topic_0109933555_note87016592006"></a><a name="zh-cn_topic_0109933555_note87016592006"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933555_p167018591102"><a name="zh-cn_topic_0109933555_p167018591102"></a><a name="zh-cn_topic_0109933555_p167018591102"></a>创建服务实例时，用户选中的套餐对应的BlueprintID会传递给服务的Broker，便于快速根据Blueprint启动实例。当存在多个Blueprint文件时，启动实例时具体使用哪个，这个是由用户创建服务实例时，由AOS根据套餐转换为对应的Blueprint_ID，传递给Broker的，由Broker根据“套餐名”和Blueprint_ID来控制启动的实例规格大小。</p>
<p id="zh-cn_topic_0109933555_p1071559406"><a name="zh-cn_topic_0109933555_p1071559406"></a><a name="zh-cn_topic_0109933555_p1071559406"></a>Blueprint文件也可以在服务软件包内部。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0109933555_row97117598013"><td class="cellrowborder" valign="top" width="27.439999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933555_p871135919020"><a name="zh-cn_topic_0109933555_p871135919020"></a><a name="zh-cn_topic_0109933555_p871135919020"></a>MeteringItems</p>
</td>
<td class="cellrowborder" valign="top" width="72.56%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933555_p36071594234"><a name="zh-cn_topic_0109933555_p36071594234"></a><a name="zh-cn_topic_0109933555_p36071594234"></a>用于指定当前发布服务的计量因子。<span>AOS</span>会根据这里指定的字段，详细记录被订购的服务实例关于这些字段相关的使用量/使用时长，并转交给计费系统。计费<span>系统负责根据使用情况进行计费。计量计费规格与套餐相关。</span></p>
<a name="zh-cn_topic_0109933555_ul20719591902"></a><a name="zh-cn_topic_0109933555_ul20719591902"></a><ul id="zh-cn_topic_0109933555_ul20719591902"><li>ItemName：用于指定当前套餐下的计量项目名称，若为空默认按套餐名称来计量。如果一个套餐有多个计量项目，那同一个实例就会按照计量项目分别记录使用情况（输出多个话单）。</li><li>Specification：用于指定当前套餐下的计量项目的规格，若为空默认按套餐名称来计量。</li><li>Accumulate：当前收费项目下的累计项，用于指定Metadata中的哪个字段为计费累计项。<div class="note" id="zh-cn_topic_0109933555_note0722591807"><a name="zh-cn_topic_0109933555_note0722591807"></a><a name="zh-cn_topic_0109933555_note0722591807"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933555_p7721595019"><a name="zh-cn_topic_0109933555_p7721595019"></a><a name="zh-cn_topic_0109933555_p7721595019"></a>这里能指定的计量累计项，当前必须限定在Metadata字段列举的范围内。也就是Metadata如果有指定两个Key，只能从这两个Key中选择，超出范围则会被当做无效忽略。</p>
</div></div>
</li></ul>
</td>
</tr>
</tbody>
</table>


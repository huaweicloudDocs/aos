# Service基本信息<a name="aos_01_9019"></a>

服务描述文件Service.yml中所有的参数，都是允许用户自定义的。目前用户能够控制的参数有以下五类：

-   服务元数据：ServiceMatadata。
-   发布阶段参数：PublishParameter。
-   订购阶段参数：ProvisionParameter。
-   绑定阶段参数：BindingParameter。
-   套餐阶段参数：PlanMetadata。

以上参数中，每类参数均可以再定义多个参数，每个参数必须先指定类型，再根据类型设置对应的参数属性。当前支持的参数类型有：

-   数字：float。
-   字符串：string。
-   密码：pw。
-   枚举：enum。
-   docker镜像：image。
-   布尔：bool。

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >yml文件中书写格式以两个空格分层，不能有tab键，否则发布服务时配置文件会报格式错误。  


服务基本信息。

```
Service: #最基础的服务信息
  Name: hadoop
  Alias: 大数据计算 #支持中文
  Vendor: ServiceCatalog  #服务发布商
  Catalog: compute #服务分类(大类)
  Tags: [hadoop, data] #服务类型(小类)
  Mode: passthrough  #可选，默认不填表明普通模式 ，passthrough是透传模式
  ServicePkg: http://some.url/version  #服务包地址
  Blueprint: "DefaultTemplateName:1.0"  #设计包，可选（逻辑多租不需要）
  Dependency: #依赖的服务的标签，可选
    - ServiceTag-A
    - ServiceTag-B
  Description: description of this service  #可选
  SDK: repository/filename/version   #可选
  Logo: http://logo.address.url/   #可选
  Help: http://help.address.url/   #可选  
  UsePaasResource: false   #是否使用paas资源，false则部署在用户资源下
```

Service信息各字段说明请参见[表1](#zh-cn_topic_0109933547_table71521551123020)。

**表 1**  Service字段说明

<a name="zh-cn_topic_0109933547_table71521551123020"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933547_row9153165123017"><th class="cellrowborder" valign="top" width="21%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933547_p15153151193018"><a name="zh-cn_topic_0109933547_p15153151193018"></a><a name="zh-cn_topic_0109933547_p15153151193018"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="79%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933547_p515325173013"><a name="zh-cn_topic_0109933547_p515325173013"></a><a name="zh-cn_topic_0109933547_p515325173013"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933547_row19153175133018"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p17153155123017"><a name="zh-cn_topic_0109933547_p17153155123017"></a><a name="zh-cn_topic_0109933547_p17153155123017"></a>Name</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p5153251203012"><a name="zh-cn_topic_0109933547_p5153251203012"></a><a name="zh-cn_topic_0109933547_p5153251203012"></a>服务名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row15153125113016"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p8154351113012"><a name="zh-cn_topic_0109933547_p8154351113012"></a><a name="zh-cn_topic_0109933547_p8154351113012"></a>Alias</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p815495183018"><a name="zh-cn_topic_0109933547_p815495183018"></a><a name="zh-cn_topic_0109933547_p815495183018"></a>服务别名，支持中文。主要方便对英文服务名字有更直观的理解。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row215465163013"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p11154165110305"><a name="zh-cn_topic_0109933547_p11154165110305"></a><a name="zh-cn_topic_0109933547_p11154165110305"></a>Catalog</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p12155651173019"><a name="zh-cn_topic_0109933547_p12155651173019"></a><a name="zh-cn_topic_0109933547_p12155651173019"></a>表示服务大类。例如计算类，资源类，工具类。对应关系如下（大小写不敏感）。</p>
<a name="zh-cn_topic_0109933547_ul1115511515302"></a><a name="zh-cn_topic_0109933547_ul1115511515302"></a><ul id="zh-cn_topic_0109933547_ul1115511515302"><li>Analysis：分析服务</li><li>Compute：计算框架</li><li>MiddleWare：中间件</li><li>DataMarket：数据市场</li><li>Tool：工具类</li><li>Other：其他 （不符合上面所列的，都是其他）</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row12899202974219"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p79005293422"><a name="zh-cn_topic_0109933547_p79005293422"></a><a name="zh-cn_topic_0109933547_p79005293422"></a>Vendor</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p490032944215"><a name="zh-cn_topic_0109933547_p490032944215"></a><a name="zh-cn_topic_0109933547_p490032944215"></a>服务发布商。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row1315635118304"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p18156115123011"><a name="zh-cn_topic_0109933547_p18156115123011"></a><a name="zh-cn_topic_0109933547_p18156115123011"></a>Tags</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p1715695143011"><a name="zh-cn_topic_0109933547_p1715695143011"></a><a name="zh-cn_topic_0109933547_p1715695143011"></a>指定服务标记，用于更进一步设定服务类型。以mysql服务为例，可以有集群版、单机版、开源版。服务上架时，服务名可以选不同的名字，但可以将Tag都记为mysql，表示为同一类型的服务。可以把该字段看着服务的小类。这里支持为发布的服务设置多个Tag。</p>
<div class="note" id="zh-cn_topic_0109933547_note1215665114309"><a name="zh-cn_topic_0109933547_note1215665114309"></a><a name="zh-cn_topic_0109933547_note1215665114309"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933547_p18156175119305"><a name="zh-cn_topic_0109933547_p18156175119305"></a><a name="zh-cn_topic_0109933547_p18156175119305"></a>当指定依赖其他服务时，此字段需要设置成对方的Tag，而不是对方的服务名。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row85345441178"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p135346441677"><a name="zh-cn_topic_0109933547_p135346441677"></a><a name="zh-cn_topic_0109933547_p135346441677"></a>Mode</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p1153454414713"><a name="zh-cn_topic_0109933547_p1153454414713"></a><a name="zh-cn_topic_0109933547_p1153454414713"></a>可选，默认不填表明普通模式 ，passthrough是透传模式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row171561151103018"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p10157195163014"><a name="zh-cn_topic_0109933547_p10157195163014"></a><a name="zh-cn_topic_0109933547_p10157195163014"></a>ServicePkg</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p12157451163017"><a name="zh-cn_topic_0109933547_p12157451163017"></a><a name="zh-cn_topic_0109933547_p12157451163017"></a>软件包地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row315775193010"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p3157351123017"><a name="zh-cn_topic_0109933547_p3157351123017"></a><a name="zh-cn_topic_0109933547_p3157351123017"></a>Blueprint</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p31571951123012"><a name="zh-cn_topic_0109933547_p31571951123012"></a><a name="zh-cn_topic_0109933547_p31571951123012"></a>表示编排设计包的名字及版本号，设计包需要提前上传到模板仓库。设计包文件格式为编排设计包格式。该文件用于描述如何启动软件包。该字段为可选，逻辑多租的实例按理就不需要模板。</p>
<div class="note" id="zh-cn_topic_0109933547_note1515713514302"><a name="zh-cn_topic_0109933547_note1515713514302"></a><a name="zh-cn_topic_0109933547_note1515713514302"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933547_p18731425148"><a name="zh-cn_topic_0109933547_p18731425148"></a><a name="zh-cn_topic_0109933547_p18731425148"></a>若发布服务时套餐不指定其他Blueprint，该套餐就会使用这里配置的Blueprint。若套餐中指定其他Blueprint，会覆盖此默认数值。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row5158951133016"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p715817515309"><a name="zh-cn_topic_0109933547_p715817515309"></a><a name="zh-cn_topic_0109933547_p715817515309"></a>Dependency</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p115815513309"><a name="zh-cn_topic_0109933547_p115815513309"></a><a name="zh-cn_topic_0109933547_p115815513309"></a>当前服务所依赖的服务。</p>
<div class="note" id="zh-cn_topic_0109933547_note31581251193013"><a name="zh-cn_topic_0109933547_note31581251193013"></a><a name="zh-cn_topic_0109933547_note31581251193013"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0109933547_p81581551133020"><a name="zh-cn_topic_0109933547_p81581551133020"></a><a name="zh-cn_topic_0109933547_p81581551133020"></a>请配置为当前服务所依赖服务的Tag，而不是所依赖服务的服务名，支持为当前发布的服务指定多个依赖</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row515945112308"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p71591551143012"><a name="zh-cn_topic_0109933547_p71591551143012"></a><a name="zh-cn_topic_0109933547_p71591551143012"></a>Description</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p16159351113012"><a name="zh-cn_topic_0109933547_p16159351113012"></a><a name="zh-cn_topic_0109933547_p16159351113012"></a>服务的详细描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row11591451183010"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p41591751143018"><a name="zh-cn_topic_0109933547_p41591751143018"></a><a name="zh-cn_topic_0109933547_p41591751143018"></a>SDK</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p615935117307"><a name="zh-cn_topic_0109933547_p615935117307"></a><a name="zh-cn_topic_0109933547_p615935117307"></a>服务的sdk文件地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row17160135133013"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p3160651163020"><a name="zh-cn_topic_0109933547_p3160651163020"></a><a name="zh-cn_topic_0109933547_p3160651163020"></a>Logo</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p1916095115302"><a name="zh-cn_topic_0109933547_p1916095115302"></a><a name="zh-cn_topic_0109933547_p1916095115302"></a>服务的logo图标文件地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row1516025183013"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p516012519306"><a name="zh-cn_topic_0109933547_p516012519306"></a><a name="zh-cn_topic_0109933547_p516012519306"></a>Help</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p1016185163010"><a name="zh-cn_topic_0109933547_p1016185163010"></a><a name="zh-cn_topic_0109933547_p1016185163010"></a>服务的帮助文档地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933547_row1916794614219"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933547_p6167446144212"><a name="zh-cn_topic_0109933547_p6167446144212"></a><a name="zh-cn_topic_0109933547_p6167446144212"></a>UsePaasResource</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933547_p17167146204217"><a name="zh-cn_topic_0109933547_p17167146204217"></a><a name="zh-cn_topic_0109933547_p17167146204217"></a>是否使用paas资源，false则部署在用户资源下。默认为false。</p>
</td>
</tr>
</tbody>
</table>


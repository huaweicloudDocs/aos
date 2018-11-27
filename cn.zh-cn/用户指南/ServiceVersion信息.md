# ServiceVersion信息<a name="aos_01_9020"></a>

指定一个服务多个版本的相关信息，例如不同版本的软件包信息。

```
ServiceVersion:
  MetadataDefine: #服务发布者提供的，用于启动服务实例的信息
    zk: 
      type: image
      alias: 版本参数别名
      default: 默认值
    hadoop: 
      type: string
  VersionArray:
    1.1:
      VersionCode: "1.1"  #版本1.1
      Description: 第一个版本
      Metadata: 
        zk: 10.106.163.207:20202/csc_test3/hadoop:latest
        hadoop: hadoop1
    1.2:
      VersionCode: "1.2"  #版本1.2
      Description: 第二个版本
      Metadata: 
        zk: 10.106.163.207:20202/csc_test3/hadoop:latest
        hadoop: hadoop2
```

ServiceVersion信息各字段说明请参见[表1](#zh-cn_topic_0109933548_table182761311143413)。

**表 1**  ServiceVersion字段说明

<a name="zh-cn_topic_0109933548_table182761311143413"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933548_row1327713114341"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933548_p8277611173420"><a name="zh-cn_topic_0109933548_p8277611173420"></a><a name="zh-cn_topic_0109933548_p8277611173420"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="81%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933548_p19277191103414"><a name="zh-cn_topic_0109933548_p19277191103414"></a><a name="zh-cn_topic_0109933548_p19277191103414"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933548_row12277011183410"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933548_p172771111113419"><a name="zh-cn_topic_0109933548_p172771111113419"></a><a name="zh-cn_topic_0109933548_p172771111113419"></a>MetadataDefine</p>
</td>
<td class="cellrowborder" valign="top" width="81%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933548_p1627716112342"><a name="zh-cn_topic_0109933548_p1627716112342"></a><a name="zh-cn_topic_0109933548_p1627716112342"></a>用于定义不同版本之间共同的参数的格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933548_row52776113341"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933548_p52771111143417"><a name="zh-cn_topic_0109933548_p52771111143417"></a><a name="zh-cn_topic_0109933548_p52771111143417"></a>VersionArray</p>
</td>
<td class="cellrowborder" valign="top" width="81%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933548_p18277711183410"><a name="zh-cn_topic_0109933548_p18277711183410"></a><a name="zh-cn_topic_0109933548_p18277711183410"></a>指定当前服务的多个版本信息，例如不同的服务版本可以指定不同的软件包。每个版本格式介绍如下：</p>
<pre class="screen" id="zh-cn_topic_0109933548_screen17415191363517"><a name="zh-cn_topic_0109933548_screen17415191363517"></a><a name="zh-cn_topic_0109933548_screen17415191363517"></a>  Version:
    VersionCode: "1.2"  #版本1.2
    Description: 第二个版本
    Metadata: 
      zk: hadoop:latest
      hadoop: hadoop2</pre>
<a name="zh-cn_topic_0109933548_ul981815306352"></a><a name="zh-cn_topic_0109933548_ul981815306352"></a><ul id="zh-cn_topic_0109933548_ul981815306352"><li>VersionCode：指定发布服务的版本信息，是字符串类型的。版本格式限定是“A.B”，其中A的范围为0-99，B的范围为0-99。</li><li>Description：当前版本的介绍信息。例如：“1.2版本修复了1.1版本的xxx问题”。</li><li>Metadata：服务发布者提供的，关于服务自身相关的各种属性信息。这些属性信息可以用于启动服务实例，比如软件包的地址信息。内容为Parameter类型。格式为key/value形式。</li></ul>
</td>
</tr>
</tbody>
</table>


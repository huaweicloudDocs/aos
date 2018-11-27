# ServicePublish（服务发布）<a name="aos_01_9023"></a>

用于控制发布服务的属性。

>![](public_sys-resources/icon-note.gif) **说明：**   
>这些参数列表，由界面传给AOS服务管理，服务管理在启动该Broker时，将参数列表作为parameters传递给Broker程序（参数信息AOS全程透传，不关心其内容）。  

```
ServicePublish: #服务发布自定义参数
  ResourcePool: [project1_id, project2_id]  #服务所支持的项目的ID列表
  IsPublic: true  #公共服务or私有服务
  Metering: true #是否需要计量计费
  Parameters:
    DB: 
      type: string
      alias: 数据库
      default: Oracle
      read_only: false    
    user_name: 
      type: string
      alias: 用户名
      default: userA
    password: 
      type: pw
    ip: 
      type: string
    port: 
      type: float
      alias: 端口号
```

ServicePublish各字段说明请参见[表1](#zh-cn_topic_0109933551_table1035212419581)。

**表 1**  ServicePublish字段说明

<a name="zh-cn_topic_0109933551_table1035212419581"></a>
<table><thead align="left"><tr id="zh-cn_topic_0109933551_row535304120583"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0109933551_p17117101919312"><a name="zh-cn_topic_0109933551_p17117101919312"></a><a name="zh-cn_topic_0109933551_p17117101919312"></a>字段名</p>
</th>
<th class="cellrowborder" valign="top" width="67%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0109933551_p1435317414586"><a name="zh-cn_topic_0109933551_p1435317414586"></a><a name="zh-cn_topic_0109933551_p1435317414586"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0109933551_row193531412589"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933551_p103531741195813"><a name="zh-cn_topic_0109933551_p103531741195813"></a><a name="zh-cn_topic_0109933551_p103531741195813"></a>ResourcePool</p>
</td>
<td class="cellrowborder" valign="top" width="67%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933551_p15353104110588"><a name="zh-cn_topic_0109933551_p15353104110588"></a><a name="zh-cn_topic_0109933551_p15353104110588"></a>表示服务允许订购的范围（资源维度）。如果发布时只指定了项目1，那么在其它的项目中就没有权限申请。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933551_row12353184145815"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933551_p19353841205810"><a name="zh-cn_topic_0109933551_p19353841205810"></a><a name="zh-cn_topic_0109933551_p19353841205810"></a>IsPublic</p>
</td>
<td class="cellrowborder" valign="top" width="67%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933551_p15353741145814"><a name="zh-cn_topic_0109933551_p15353741145814"></a><a name="zh-cn_topic_0109933551_p15353741145814"></a>表示服务是否全局可见（可被订购）。如果是公共服务，所有租户都可购买，如果是私有服务，只支持自己租户购买。默认为发布私有服务。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933551_row133531641165814"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933551_p235344185817"><a name="zh-cn_topic_0109933551_p235344185817"></a><a name="zh-cn_topic_0109933551_p235344185817"></a>Metering</p>
</td>
<td class="cellrowborder" valign="top" width="67%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933551_p83535413587"><a name="zh-cn_topic_0109933551_p83535413587"></a><a name="zh-cn_topic_0109933551_p83535413587"></a>用于指定当前发布的服务是否需要进行计量计费。默认为免费（不计量）。</p>
</td>
</tr>
<tr id="zh-cn_topic_0109933551_row193533413583"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0109933551_p035394112582"><a name="zh-cn_topic_0109933551_p035394112582"></a><a name="zh-cn_topic_0109933551_p035394112582"></a>Parameters</p>
</td>
<td class="cellrowborder" valign="top" width="67%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0109933551_p53541414589"><a name="zh-cn_topic_0109933551_p53541414589"></a><a name="zh-cn_topic_0109933551_p53541414589"></a>指定服务发布时需要额外的参数信息，这些参数信息在发布的时候由发布者根据现场情况确定，并会在发布过程中传递给Broker和Console程序，该字段由多个key/value列表组成。</p>
</td>
</tr>
</tbody>
</table>


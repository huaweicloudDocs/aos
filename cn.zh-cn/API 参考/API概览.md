# API概览<a name="aos_02_0002"></a>

<a name="table636420173499"></a>
<table><thead align="left"><tr id="row1936421713499"><th class="cellrowborder" valign="top" width="32%" id="mcps1.1.3.1.1"><p id="p036401754914"><a name="p036401754914"></a><a name="p036401754914"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="68%" id="mcps1.1.3.1.2"><p id="p1364917154914"><a name="p1364917154914"></a><a name="p1364917154914"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1636416178493"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.3.1.1 "><p id="p7364717114914"><a name="p7364717114914"></a><a name="p7364717114914"></a><a href="创建模板.md">模板管理接口</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.1.3.1.2 "><p id="p19208131145113"><a name="p19208131145113"></a><a name="p19208131145113"></a>模板管理接口，包括创建、查询、更新、删除模板的接口等。</p>
<p id="p02091211155119"><a name="p02091211155119"></a><a name="p02091211155119"></a>通过这些接口，您可以创建模板、查询模板列表、更新模板、删除模板、查询指定模板和查询模板输入。</p>
</td>
</tr>
<tr id="row936591714910"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.3.1.1 "><p id="p2036571717494"><a name="p2036571717494"></a><a name="p2036571717494"></a><a href="创建堆栈.md">堆栈管理接口</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.1.3.1.2 "><p id="p14872144045215"><a name="p14872144045215"></a><a name="p14872144045215"></a>堆栈管理接口，包括创建、查询、删除堆栈的接口等。</p>
<p id="p387264025211"><a name="p387264025211"></a><a name="p387264025211"></a>通过这些接口，您可以创建堆栈、删除堆栈，执行堆栈生命周期，查询堆栈列表、堆栈、堆栈元素列表、堆栈元素、堆栈输出、堆栈输入、堆栈执行记录、堆栈执行记录列表。</p>
</td>
</tr>
</tbody>
</table>

## 模板管理接口<a name="section14967428145618"></a>

模板管理接口，包括创建、查询、更新、删除模板的接口等。通过这些接口，您可以创建模板、查询模板列表、更新模板、删除模板、查询指定模板和查询模板输入。

**表 1**  模板管理接口

<a name="table334371126"></a>
<table><thead align="left"><tr id="row2344515214"><th class="cellrowborder" valign="top" width="32%" id="mcps1.2.3.1.1"><p id="p1534413111219"><a name="p1534413111219"></a><a name="p1534413111219"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="68%" id="mcps1.2.3.1.2"><p id="p103441811121"><a name="p103441811121"></a><a name="p103441811121"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row183441814213"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p183441918219"><a name="p183441918219"></a><a name="p183441918219"></a><a href="创建模板.md">创建模板</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p173441811127"><a name="p173441811127"></a><a name="p173441811127"></a><span>通过将本地模板文件上传至服务器的方式来创建模板。</span></p>
</td>
</tr>
<tr id="row334491828"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p183441811426"><a name="p183441811426"></a><a name="p183441811426"></a><a href="查询模板列表.md">查询模板列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p16344013212"><a name="p16344013212"></a><a name="p16344013212"></a>根据提供的参数查询模板列表。</p>
</td>
</tr>
<tr id="row1234410113211"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p1134415110210"><a name="p1134415110210"></a><a name="p1134415110210"></a><a href="更新模板.md">更新模板</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1344712214"><a name="p1344712214"></a><a name="p1344712214"></a>更新模板，包括两种方式：本地上传和URL上传更新。</p>
<p id="p5633939131513"><a name="p5633939131513"></a><a name="p5633939131513"></a>只有当未使用该模板创建堆栈之前才能进行更新。</p>
</td>
</tr>
<tr id="row234413112219"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p183441511622"><a name="p183441511622"></a><a name="p183441511622"></a><a href="删除模板.md">删除模板</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p193441716219"><a name="p193441716219"></a><a name="p193441716219"></a>删除一个指定的模板。</p>
<p id="p5277134417175"><a name="p5277134417175"></a><a name="p5277134417175"></a>只有不存在使用该模板创建的堆栈时才能删除。</p>
</td>
</tr>
<tr id="row1534418114216"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p93441315212"><a name="p93441315212"></a><a name="p93441315212"></a><a href="查询模板.md">查询模板</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p634411320"><a name="p634411320"></a><a name="p634411320"></a>查询指定模板的详细信息，包括模板名称、模板版本、模板描述、创建时间、更新时间等。</p>
</td>
</tr>
<tr id="row143441212211"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p1734414117212"><a name="p1734414117212"></a><a name="p1734414117212"></a><a href="查询模板输入.md">查询模板输入</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p12344412022"><a name="p12344412022"></a><a name="p12344412022"></a>查询指定模板的输入参数。</p>
</td>
</tr>
</tbody>
</table>

## 堆栈管理接口<a name="section59291310185611"></a>

堆栈管理接口，包括创建、查询、删除堆栈的接口等。通过这些接口，您可以创建堆栈、删除堆栈，执行堆栈生命周期，查询堆栈列表、堆栈、堆栈元素列表、堆栈元素、堆栈输出、堆栈输入、堆栈执行记录、堆栈执行记录列表。

**表 2**  堆栈管理接口

<a name="table88711342351"></a>
<table><thead align="left"><tr id="row88716427513"><th class="cellrowborder" valign="top" width="32%" id="mcps1.2.3.1.1"><p id="p1871442156"><a name="p1871442156"></a><a name="p1871442156"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="68%" id="mcps1.2.3.1.2"><p id="p12871194215516"><a name="p12871194215516"></a><a name="p12871194215516"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9609616236"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p060961102315"><a name="p060961102315"></a><a name="p060961102315"></a><a href="创建堆栈.md">创建堆栈</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p18609101132320"><a name="p18609101132320"></a><a name="p18609101132320"></a>创建堆栈，堆栈的输入由模板和输入参数两部分组成。</p>
<a name="ul932460112019"></a><a name="ul932460112019"></a><ul id="ul932460112019"><li>模板：定义了堆栈的骨架，决定了堆栈内部节点的构造以及节点间的关系，以及每个节点的属性的值或来源。</li><li>输入参数：是模板内节点属性值的来源之一，定义在模板的inputs字段下，由模板内的get_input函数触发。</li></ul>
</td>
</tr>
<tr id="row49731192313"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p1197314122314"><a name="p1197314122314"></a><a name="p1197314122314"></a><a href="删除堆栈.md">删除堆栈</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1597341182310"><a name="p1597341182310"></a><a name="p1597341182310"></a>删除一个指定的堆栈。</p>
</td>
</tr>
<tr id="row1035932132312"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p03598219236"><a name="p03598219236"></a><a name="p03598219236"></a><a href="执行堆栈生命周期.md">执行堆栈生命周期</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p53597222314"><a name="p53597222314"></a><a name="p53597222314"></a>执行特定的堆栈生命周期操作。</p>
</td>
</tr>
<tr id="row1453215232317"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p5532112202312"><a name="p5532112202312"></a><a name="p5532112202312"></a><a href="查询堆栈列表.md">查询堆栈列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1626004381212"><a name="p1626004381212"></a><a name="p1626004381212"></a>查询堆栈列表。</p>
</td>
</tr>
<tr id="row1872319272319"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p1172492172314"><a name="p1172492172314"></a><a name="p1172492172314"></a><a href="查询堆栈.md">查询堆栈</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1872411262317"><a name="p1872411262317"></a><a name="p1872411262317"></a>查询指定堆栈的详细信息，包括堆栈名称、堆栈描述、模板id、模板名称、堆栈状态等。</p>
</td>
</tr>
<tr id="row788010215233"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p3880921235"><a name="p3880921235"></a><a name="p3880921235"></a><a href="查询堆栈元素列表.md">查询堆栈元素列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1848720253128"><a name="p1848720253128"></a><a name="p1848720253128"></a>查询堆栈元素列表。</p>
</td>
</tr>
<tr id="row167333142319"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p57312382314"><a name="p57312382314"></a><a name="p57312382314"></a><a href="查询堆栈元素.md">查询堆栈元素</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p189904612235"><a name="p189904612235"></a><a name="p189904612235"></a>查询堆栈某个元素的详细信息。</p>
</td>
</tr>
<tr id="row154421436235"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p54423342316"><a name="p54423342316"></a><a name="p54423342316"></a><a href="查询堆栈输出.md">查询堆栈输出</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p19611142710415"><a name="p19611142710415"></a><a name="p19611142710415"></a>查询指定堆栈输出。</p>
</td>
</tr>
<tr id="row166147312315"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p156141236237"><a name="p156141236237"></a><a name="p156141236237"></a><a href="查询堆栈输入.md">查询堆栈输入</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p201518283299"><a name="p201518283299"></a><a name="p201518283299"></a>查询指定堆栈输入。</p>
</td>
</tr>
<tr id="row11789835230"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p19789833231"><a name="p19789833231"></a><a name="p19789833231"></a><a href="查询堆栈执行记录.md">查询堆栈执行记录</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1768961516235"><a name="p1768961516235"></a><a name="p1768961516235"></a>查询堆栈某一次执行记录。</p>
</td>
</tr>
<tr id="row196218372315"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.3.1.1 "><p id="p2963535239"><a name="p2963535239"></a><a name="p2963535239"></a><a href="查询堆栈执行记录列表.md">查询堆栈执行记录列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.3.1.2 "><p id="p1461002505612"><a name="p1461002505612"></a><a name="p1461002505612"></a>查询堆栈最近的执行记录列表。</p>
</td>
</tr>
</tbody>
</table>


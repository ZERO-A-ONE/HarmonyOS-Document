# 内核子系统<a name="ZH-CN_TOPIC_0000001051340509"></a>

## 简介<a name="section12995104752113"></a>

OpenHarmony内核是华为推出面向IoT领域的实时操作系统内核，它同时具备RTOS轻快和Linux易用的特点。

OpenHarmony内核主要包括进程和线程调度、内存管理、IPC机制、timer管理等内核基本功能。

OpenHarmony内核的源代码分为 [`kernel_liteos_a`](https://gitee.com/openharmony/kernel_liteos_a) 和 [`kernel_liteos_m`](https://gitee.com/openharmony/kernel_liteos_m) 这2个代码仓库，其中`kernel_liteos_a`主要针对Cortex-A系列处理器，而`kernel_liteos_m`则主要针对Cortex-M系列处理器，两者目录结构非常相似，所以下面主要针对`kernel_liteos_a`代码仓库进行介绍。

## 目录<a name="section1121775732114"></a>

**表 1**  OpenHarmony内核源代码目录结构

<a name="table2977131081412"></a>
<table><thead align="left"><tr id="row7977610131417"><th class="cellrowborder" valign="top" width="30.34%" id="mcps1.2.3.1.1"><p id="p18792459121314"><a name="p18792459121314"></a><a name="p18792459121314"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="69.66%" id="mcps1.2.3.1.2"><p id="p77921459191317"><a name="p77921459191317"></a><a name="p77921459191317"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17977171010144"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p2793159171311"><a name="p2793159171311"></a><a name="p2793159171311"></a>apps</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p879375920132"><a name="p879375920132"></a><a name="p879375920132"></a>用户态的init和shell应用程序。</p>
</td>
</tr>
<tr id="row6978161091412"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p37931659101311"><a name="p37931659101311"></a><a name="p37931659101311"></a>arch</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p6793059171318"><a name="p6793059171318"></a><a name="p6793059171318"></a>体系架构的目录，如arm等。</p>
</td>
</tr>
<tr id="row6978201031415"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p117935599130"><a name="p117935599130"></a><a name="p117935599130"></a>bsd</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p0793185971316"><a name="p0793185971316"></a><a name="p0793185971316"></a>freebsd相关的驱动和适配层模块代码引入，例如USB等。</p>
</td>
</tr>
<tr id="row113263612392"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p2133163611390"><a name="p2133163611390"></a><a name="p2133163611390"></a>compat</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p1913313364399"><a name="p1913313364399"></a><a name="p1913313364399"></a>内核posix接口的兼容。</p>
</td>
</tr>
<tr id="row15700172218399"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p10701622113920"><a name="p10701622113920"></a><a name="p10701622113920"></a>fs</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p270110222398"><a name="p270110222398"></a><a name="p270110222398"></a>文件系统模块，主要来源于NuttX开源项目。</p>
</td>
</tr>
<tr id="row1897841071415"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p16793185961315"><a name="p16793185961315"></a><a name="p16793185961315"></a>kernel</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p14793959161317"><a name="p14793959161317"></a><a name="p14793959161317"></a>进程、内存、IPC等模块。</p>
</td>
</tr>
<tr id="row172848480398"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p728414485392"><a name="p728414485392"></a><a name="p728414485392"></a>lib</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p12284154818399"><a name="p12284154818399"></a><a name="p12284154818399"></a>内核的lib库。</p>
</td>
</tr>
<tr id="row5827141194012"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p48272110403"><a name="p48272110403"></a><a name="p48272110403"></a>net</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p28272119406"><a name="p28272119406"></a><a name="p28272119406"></a>网络模块，主要来源于lwip开源项目。</p>
</td>
</tr>
<tr id="row980916239407"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p080910232403"><a name="p080910232403"></a><a name="p080910232403"></a>platform</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p11809202324018"><a name="p11809202324018"></a><a name="p11809202324018"></a>支持不同的芯片平台代码，如Hi3516DV300等。</p>
</td>
</tr>
<tr id="row194244440402"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p0424124412401"><a name="p0424124412401"></a><a name="p0424124412401"></a>security</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p442410448409"><a name="p442410448409"></a><a name="p442410448409"></a>安全特性相关的代码，包括进程权限管理和虚拟id映射管理。</p>
</td>
</tr>
<tr id="row674312515406"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p1274395114012"><a name="p1274395114012"></a><a name="p1274395114012"></a>syscall</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p1374365134011"><a name="p1374365134011"></a><a name="p1374365134011"></a>系统调用。</p>
</td>
</tr>
<tr id="row343553564120"><td class="cellrowborder" valign="top" width="30.34%" headers="mcps1.2.3.1.1 "><p id="p54351735114113"><a name="p54351735114113"></a><a name="p54351735114113"></a>tools</p>
</td>
<td class="cellrowborder" valign="top" width="69.66%" headers="mcps1.2.3.1.2 "><p id="p17435635114116"><a name="p17435635114116"></a><a name="p17435635114116"></a>构建工具及相关配置和代码。</p>
</td>
</tr>
</tbody>
</table>

## 约束<a name="section1967115154223"></a>

Hi3518EV300默认使用jffs2文件系统，Hi3516DV300默认使用vfat文件系统。若要使用其他文件系统，需要新增适配。

## 使用<a name="section1821123352217"></a>

请参考[《内核使用指南》](../kernel/Readme-CN.md)。

## 涉及仓库<a name="section2392425183215"></a>

[drivers_liteos](https://gitee.com/openharmony/drivers_liteos)

[kernel_liteos_a](https://gitee.com/openharmony/kernel_liteos_a)

[kernel_liteos_a_huawei_proprietary_fs_proc](https://gitee.com/openharmony/kernel_liteos_a_huawei_proprietary_fs_proc)

[kernel_liteos_m](https://gitee.com/openharmony/kernel_liteos_m)


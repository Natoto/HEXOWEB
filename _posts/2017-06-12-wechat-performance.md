---
layout: post
title: wechat 事件监听统计列表 PerformanceDataIdKey.dat
tags: wechat
date: 2017-07-20
---

<!--
 描述：此配置用于idkey上报耗时和耗内存数据的idkey映射，主要通过MMPerformanceDataReportMgr采集耗时和耗内存数据，然后根据配置区分设备上报到idkey服务器
 
 注意：该配置如果有修改每次版本发布时需要重新上线一份配置，上线事项可以联系sidwu
 
 字段说明：
 KeysConfig：默认所有要采集耗时和耗内存的上报id必须分设备，按照该节中的配置申请key
 
 key：通过“终端质量监控系统”申请的key信息
 device：设备标示符，如果是all则表示所有设备，具体设备使用具体设备的identify
 totalCostTimeKey：对于耗时数据对应计算总耗时的key，对于耗内存数据对应计算总耗内存的key，该key通过“终端质量监控系统”申请获得
 totalCountKey：功能路径执行的次数，该key通过“终端质量监控系统”申请获得
 des：该key描述信息
 
 CostTimeIDsConfig：耗时数据配置节
 CostMemoryIDsConfig：耗内存数据配置节
 
 case：功能路径，如启动、进入朋友圈等
 caseID：功能路径id，一个功能路径对应一个唯一的id，在PerformanceDef.h文件的eCaseID枚举处定义
 ID：通过“终端质量监控系统”申请的id
 des：case的描述信息
 
 PS：如果你看不懂以上说明，找sdiwu吧，他会手把手教你的
 -->
<KeysConfig>
    <!-- 总体耗时 KEY -->
    <key device="all" totalCostTimeKey="1" totalCountKey="2" des="总体耗时" />
    
    <!-- iPhone4 KEY -->
    <key device="iPhone3,1" totalCostTimeKey="4" totalCountKey="5" des="iPhone4设备" />
    <key device="iPhone3,2" totalCostTimeKey="4" totalCountKey="5" des="iPhone4设备" />
    <key device="iPhone3,3" totalCostTimeKey="4" totalCountKey="5" des="iPhone4设备" />
    
    <!-- iPhone4s KEY -->
    <key device="iPhone4,1" totalCostTimeKey="7" totalCountKey="8" des="iPhone4s设备" />
    
    <!-- iPhone5 KEY -->
    <key device="iPhone5,1" totalCostTimeKey="10" totalCountKey="11" des="iPhone5设备" />
    <key device="iPhone5,2" totalCostTimeKey="10" totalCountKey="11" des="iPhone5设备" />
    
    <!-- iPhone5c KEY -->
    <key device="iPhone5,3" totalCostTimeKey="13" totalCountKey="14" des="iPhone5c设备" />
    <key device="iPhone5,4" totalCostTimeKey="13" totalCountKey="14" des="iPhone5c设备" />
    
    <!-- iPhone5s KEY -->
    <key device="iPhone6,1" totalCostTimeKey="16" totalCountKey="17" des="iPhone5s设备" />
    <key device="iPhone6,2" totalCostTimeKey="16" totalCountKey="17" des="iPhone5s设备" />
    
    <!-- iPhone6 KEY -->
    <key device="iPhone7,2" totalCostTimeKey="19" totalCountKey="20" des="iPhone6设备" />
    
    <!-- iPhone6+ KEY -->
    <key device="iPhone7,1" totalCostTimeKey="22" totalCountKey="23" des="iPhone6+设备" />

    <!-- iPhone6s KEY-->
    <key device="iPhone8,1" totalCostTimeKey="25" totalCountKey="26" des="iPhone6s设备" />

    <!-- iPhone6s+ KEY-->
    <key device="iPhone8,2" totalCostTimeKey="28" totalCountKey="29" des="iPhone6s+设备" />

    <!-- iPhone7 KEY-->
    <key device="iPhone9,1" totalCostTimeKey="31" totalCountKey="32" des="iPhone7设备" />
    <key device="iPhone9,3" totalCostTimeKey="31" totalCountKey="32" des="iPhone7设备" />

    <!-- iPhone7+ KEY-->
    <key device="iPhone9,2" totalCostTimeKey="34" totalCountKey="35" des="iPhone7+设备" />
    <key device="iPhone9,4" totalCostTimeKey="34" totalCountKey="35" des="iPhone7+设备" />

</KeysConfig>

<CostTimeIDsConfig>
    
    <case caseID="1" ID="1" des="启动耗时" />
    <case caseID="2" ID="2" des="进入朋友圈耗时" />
    <case caseID="3" ID="3" des="进入会话耗时" />
    <case caseID="4" ID="4" des="切换通讯录耗时" />
    <case caseID="5" ID="5" des="加载通讯录耗时" />
    <case caseID="6" ID="36" des="主界面读DB耗时" />
    <case caseID="7" ID="55" des="主界面加载耗时" />
    <case caseID="8" ID="56" des="主界面刷新耗时" />
    <case caseID="9" ID="34" des="会话多图文消息节点打开耗时MultiReaderMessageNodeView" />
    <case caseID="10" ID="38" des="服务号通知消息打开耗时HeadImgReaderMessageNodeaView" />
    <case caseID="11" ID="39" des="系统消息打开耗时MessageSysNodeView" />
    <case caseID="12" ID="42" des="会话染色消息打开耗时AttributedReaderMessageNodeaView" />
    <case caseID="13" ID="43" des="会话单图文消息打开耗时ReaderNewMessageNodeView" />
    <case caseID="14" ID="44" des="邮件消息打开耗时MailMessageNodeView" />
    <case caseID="15" ID="45" des="会话图片消息打开耗时ImageMessageNodeView" />
    <case caseID="16" ID="46" des="会话语音消息打开耗时VoiceMessageNodeView" />
    <case caseID="17" ID="47" des="会话小视频消息打开耗时ShortVideoMessageNodeView" />
    <case caseID="18" ID="48" des="会话名片消息打开耗时ShareCardMessageNodeView" />
    <case caseID="19" ID="49" des="会话表情消息打开耗时EmoticonMessageNodeView" />
    <case caseID="20" ID="50" des="会话地理位置消息打开耗时LocationMessageNodeView" />
    <case caseID="21" ID="51" des="会话VOIP消息打开耗时VoipContentNodeView" />
    <case caseID="22" ID="52" des="会话纯文本消息双击打开耗时TextMessageNodeView" />
    <case caseID="23" ID="58" des="会话App链接消息打开耗时AppUrlMessageNodeView" />
    <case caseID="24" ID="59" des="会话消息总绘制耗时" />
    <case caseID="25" ID="60" des="绘制会话多图文消息节点耗时MultiReaderMessageNodeView" />
    <case caseID="26" ID="61" des="绘制服务号通知消息耗时HeadImgReaderMessageNodeaView" />
    <case caseID="27" ID="62" des="绘制系统消息耗时MessageSysNodeView" />
    <case caseID="28" ID="63" des="绘制会话染色消息耗时AttributedReaderMessageNodeaView" />
    <case caseID="29" ID="65" des="绘制会话单图文消息耗时ReaderNewMessageNodeView" />
    <case caseID="30" ID="66" des="绘制邮件消息耗时MailMessageNodeView" />
    <case caseID="31" ID="67" des="绘制会话图片消息耗时ImageMessageNodeView" />
    <case caseID="32" ID="68" des="绘制会话语音消息耗时VoiceMessageNodeView" />
    <case caseID="33" ID="69" des="绘制会话小视频消息耗时ShortVideoMessageNodeView" />
    <case caseID="34" ID="70" des="绘制会话名片消息耗时ShareCardMessageNodeView" />
    <case caseID="35" ID="71" des="绘制会话表情消息耗时EmoticonMessageNodeView" />
    <case caseID="36" ID="72" des="绘制会话地理位置消息耗时LocationMessageNodeView" />
    <case caseID="37" ID="73" des="绘制会话VOIP消息耗时VoipContentNodeView" />
    <case caseID="38" ID="74" des="绘制会话纯文本消息耗时TextMessageNodeView" />
    <case caseID="39" ID="75" des="绘制会话App链接消息耗时AppUrlMessageNodeView" />
    <case caseID="40" ID="76" des="会话加载更多耗时" />
    <case caseID="41" ID="85" des="进入收藏耗时" />
    <case caseID="42" ID="325" des="预排版耗时" />
	<case caseID="43" ID="548" des="init过程耗时" />
</CostTimeIDsConfig>

<CostMemoryIDsConfig>
    
    <case caseID="1" ID="6" des="启动耗内存" />
    <case caseID="2" ID="7" des="进入朋友圈耗内存" />
    <case caseID="3" ID="8" des="进入会话耗内存" />
    <case caseID="4" ID="9" des="切换通讯录耗内存" />
    <case caseID="5" ID="10" des="加载通讯录耗内存" />
    
</CostMemoryIDsConfig>

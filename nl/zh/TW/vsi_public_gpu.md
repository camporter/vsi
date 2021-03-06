---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
{: #gpu}

GPU 設定檔最適用於高效能工作負載，這些工作負載需要更高的運算密度才能減少資源管理及成本。GPU 設定檔完全適合人工智慧處理程序、大量圖形及資料的應用程式，或開發需要快速效能的新應用程式。

{{site.data.keyword.cloud_notm}} Accelerated Compute "ac1" 及 "ac2" 特性採用 NVDIA Tesla GPU 技術，且兩者都提供區塊及本端 SSD 儲存空間。您可以從中選擇下列 GPU 設定檔：  

  <table>
<CAPTION>表 1. P100 GPU 設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>儲存空間類型</th>
<th>開機磁碟 (GB)</th>
<th>次要磁碟（2 及 3）(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>300（本端）</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>600（本端）</td></tr>

</TBODY>
</table>

**附註：**_DAL13_、_LON06_ 及 _WDC07_ 資料中心內提供 P100 GPU 設定檔。

<table>
<CAPTION>表 2. V100 GPU 設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>儲存空間類型</th>
<th>開機磁碟 (GB)</th>
<th>次要磁碟（2 及 3）(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>300（本端）</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>600（本端）</td></tr>

</TBODY>
</table>

**附註：**_DAL10_、_DAL12_、_LON04_ 及 _WDC07_ 資料中心內提供 V100 GPU 設定檔。


## 開始之前
請檢閱下列 GPU 必要條件。

1. 只有支援「硬體虛擬機器 (HVM)」開機模式的作業系統上才提供 GPU 設定檔虛擬伺服器。請參閱下列清單，以取得支援 HVM 開機模式的作業系統。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 必須安裝適當的 NVIDIA 驅動程式及軟體。如需軟體及 NVIDIA 驅動程式的相關資訊，請參閱[安裝 GPU 驅動程式及軟體套件](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages)。  
**附註：**您安裝的軟體可能有必備軟體及作業系統特定配置。

## 新增或移除 GPU
您可以在起始訂購之後變更虛擬伺服器上的 GPU 數目。但是，這取決於您已佈建的 GPU 數目。您會有下列其中一個選項。

- 如果佈建一個 GPU，則您可以新增另一個 GPU，或者
- 如果佈建兩個 GPU，則您可以撤回至一個 GPU

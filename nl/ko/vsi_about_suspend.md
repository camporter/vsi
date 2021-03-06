---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-25"

keywords: virtual server, suspend billing feature, virtual server instances, suspend billing

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# 비용 청구 일시중단 정보
{: #requirements}

비용 청구 일시중단 기능을 지원하는 가상 서버의 전원을 끄면 특정 컴퓨팅 리소스에 대해 비용이 발생하지 않습니다. 비용 청구는 서버의 전원이 꺼지면 자동으로 중지됩니다. 비용 청구 일시중단 기능은 비용을 절감하고 리소스가 다시 필요할 때 가상 서버를 다시 프로비저닝할 필요가 없게 해 줍니다.
{:shortdesc}

2018년 11월 1일 이전에 작성된 대부분의 가상 서버 인스턴스는 비용 청구 일시중단 기능을 지원하지 않습니다. 가상 서버 인스턴스가 비용 청구 일시중단 기능을 지원하는지 여부를 알아보려면 [비용 청구 일시중단 기능 보기](/docs/vsi?topic=virtual-servers-viewing-suspend-billing-feature)를 참조하십시오.

이 기능은 전 세계의 데이터 센터에서 사용할 수 있습니다. 비용 청구 일시중단 기능을 지원하는 가상 서버 인스턴스를 프로비저닝하려면 가상 서버 인스턴스가 다음 설정으로 구성되어야 합니다.

* 시간별 SAN
* 다음 제품군 중 하나의 공용 프로파일:
  * 밸런스됨
  * 컴퓨팅
  * 메모리

비용 청구 일시중단 기능은 가상 서버 인스턴스를 프로비저닝하고 재확보할 수 있는 더 빠른 대안으로 사용할 수 있습니다.
{:tip}

비용 청구는 {{site.data.keyword.slportal_full}}, CLI 또는 {{site.data.keyword.slapi_short}}를 통해 가상 서버 인스턴스의 전원을 끈 경우에만 일시중단됩니다. OS를 통해 직접 가상 서버 인스턴스의 전원을 끄는 경우에는 해당 인스턴스에 대한 비용 청구가 일시중단되지 않습니다.
{:note}

## 프로비저닝 세부사항

{{site.data.keyword.cloud_notm}} 카탈로그(cloud.ibm.com), CLI 또는 {{site.data.keyword.slapi_short}}를 통해 비용 청구 일시중단 기능을 지원하는 가상 서버 인스턴스를 프로비저닝할 수 있습니다. {{site.data.keyword.slportal}}(control.softlayer.com)을 통해 비용 청구 일시중단 기능을 지원하는 가상 서버 인스턴스를 프로비저닝할 수 없습니다. 공용 가상 서버 인스턴스 프로비저닝에 대한 자세한 정보는 [공용 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)을 참조하십시오.

{{site.data.keyword.cloud_notm}} 카탈로그의 경우, 가상 서버를 주문하려면 업그레이드된 계정이 있어야 합니다. 계정 업그레이드에 대한 자세한 정보는 [IBM ID로 전환](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)을 참조하십시오.
{:note}

### Softlayer API를 통해 프로비저닝
{{site.data.keyword.slapi_short}}를 통해 비용 청구 일시중단 기능을 지원하는 가상 서버 인스턴스를 프로비저닝할 수 있습니다. API 예는 [주문 발주 오브젝트를 사용한 공용 인스턴스 프로비저닝](/docs/vsi?topic=virtual-servers-api-rest-public#provisioning-a-public-instance-using-place-order-object)을 참조하십시오.

프로비저닝 프로세스 중에 특정 비용 청구 일시중단 패키지 ID를 지정해야 합니다. {{site.data.keyword.slapi_short}}에서 키 이름 `SUSPEND_CLOUD_SERVER`를 사용하여 비용 청구 일시중단 패키지 ID를 조회할 수 있습니다. 서버 패키지 검색에 대한 예는 [{{site.data.keyword.slapi_short}} 주문 CLI를 사용한 주문 이해 및 빌드 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://softlayer.github.io/article/understanding-ordering/){: new_window}를 참조하십시오.

## 비용 청구 세부사항

가상 서버 인스턴스의 전원을 껐을 때 어떤 비용은 더 이상 발생하지 않고 어떤 비용은 계속 발생하는지 이해해야 합니다.

| 리소스                      | 비용 청구 중지   | 비용 청구 지속 |
| ----------------------------- | ----------------- | ---------------- |
| vCPU                          |          X        |                  |
| RAM                           |          X        |                  |
| 포트 속도                    |          X        |                  |
| 운영 체제 라이센스     |          X        |                  |
| 모니터링 추가 기능             |          X        |                  |
| 보조 공인 IP 주소 |                   |          X        |
| 스토리지                       |                   |          X        |
{: caption="표 1. 리소스 비용 청구 세부사항" caption-side="top"}   

비용 청구 일시중단 기능을 지원하는 가상 서버 인스턴스를 프로비저닝하는 경우 가상 서버 인스턴스의 사용 시간 및 일시중단 시간은 모두 분 단위로 계산됩니다. 인스턴스의 전원을 꺼서 비용 청구 일시중단 기능을 시작한 적이 없는 경우에도, 비용 청구는 인스턴스 라이프사이클의 분 단위로 계산됩니다.
{:note}

### 최소 사용 요금
비용 청구 일시중단 기능을 지원하는 가상 서버 인스턴스에는 일부 경우에 적용되는 최소 사용 요금이 있을 수 있습니다. 사용량이 25%보다 많은 경우에는 해당 사용량에 대해 비용이 청구됩니다. 사용량이 25%보다 적은 경우에는 현재 비용 청구 주기에서 인스턴스가 존재한 시간의 25%에 대해 비용이 청구됩니다.

### 비용 청구서
가상 서버에서 비용 청구를 일시중단하면 비용 청구서에서 몇 가지가 변경됩니다. 관련 요금이 이제 사용량 기반 세부사항으로 표시됩니다. 예를 들면 사용 가능 시간, 사용 시간 및 총 청구 시간을 반영하는 다음 추가 항목이 표시될 수 있습니다.

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## 리소스 세부사항

### 스토리지

가상 서버 인스턴스에서 비용 청구를 일시중단하는 경우 연관된 스토리지에 대한 비용 청구는 지속되지만, 가상 서버 인스턴스의 전원이 꺼져 있는 동안에는 저장된 데이터에 액세스할 수 없습니다. 인스턴스에 대한 비용 청구를 재개하고 나면 데이터에 다시 액세스할 수 있습니다.

### IP 주소

가상 서버 인스턴스에 대한 비용 청구가 일시중단되는 경우에도 모든 공인 IP 주소는 유지됩니다.

### 제한사항

일시중단된 가상 서버 인스턴스는 계정 전체의 디바이스 할당량에 계속 반영됩니다. 인스턴스 한계에 대한 자세한 정보는 [FAQ: 가상 서버](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent)를 참조하십시오.

## 다음 단계
비용 청구 일시중단을 지원하는 가상 서버를 프로비저닝한 후에는 디바이스에서 비용 청구를 일시중단하고 재개할 수 있습니다.

가상 서버 인스턴스에서 비용 청구가 일시중단되면 디바이스에 대한 비용 청구를 재개할 때까지 인스턴스에서 모든 동일한 조치를 완료할 수 없습니다. 사용자는 {{site.data.keyword.slapi_short}}를 통해, 또는 {{site.data.keyword.slportal}}에서 디바이스 세부사항 페이지에 액세스하여 디바이스의 중지 여부와 상태가 변경된 시점의 관련 날짜를 볼 수 있습니다.

가상 서버 인스턴스에서 비용 청구를 일시중단하려면 가상 서버의 전원을 끄십시오. 자세한 정보는 [가상 서버 관리](/docs/vsi?topic=virtual-servers-managing-virtual-servers)를 참조하십시오.

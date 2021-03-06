---

copyright:
  years: 2018
lastupdated: "2018-10-31"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 배치 그룹
{: #placement-groups}

{{site.data.keyword.BluVirtServers}}의 배치 그룹을 통해 공용 인스턴스를 사용하여 데이터 센터 내에서 고가용성을 빌드하거나 대규모 배치에서 추가적인 레벨의 내결함성을 제공할 수 있습니다.
{:shortdesc}

배치 그룹을 작성한 다음 최대 5개의 새 가상 서버 인스턴스를 지정하십시오. 분산 규칙을 사용하면 각 가상 서버가 다른 실제 호스트에서 프로비저닝됩니다.

시작하려면 다음 단계를 수행하십시오.

1. 브라우저에서 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){:new_window}을 열고 사용자 계정에 로그인하십시오.
2. 배치 그룹 페이지에서 **배치 그룹 추가**를 클릭하십시오.
3. 배치 그룹의 이름, 설명 및 데이터 센터를 입력하고 **추가**를 클릭하십시오.
4. **주문** 섹션을 찾고 **디바이스**를 클릭하십시오.
5. 디바이스 페이지에서 Virtual Server 오퍼링 중 하나에 대해 **시간별** 또는 **월별**을 클릭하십시오.
6. 기타 필요한 정보를 완료하고 **주문에 추가**를 클릭하십시오. 체크아웃 페이지가 열립니다.
7. 기존 배치 그룹을 선택할 수 있습니다. **분산**은 인스턴스가 다른 실제 하드웨어에 있음을 의미합니다.
8. 마지막으로 **주문 제출**을 클릭하십시오.

##제한사항
기존 인스턴스는 배치 그룹에 추가할 수 없습니다. 프로비저닝할 때 가상 서버 인스턴스만 배치 그룹에 추가할 수 있습니다.

배치 그룹에서 인스턴스를 제거하려면 인스턴스를 삭제하거나 재확보해야 합니다.

## 다음 단계

새 배치 그룹을 작성하고 관리하려면 [배치 그룹 관리](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup)를 참조하십시오.

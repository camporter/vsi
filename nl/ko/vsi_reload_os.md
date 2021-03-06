---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

#  OS 다시 로드
언제든지 디바이스의 운영 체제(OS)를 다시 로드하여 디바이스를 원래 작동 상태로 복원하거나, 디바이스를 다른 소프트웨어로 다시 구성할 수 있습니다. OS 다시 로드는 디바이스에서 모든 데이터를 제거하며 OS 다시 로드 설정의 구성 프로세스 중에 지정된 바와 같이 "새 것과 같은" 구성을 적용합니다. OS 다시 로드는 디바이스에서 모든 데이터를 지우므로 다시 로드 전에 데이터가 백업되지 않은 경우 데이터가 영구적으로 삭제되어 복원할 수 없게 됩니다.
{:shortdesc}

**중요:** 데이터를 보존하려는 경우에는 다시 로드를 수행하기 전에 모든 데이터를 백업하십시오.

## 다시 로드 수행
1. **디바이스 목록**에서 OS 다시 로드가 필요한 서버를 클릭하십시오.
2. 페이지 왼쪽 상단에 있는 **조치** 메뉴에서 **OS 다시 로드**를 선택하십시오.
3. 기존 구성을 다시 로드할지, 또는 새 구성을 사용하여 디바이스를 다시 로드할지 결정하십시오.

   <table>
   <CAPTION>표 1. OS 다시 로드 옵션</CAPTION>
   <THEAD>
   <TR>
   <th>다시 로드 유형</th>
   <th>단계</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>새 구성을 사용하여 다시 로드하려는 경우</td>
   <td>
   <ol>
   <li>업데이트가 필요한 카테고리에 대해 <b>편집</b>을 클릭하십시오.</li>
   <li><i>소프트웨어 선택</i> 드롭 다운 목록에서 디바이스에 적용할 새 소프트웨어를 선택하십시오.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>기존 구성을 사용하여 다시 로드하려는 경우</td>
   <td>다음 단계로 진행하십시오.</td>
   </tr>
   </TBODY>
   </table>

4. 디바이스가 프로비저닝된 다음 설치 후 스크립트를 적용해야 하는지 결정하십시오.

   설치 후 스크립트를 적용하려는 경우에는 기존 스크립트 드롭 다운 목록에서 스크립트를 선택하거나 새 스크립트의 완전한 URL을 입력하십시오.  그렇지 않은 경우에는 다음 단계로 진행하십시오.

5. 실제 디바이스의 경우에는 설치된 파티션을 추가할지, 제거할지 또는 변경하지 않을지 결정하십시오.
   
   <table>
   <CAPTION>표 2. 파티션 조치 옵션</CAPTION>
   <THEAD>
   <TR>
   <th>파티션 조치</th>
   <th>단계</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>설치된 파티션을 추가하려는 경우</td>
   <td>
   <ul>
   <li><b>다른 파티션 추가</b> 링크를 클릭하십시오.</li>
   <li>파티션의 정확한 이름을 입력하십시오.</li>
   <li>파티션 크기(GB)를 입력하십시오. 원하는 경우에는 늘리기를 선택해 나머지 디스크 공간을 채우도록 파티션 크기를 늘릴 수 있습니다.
   <p><b>참고:</b> 한 번에 하나의 파티션에 대해서만 늘리기를 선택할 수 있습니다. 이 파티션은 지정된 크기보다 크며 사용 가능한 모든 용량을 채웁니다. 늘리기 파티션의 용량은 설치된 파티션 섹션에 제공된 총 용량에서 다른 모든 파티션의 합산된 크기를 빼 계산됩니다.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>설치된 파티션을 제거하려는 경우</td>
   <td>파티션을 삭제하려면 <b>삭제</b> 아이콘을 클릭하십시오.</td>
   </tr>
   <tr>
   <td>변경하지 않으려는 경우</td>
   <td>다음 단계로 진행하십시오.</td>
   </tr>
   </TBODY>
   </table>
    
6. 디바이스에 하나 이상의 SSH 키를 적용할지 결정하십시오.

7. OS 다시 로드 중 또는 다시 로드 후 적용할 옵션의 해당 선택란을 선택하십시오.

   **참고:** 옵션은 디바이스에 따라 다릅니다. 모든 디바이스에서 모든 옵션을 사용할 수 있는 것은 아닙니다.

8. **위 구성을 다시 로드** 단추를 클릭하여 검토 팝업으로 진행하십시오. 디바이스에 대한 변경사항을 취소하고 화면을 종료하려면 **취소** 단추를 클릭하십시오.

9. 새 구성 섹션의 모든 세부사항이 올바른지 확인하십시오.  

10. **OS 다시 로드 확인** 단추를 클릭하여 OS 다시 로드를 확인하고 시작하십시오. 조치를 취소하려면 **취소** 단추를 클릭하십시오.

## 다음 단계
OS 다시 로드 프로세스를 시작하면 디바이스가 오프라인 상태가 되며 OS 다시 로드 프로세스가 진행되기 시작합니다.
OS 다시 로드에 소요되는 시간은 디바이스의 현재 구성 및 새 구성에 따라 달라집니다.
구성 프로세스 중에, OS 다시 로드의 최소 소요 시간이 각 화면에 표시됩니다.
표시되는 시간 범위는 시스템의 예상 시간이며 참고용으로 제공된 것입니다. 다시 로드에 24시간 이상이 소요되는 경우에는
지원 팀에 문의하십시오. 디바이스는 온라인 상태가 되면 OS 다시 로드의 새 구성에 지정되어 있는 바와 같이 작동합니다. 이전에 디바이스에 저장되었던 모든 데이터는 유실되지만 다시 로드 전에 디바이스의 백업이 작성된 경우에는 이를 복원할 수 있습니다.
데이터가 백업되지 않은 경우에는 이를 복원할 수 없습니다.
 
EVault에 디바이스를 다시 등록하려는 경우에는 [EVault에 디바이스 다시 등록 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}을 참조하십시오.

# V7: 코드 품질 및 빌드 설정 요구사항

## 통제 목표

이 통제의 목표는 앱을 개발할 때 기본적인 보안 코딩 방법을 준수하고, 컴파일러에서 제공하는 "무료" 보안 기능이 활성화되도록 하는 것입니다.

## 보안 검증 요구사항

| # | MSTG-ID | 설명 | L1 | L2 |
| --- | --- | --- | --- | --- |
| **7.1** | MSTG‑CODE‑1 | 앱이 유효한 인증서로 서명 및 프로비저닝되어야 하며, 개인 키가 올바르게 보호되어야 한다. | ✓ | ✓ |
| **7.2** | MSTG‑CODE‑2 | 앱은 릴리 모드로 빌드되어 있어야 한다. (디버그 불가) | ✓ | ✓ |
| **7.3** | MSTG‑CODE‑3 | 네이티브 바이너리에서 디버그 기호가 제거되어야 한다. | ✓ | ✓ |
| **7.4** | MSTG‑CODE‑4 | 디버깅 코드 및 개발자 지원 코드(예 : 테스트 코드, 백도어, 숨겨진 설정)가 제거되어야 한다. 앱은 자세한(verbose) 오류나 디버깅 메시지를 기록하지 않아야 한다. | ✓ | ✓|
| **7.5** | MSTG‑CODE‑5 | 앱에서 사용되는 라이브러리 및 프레임워크 등은 모든 타사 구성 요소를 식별하고 알려진 취약점이 있는지 확인하여야 한다. | ✓ | ✓ |
| **7.6** | MSTG‑CODE‑6 | 앱은 가능한 모든 예외를 포착하고 처리하여야 한다. | ✓ | ✓ |
| **7.7** | MSTG‑CODE‑7 | 보안 통제의 오류 처리 로직은 기본적으로 액세스를 거부하여야 한다. | ✓ | ✓ |
| **7.8** | MSTG‑CODE‑8 | 관리되지 않는 코드에서 메모리는 할당, 해제 및 안전하게 사용되어야 한다. | ✓ | ✓ |
| **7.9** | MSTG‑CODE‑9 | 바이트 코드의 경량화, 스택 보호, PIE 지원 및 자동 참조 카운팅과 같은 툴체인에서 제공하는 무료 보안 기능이 활성화되어야 한다. | ✓ | ✓ |

## 참고

OWASP 모바일 보안 테스트 안내서(MSTG)는 이 섹션에 나열된 요구사항을 확인하기 위한 자세한 지침을 제공합니다.

- Android: 코드 품질 및 빌드 설정 테스트 - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05i-Testing-Code-Quality-and-Build-Settings.md>
- iOS: 코드 품질 및 빌드 설정 테스트 - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06i-Testing-Code-Quality-and-Build-Settings.md>

자세한 내용은 다음을 참조하십시오:

- OWASP Mobile Top 10: M7 (Poor Code Quality) - <https://www.owasp.org/index.php/Mobile_Top_10_2016-M7-Poor_Code_Quality>
- CWE 119 (Improper Restriction of Operations within the Bounds of a Memory Buffer) - <https://cwe.mitre.org/data/definitions/119.html>
- CWE 89 (Improper Neutralization of Special Elements used in an SQL Command) - <https://cwe.mitre.org/data/definitions/89.html>
- CWE 388 (7PK - Errors) - <https://cwe.mitre.org/data/definitions/388.html>
- CWE 489 (Leftover Debug Code) - <https://cwe.mitre.org/data/definitions/489.html>

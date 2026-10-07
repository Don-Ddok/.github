<div align="center">

# 돈독 · Don-Ddok

**수출 경기 충격은 법인의 은행 거래에 어떻게 나타나는가**

iM DiGital Banker Academy 9기 · 통계 프로젝트

지방은행 데이터로 "지역 수출이 나빠지면 기업의 은행 거래가 어떻게 달라지는가"를 통계로 확인합니다.

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![statsmodels](https://img.shields.io/badge/statsmodels-4051B5?style=flat-square)
![Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)

![기간](https://img.shields.io/badge/기간-2026.09.21~10.07-555555?style=flat-square)
![소속](https://img.shields.io/badge/iM%20DiGital%20Banker%20Academy-9기-00A0B0?style=flat-square)

</div>

---

## 무엇을 하는 팀인가

은행은 기업이 어려워졌다는 사실을 **연체가 생긴 뒤에야** 확실히 알게 됩니다. 그때는 이미 늦습니다.

그보다 앞선 신호를 찾을 수 있을까. 기업의 주문과 매출은 은행 데이터에 없지만, **수출 통계는 은행 밖에 있습니다.** 밖에서 가져와 붙여 보자는 것이 이 프로젝트의 출발점입니다.

```
수주 감소 → 매출 감소 → 자금 압박 → 대출 연장·증액 → 연체 → 부실
                                                    └── 은행이 아는 시점
   └── 외부 수출 통계로 볼 수 있는 구간
```

## 핵심 질문

| | 질문 |
|---|---|
| **시차** | 수출이 나빠진 뒤 은행 거래에 변화가 나타나기까지 몇 달이 걸리는가 |
| **차등** | 수출을 하는 법인이 하지 않는 법인보다 더 크게 반응하는가 |
| **방향** | 반응은 자금 압박으로 나타나는가, 생산 축소로 나타나는가 |
| **업종** | 어떤 업종이 가장 민감한가 |

## 이렇게 접근합니다

**1. 수출 여부는 짐작하지 않고 기록으로 확인합니다**
업종 이름으로 "수출할 것 같은 회사"를 고르지 않습니다. 실제로 외환 거래 실적이 찍힌 법인만 수출 노출로 봅니다.

**2. 같은 지역 안에서 비교합니다**
대구·경북 내부에서 노출 법인과 비노출 법인을 비교합니다. 지방은행 특성상 수도권 고객은 자기선택된 특수 집단이라 비교 대상에서 제외했습니다.

**3. 변수 정의부터 검증합니다**
주어진 지표가 실제로 의미하는 바를 먼저 확인하고, 성립하지 않으면 지표를 바꿉니다. **그 과정도 결과물에 남깁니다.**

**4. 같은 법인의 반복 관측을 보정합니다**
한 회사를 36개월 따라가므로, 법인 단위 고정효과와 군집 표준오차로 착시를 줄입니다.

**5. 외부 자료도 원자료와 대조한 뒤 씁니다**
출처가 적혀 있어도 값은 따로 확인합니다. 수출입·환율처럼 밖에서 가져온 자료는 발표 기관의 원자료와 한 칸씩 맞춰 본 뒤 분석에 넣습니다.

**6. 분석 기준은 결과를 보기 전에 정합니다**
주 분석과 판정 기준을 먼저 문서로 고정하고, 결과를 본 뒤 방법을 바꾸지 않습니다. 여러 방법으로 확인한 결과는 좋은 것만 고르지 않고 전부 보고합니다.

**7. 결과가 약해도 결론으로 씁니다**
효과가 없다는 것도 발견입니다. 관련성까지만 말하고 인과는 주장하지 않습니다.

## 사용 데이터

| 구분 | 내용 |
|---|---|
| 내부 자료 | iM뱅크 제공 교육용 법인 익명데이터 — 저장소에 공개하지 않습니다 |
| 외부 자료 | 대구·경북 월별 수출입(관세청 통계, 한국무역협회 K-stat) · KOSIS 업종별 광공업생산지수 · 한국은행 ECOS 원/달러 환율·기준금리 · 월별 영업일수(공휴일 반영) · 대구·경북 기업경기실사지수(BSI) |

## 팀

<div align="center">

<table>
<tr>
<td align="center" width="140">
<a href="https://github.com/dahye292"><img src="https://github.com/dahye292.png?size=120" width="90" style="border-radius:50%"><br><b>dahye292</b></a><br>신다혜 · 팀장
</td>
<td align="center" width="140">
<a href="https://github.com/wjsdbghks2-eng"><img src="https://github.com/wjsdbghks2-eng.png?size=120" width="90" style="border-radius:50%"><br><b>wjsdbghks2-eng</b></a><br>전유환 · 팀원
</td>
<td align="center" width="140">
<a href="https://github.com/Moomooti"><img src="https://github.com/Moomooti.png?size=120" width="90" style="border-radius:50%"><br><b>Moomooti</b></a><br>허민영 · 팀원
</td>
<td align="center" width="140">
<a href="https://github.com/JANGJAEYEOL"><img src="https://github.com/JANGJAEYEOL.png?size=120" width="90" style="border-radius:50%"><br><b>JANGJAEYEOL</b></a><br>장재열 · 팀원
</td>
<td align="center" width="140">
<a href="https://github.com/FAITRUEE"><img src="https://github.com/FAITRUEE.png?size=120" width="90" style="border-radius:50%"><br><b>FAITRUEE</b></a><br>이성진 · 팀원
</td>
</tr>
</table>

</div>

## 저장소

| 저장소 | 내용 |
|---|---|
| [Don-Ddok_Docs](https://github.com/Don-Ddok/Don-Ddok_Docs) | 기획서, 일일 진행 일지, 역할 분담, 데이터 명세서, 최종 결과 보고서와 발표자료, 파트별 분석 결과와 그림 |
| [Don-Ddok_Data](https://github.com/Don-Ddok/Don-Ddok_Data) | 전처리·분석 코드, 집계 결과표, 원자료와 대조한 공개 외부 데이터 (은행 원본 데이터 제외) |
| [Don-Ddok_Dashboard](https://github.com/Don-Ddok/Don-Ddok_Dashboard) | 법인 고객 마케팅 월보 프로토타입 — [donddok.vercel.app](https://donddok.vercel.app) |

## 진행 상황

| 단계 | 상태 |
|---|---|
| 주제 확정·기획 | 완료 |
| 분석용 데이터 구축·검증 | 완료 |
| 파트별 분석(요구불·매칭 모델, 수신 채널, 여신·업종) | 완료 — 공통 사양으로 네 계정 재추정, 강건성·사전추세 점검까지 |
| 실무 활용 화면(법인 고객 마케팅 월보) | 공개 — 이번 달 추천, 팀 인사이트, 여신 분석, 용어 사전 |
| 결과 보고서·발표 | 완료 — 최종 보고서와 발표자료 제출(10/6) |

## 먼저 볼 곳

| 보고 싶은 것 | 위치 |
|---|---|
| 결과를 화면으로 | [donddok.vercel.app](https://donddok.vercel.app) — 수출 둔화 단계별로 먼저 제안할 고객과 상품, 그 근거와 한계 |
| 여신·업종 분석 한눈에 | [파트 3 그림 모음](https://github.com/Don-Ddok/Don-Ddok_Docs/blob/main/분석결과/파트3_여신업종분석/그림/README.md) — 분석마다 방법·결과·문제점을 한 장씩 |
| 계정별 반응을 같은 잣대로 | [파트 1 요구불·매칭 모델](https://github.com/Don-Ddok/Don-Ddok_Docs/tree/main/분석결과/파트1_요구불매칭분석) — 네 계정 공통 사양 재추정과 상품 매칭 모델 |
| 팀 결과 보고서 | [최종본(10/6)](https://github.com/Don-Ddok/Don-Ddok_Docs/tree/main/결과보고서) |
| 발표자료 | [최종 발표자료(10/6, 33쪽)](https://github.com/Don-Ddok/Don-Ddok_Docs/blob/main/발표자료/돈독_최종_발표자료_20261006.pdf) |

화면과 문서의 숫자는 모두 집계 결과입니다. 약하거나 기각된 결과도 그대로 적었습니다.

---

<div align="center">
<sub>
원본 데이터는 은행 제공 자료라 이 조직의 어떤 저장소에도 올리지 않습니다.<br>
이 프로젝트는 교육 과정의 결과물이며 iM뱅크의 공식 입장이 아닙니다.
</sub>
</div>

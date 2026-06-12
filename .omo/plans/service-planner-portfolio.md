# 7년차 인하우스 서비스 기획자 포트폴리오 구성 계획

## TL;DR
> Summary:      첫 회사의 호스팅 커머스 외부 연동·운영 안정성 경험과 PG사의 정산·결제 운영·UX 관점 확장을 연결해, 7년차 인하우스 서비스 기획자/PM·PO 후보로 보이게 만드는 포트폴리오 작성 계획이다.
> Deliverables:
> - 3~5분 안에 직무·레벨·대표 경험이 보이는 포트폴리오 구조
> - 대표 프로젝트 2~3개 작성 템플릿
> - 재입사 서사 정리 문장
> - JD별로 순서를 바꿀 수 있는 모듈형 구성
> - 2주 작성 로드맵과 검수 체크리스트
> Effort:       Medium
> Risk:         Medium - 실제 프로젝트별 수치와 산출물 보유 여부가 아직 확인되지 않았다.

## Scope
### Must have
- 포지셔닝: `호스팅 커머스의 외부 연동·운영 안정성 경험을 바탕으로, PG사에서 정산과 결제 운영 관점을 확장한 인하우스 서비스 기획자`
- 대표 경험 후보: 네이버페이 연동, 카카오싱크 연동, ISMS 대응, PG 정산 업무, 관리자/운영 UX 또는 운영 프로세스 개선
- 커리어 서사: 첫 회사의 커머스/연동 경험 → PG사의 정산/UX 관점 확장 → 넓어진 관점으로 첫 회사 재입사
- 전자책 원칙 반영: 3~5분 스캔, 직무/레벨 명확화, 기여도 의심 제거, PARL 구조, 숫자 없는 성과의 구체화
- 방어 가능한 표현: 실제 담당 범위, 팀 구조, 결정권, 조율 대상, 내가 없었으면 생겼을 리스크

### Must NOT have
- 주문·결제·정산 전체 흐름을 처음부터 깊게 담당한 것처럼 쓰지 않는다.
- 데이터 기반 지표 개선이나 AI 자동화를 대표 프로젝트로 올리지 않는다.
- `전략 수립`, `로드맵 리딩`, `총괄` 같은 표현을 실제 결정권 없이 사용하지 않는다.
- 재입사를 `담당자 퇴사`, `사람이 없어서`, `지인이 불러서`로 설명하지 않는다.
- 이전 회사의 조직 문제를 불만처럼 서술하지 않는다.

## Verification strategy
> Zero human intervention - all verification is agent-executed where possible, but project 사실관계와 수치 보강은 사용자 확인이 필요하다.
- Test decision: none - 문서/기획 산출물 작성 계획이며 코드 변경이 아니다.
- QA policy: 각 todo는 산출물 존재 여부와 체크리스트 충족 여부로 검수한다.
- Evidence: `.omo/drafts/service-planner-portfolio-brief.md`, `.omo/plans/service-planner-portfolio.md`
- Metis gap review: spawned but inconclusive - reviewer did not return a deliverable after repeated waits and was closed. Local gap review was applied by adding open facts, artifact paths, scope guardrails, and final verification checks.

## Execution strategy
### Parallel execution waves
> Target 5-8 todos per wave.
Wave 1 (no deps): 1, 2, 3, 4
Wave 2 (after 1): 5, 6, 7, 8
Wave 3 (after 2): 9, 10, 11, 12
Final wave: F1, F2, F3, F4
Critical path: 1 → 4 → 5 → 8 → 9 → 12

### Dependency matrix
| Todo | Depends on | Blocks | Can parallelize with |
| --- | --- | --- | --- |
| 1 | none | 4, 5 | 2, 3 |
| 2 | none | 5, 6 | 1, 3, 4 |
| 3 | none | 7, 8 | 1, 2 |
| 4 | 1 | 5, 9 | 2, 3 |
| 5 | 1, 2, 4 | 8, 9 | 6, 7 |
| 6 | 2 | 8, 10 | 5, 7 |
| 7 | 3 | 8, 11 | 5, 6 |
| 8 | 5, 6, 7 | 9, 10, 11 | none |
| 9 | 8 | 12 | 10, 11 |
| 10 | 8 | 12 | 9, 11 |
| 11 | 8 | 12 | 9, 10 |
| 12 | 9, 10, 11 | final | none |

## Todos
- [ ] 1. 확정 포지셔닝 문장 작성
  What to do / Must NOT do: 첫 페이지에 들어갈 한 줄 브랜딩과 3줄 요약을 작성한다. `주문·결제 전체 전문가`처럼 과장하지 않는다.
  Parallelization: Can parallel Y | Wave 1 | Blocks 4, 5
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 한 줄 브랜딩 1개, 3줄 요약 1개, 핵심 키워드 3개가 작성된다.
  QA scenarios: 문서 스캔 QA - 60초 안에 목표 직무, 레벨, 대표 경험이 식별되는지 체크한다. Evidence `.omo/evidence/task-1-positioning.md`
  Commit: N | docs(portfolio): define positioning | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 2. 커리어 전환 서사 정리
  What to do / Must NOT do: 첫 회사, PG사, 재입사의 흐름을 성장 루프로 작성한다. 전 회사 비판이나 내부 담당자 부재 표현은 쓰지 않는다.
  Parallelization: Can parallel Y | Wave 1 | Blocks 5, 6
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 긴 버전 1개, 면접 답변용 짧은 버전 1개, 이력서/포트폴리오용 2문장 버전 1개가 작성된다.
  QA scenarios: 리스크 표현 QA - `사람이 없어서`, `업무를 못 받아서`, `대표/팀장 때문에` 같은 표현이 없는지 확인한다. Evidence `.omo/evidence/task-2-career-story.md`
  Commit: N | docs(portfolio): write career narrative | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 3. 대표 프로젝트 후보 확정 인터뷰
  What to do / Must NOT do: 네이버페이, 카카오싱크, ISMS, PG 정산, 관리자/운영 UX 후보별 실제 역할과 산출물을 확인한다. 기억이 불명확한 경험은 대표 프로젝트에서 제외한다.
  Parallelization: Can parallel Y | Wave 1 | Blocks 7, 8
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 각 후보마다 담당 범위, 팀 구조, 산출물, 기간, 이해관계자, 결과 근거가 채워진다.
  QA scenarios: 대표성 QA - 각 후보가 `내가 직접 설명 가능한 경험`인지 O/X로 분류한다. Evidence `.omo/evidence/task-3-project-inventory.md`
  Commit: N | docs(portfolio): inventory projects | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 4. 5분 스캔형 목차 설계
  What to do / Must NOT do: 포트폴리오를 표지, 요약, 대표 프로젝트, 보조 활동, 산출물 링크 순서로 설계한다. 연대기식 나열을 피한다.
  Parallelization: Can parallel Y | Wave 1 | Blocks 5, 9
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 표지 포함 8~12개 섹션의 목차가 작성되고, 각 섹션의 목적이 1문장으로 정의된다.
  QA scenarios: 5분 스캔 QA - 목차만 보고 직무/레벨/대표 프로젝트 2개가 보이는지 확인한다. Evidence `.omo/evidence/task-4-outline.md`
  Commit: N | docs(portfolio): design scan-first outline | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 5. 네이버페이/카카오싱크 프로젝트 템플릿 작성
  What to do / Must NOT do: 외부 서비스/API 연동 경험을 `Problem → Approach → Result → My Role → Lesson`로 작성한다. 결제 도메인 전체를 깊게 담당한 것처럼 쓰지 않는다.
  Parallelization: Can parallel Y | Wave 2 | Blocks 8, 9
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 네이버페이와 카카오싱크 각각에 대해 프로젝트 초안 템플릿이 만들어진다.
  QA scenarios: 기여도 QA - 각 프로젝트에 내가 맡은 요구사항 정리, 협의, 정책/화면/운영 기준 중 최소 2개가 명시된다. Evidence `.omo/evidence/task-5-integration-projects.md`
  Commit: N | docs(portfolio): draft integration cases | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 6. ISMS 대응 프로젝트 템플릿 작성
  What to do / Must NOT do: ISMS를 단순 인증 참여가 아니라 정책, 보안 기준, 운영 안정성 측면에서 정리한다. 보안 전문가처럼 과장하지 않는다.
  Parallelization: Can parallel Y | Wave 2 | Blocks 8, 10
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: ISMS 대응의 배경, 담당 범위, 협업 부서, 산출물, 리스크 감소 관점이 정리된다.
  QA scenarios: 보안 과대포장 QA - `보안 전략 총괄` 같은 표현 없이 서비스 기획자의 역할로 설명되는지 확인한다. Evidence `.omo/evidence/task-6-isms-case.md`
  Commit: N | docs(portfolio): draft isms case | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 7. PG 정산 프로젝트 템플릿 작성
  What to do / Must NOT do: PG사에서 배운 정산 업무를 돈의 흐름, 운영 리스크, 관리자 UX 관점으로 정리한다. 첫 회사 경험과 뒤섞어 과거부터 전문성이 있었던 것처럼 쓰지 않는다.
  Parallelization: Can parallel Y | Wave 2 | Blocks 8, 11
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 정산 업무의 범위, 배운 구조, 자주 본 이슈, 기획 관점으로 전환된 인사이트가 작성된다.
  QA scenarios: 도메인 확장 QA - `PG사에서 새롭게 확장한 관점`이 명확히 구분되는지 확인한다. Evidence `.omo/evidence/task-7-pg-settlement.md`
  Commit: N | docs(portfolio): draft settlement case | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 8. 대표 프로젝트 2~3개 선정
  What to do / Must NOT do: 작성 가능한 근거가 가장 강한 프로젝트 2~3개만 대표로 고른다. 약한 경험을 억지로 대표에 넣지 않는다.
  Parallelization: Can parallel N | Wave 2 | Blocks 9, 10, 11
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 대표 프로젝트 2~3개와 보조 프로젝트가 분리되고, 제외 사유가 기록된다.
  QA scenarios: 방어 가능성 QA - 각 대표 프로젝트에 대해 면접 질문 5개를 뽑고 답변 가능한지 체크한다. Evidence `.omo/evidence/task-8-project-selection.md`
  Commit: N | docs(portfolio): select representative cases | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 9. 대표 프로젝트별 헤드라인 구체화
  What to do / Must NOT do: 제목만 보고 문제와 역할이 보이게 만든다. 성과 숫자가 없으면 무리하게 숫자를 만들지 않는다.
  Parallelization: Can parallel Y | Wave 3 | Blocks 12
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 각 대표 프로젝트에 나쁜 제목 1개와 개선 제목 2개가 작성된다.
  QA scenarios: 헤드라인 QA - 제목만 보고 프로젝트 문제, 대상, 역할 중 2개 이상이 보이는지 확인한다. Evidence `.omo/evidence/task-9-headlines.md`
  Commit: N | docs(portfolio): refine project headlines | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 10. 숫자 없는 성과 보강 방식 정리
  What to do / Must NOT do: 수치 성과가 부족한 프로젝트를 규모, 빈도, 기간, 대상 수, 처리 건수, 리스크 감소로 설명한다. 가짜 Before/After를 만들지 않는다.
  Parallelization: Can parallel Y | Wave 3 | Blocks 12
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 각 대표 프로젝트마다 사용할 수 있는 정량 보조 표현 후보가 3개 이상 작성된다.
  QA scenarios: 숫자 신뢰도 QA - 면접에서 근거를 물었을 때 설명 가능한 숫자만 남긴다. Evidence `.omo/evidence/task-10-impact-proxies.md`
  Commit: N | docs(portfolio): define impact proxies | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 11. JD별 모듈형 버전 설계
  What to do / Must NOT do: 지원 직무에 따라 프로젝트 순서를 바꿀 수 있게 버전을 만든다. 모든 회사에 같은 순서로 제출하지 않는다.
  Parallelization: Can parallel Y | Wave 3 | Blocks 12
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: PM/PO형, 커머스 연동/운영 플랫폼형, PG/정산 도메인형의 3개 배열안이 작성된다.
  QA scenarios: JD 매칭 QA - 각 버전마다 첫 대표 프로젝트가 해당 JD의 핵심 문제와 연결되는지 확인한다. Evidence `.omo/evidence/task-11-jd-modules.md`
  Commit: N | docs(portfolio): design jd modules | Files `.omo/plans/service-planner-portfolio.md`

- [ ] 12. 최종 작성 로드맵과 검수표 작성
  What to do / Must NOT do: 2주 안에 포트폴리오 초안을 완성하는 일정과 검수 체크리스트를 만든다. 완벽주의로 시작을 미루지 않게 한다.
  Parallelization: Can parallel N | Wave 3 | Blocks final
  References: `.omo/drafts/service-planner-portfolio-brief.md`
  Acceptance criteria: 10영업일 작성 일정, 일자별 산출물, 최종 검수 체크리스트가 작성된다.
  QA scenarios: 실행 가능성 QA - 하루 60~90분 기준으로 과제가 끝날 수 있는지 점검한다. Evidence `.omo/evidence/task-12-roadmap.md`
  Commit: N | docs(portfolio): write execution roadmap | Files `.omo/plans/service-planner-portfolio.md`

## Final verification wave
> Runs in parallel where possible. ALL must pass before declaring the portfolio plan ready.
- [ ] F1. Plan compliance audit
  Verify: 모든 todo가 대표 경험, 수용 기준, QA 시나리오, 과대포장 방지 조건을 갖췄는지 확인한다.
- [ ] F2. Scope fidelity
  Verify: 데이터/AI, 주문·결제 전체 흐름을 대표 역량처럼 올리지 않았는지 확인한다.
- [ ] F3. Interview risk review
  Verify: 재입사, 조직 개편, 내부 지인, 담당자 부재 표현이 안전한지 확인한다.
- [ ] F4. 5분 scan review
  Verify: 첫 2페이지에서 직무, 레벨, 대표 프로젝트 2개가 보이도록 구성됐는지 확인한다.

## Commit strategy
- 커밋은 사용자가 명시적으로 요청할 때만 진행한다.
- 계획서만 커밋한다면 `docs(portfolio): plan service planner portfolio`를 사용한다.
- 포트폴리오 본문 작성이 이어지면 초안, 케이스, 최종 검수 단위로 나누어 커밋한다.

## Success criteria
- 포트폴리오가 3~5분 안에 `어떤 직무/레벨의 후보인지` 보여준다.
- 대표 프로젝트가 2~3개로 좁혀지고, 각 프로젝트가 PARL + My Role 구조로 설명된다.
- 재입사 서사가 후퇴가 아니라 외부 경험 후 도메인/UX 관점을 확장해 돌아온 선택으로 보인다.
- 약한 데이터/AI 경험을 대표 프로젝트로 과장하지 않는다.
- 수치 성과가 부족한 경우에도 규모·빈도·기간·대상 수·운영 리스크 감소로 경험의 무게를 설명한다.
- JD에 따라 대표 프로젝트 순서를 바꿀 수 있는 모듈형 구성이 된다.

## Recommended portfolio artifact
- Working draft: `portfolio/service-planner-portfolio-draft.md`
- Project inventory: `portfolio/project-inventory.md`
- Final Notion/PDF outline: `portfolio/final-outline.md`
- Interview script: `portfolio/interview-script.md`

## Open facts to collect from user
- 네이버페이 연동에서 직접 맡은 범위: 요구사항 정의, 정책 정리, 화면 설계, 제휴/개발 협의, QA, 운영 적용 중 무엇이었는가
- 카카오싱크 연동에서 직접 맡은 범위와 가입/동의/회원정보 처리 관련 쟁점은 무엇이었는가
- ISMS 대응에서 담당한 산출물: 정책서, 화면/기능 수정, 권한/로그/개인정보 처리 기준, 증적 대응 중 무엇이었는가
- PG사 정산 업무에서 반복적으로 다룬 이슈: 정산 주기, 수수료, 보류/차감, 취소/환불, 대사, 관리자 처리 중 무엇이었는가
- 관리자/운영 UX 개선 사례가 있다면 실제 개선 전후의 불편, 조율 대상, 결과는 무엇이었는가

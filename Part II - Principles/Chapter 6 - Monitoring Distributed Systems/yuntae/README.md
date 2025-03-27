# Chapter 6 - Monitoring Distributed Systems

## Terms of Monitoring

- White-box monitoring
- Black-box monitoring
  - Client side에서는 상대적으로 모니터링이 어렵기 때문에 Black-box로 표현한 듯.
- Dashboards
- Alerts
  - **_Tickets, Email Alerts, Pages_**
- Root cause
- Node and machine
- Push

## Why?

- Trends
- A/B testing
- Alerting
- Dashboards
- Debugging

=> 모니터링 시스템을 구축하되, 시스템을 구축함으로써 사람의 개입을 줄이려고 하는 의도를 항상 명심해 둘 것.

## Reasonable Expectations for Monitoring

- 사후 분석을 위해서 사용해야지, 모니터링 시스템에 각 시스템과의 커플링을 만드는 것은 지양하라는 것을 말하려는 듯.
- 구글의 데이터 엔지니어링 서비스가 독립적으로 구성된 것을 보면 이해가 됨.
- 최대한 모니터링의 본질을 잊지말고 기본적인 부분부터 탄탄하게 하라는 것을 설명하려는 것으로 보임.

## Golden Signals

상황에 맞게 아래 지표들의 공식을 적당히 변형시켜 사용해야하는 듯.

### Latency

Request~Response 사이의 시간. 하나의 단위.

### Traffic

시스템에 얼마나 많은 수요가 발생하는 지.
대개 초당 Request 수로 표현.

### Errors

시스템에서 발생하는 에러의 비율.

### Saturation

서비스 리소스 사용률.
=> 얼마나 빠르게 해당 지표를 가져와 처리하는 지가 시스템 자동화의 관건이라고 생각.

## Principles

단순히 Ticket, Alert, Page를 생성하는 것이 아니라. 구체적으로 누구에게 전달할 것인지, 얼마나 중요한 것인지, 어떻게 대응해야 함을 알려줄지 등을 모두 고려해서 시스템을 설계해야 함.
=> 불필요한 알림으로 인한 노이즈를 줄이고, 가급적 정말 사람의 손을 타야하는 경우에 대해서만

## Summary

- 모니터링 시스템을 구축할 때, "단순히 지표의 값을 출력하여 모니터링 한다"가 아닌 "주로 무슨 문제 때문에 어떤 지표가 필요하다 + 구축한 시스템이 생산적으로 대응하고 지속적으로 성장하여 사람의 개입을 최소화 할 수 있는가"를 고민해야할 듯. (사람은 정말 새로운 문제에만 개입하도록)

## Question

- CSP 사의 Serverless없이 문제를 처리할 프로그램을 만들 때 어떻게 하는게 효율적일까
  - Cron 이외의 조건에 대해 Trigger를 어떻게 받을 것이며, 어떻게 소규모/최적화 할 수 있을까?
  - 단순히 service daemon?

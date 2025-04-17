# Chapter 9 - Simplicity

복잡한 시스템은 필연적으로 실패한다. 그리고 SRE는 실패를 관리하는 역할을 맡는다.
따라서 단순함은 ‘있으면 좋은 철학’이 아니라, 신뢰성을 위한 실질적인 전략.

> [!NOTE]
> 잘 동작하는 job scheduler를 가지고 너무 다양한 케이스를 처리하려다 보니, 결국은 “예외 핸들러를 위한 예외 핸들러”까지 만들어버림.
> 문제가 생겼을 때는 디버깅에 너무 오랜 시간을 투자해야하는 상황이 발생됨

## The Virtue of Boring

화려한 기술보다 지루한 기술이 신뢰성을 만든다.

> [!NOTE]
> k8s에 아무 고려없이 Istio를 붙였다가 장애가 나서 root cause가 3단계 이상 깊어지고 결국 sidecar 없이 plain kube로 돌아왔다는 썰을 들어봤음.

## Minimal APIs & Modularity

단순한 인터페이스는 그 자체로 품질 보장.  
이를 재사용할 수 있는 모듈로 만들면, 단순한 인터페이스를 가진 모듈을 조합해서 복잡한 시스템을 만들 수 있음.

> [!NOTE]
> 추상화의 기본 원칙과 유사한 듯.
> 단순히 만들기 위해서 더 많은 공수를 들이는 경우도 허다해서, 차라리 프로토타입으로 만들어두고 천천히 쪼개거나 개선해서 단순화 시키는게 나은 것 같기도.

## Release Simplicity

"If we release 100 unrelated changes to a system at the same time and performance gets worse, understanding which changes impacted performance, and how they did so, will take considerable effort or additional instrumentation"

> [!NOTE]
> 상황마다 다를 것 같은데, GitHub Actions에서 reusable workflow나 composite action 단위로 잘개 쪼갤수록 디버깅이 빨라지고 유지보수가 편해지는 것을 생각해보면 될 듯.
> 이런 것 때문에 [Grafana CI OTel Collector](https://github.com/grafana/grafana-ci-otel-collector)라는 것이 있더라.
> => GitHub Actions의 Step, Job을 Trace 컨셉으로 치환해서 보다 효과적인 워크플로우 디버깅이 가능.

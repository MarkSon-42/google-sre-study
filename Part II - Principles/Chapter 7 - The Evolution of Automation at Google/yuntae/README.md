# Chapter 7 - The Evolution of Automation at Google

## Automation in Google

Google은 단순한 자동화가 아니래 최대한 시스템의 자생력을 키우는 것에 집중하는 느낌.

- 항상 동일한 상태를 유지하도록
- 확장이 가능하도록 만들어, 플랫폼 형태로 만들어 질 수 있도록
- product의 lifecycle 상 문제를 빨리 발견할 수 있도록
- 사람의 개입을 최소화 하도록
- 시간 절감의 이익을 누릴 수 있도록

=> 하지만 처음부터 자동화를 고려할 수는 없을 것 같고, 어느정도 이런 문화/습관이 잡혀있는 조직에서 가능할 것 같음

## Use cases

- Puppet, Chef, etc...
  - "자동화를 위한 컴포넌트의 추상화 수준이 서로 다르다" => Github Actions vs Ansible을 생각해보면 될듯
- 단순히 바이너리 기준 재 배포
  - 원자성이 보장된 작업이라고 가정하지만 다양한 문제 발생의 경우의 수가 존재
  - 사람의 개입을 최소화하는 자동화 추구 => state를 확인하는 것과 같은?

## A Hierarchy of Automation Classes

1. No automation
2. Externally maintained system-specific automation
3. Externally maintained generic automation
4. Internally maintained system-specific automation
5. Systems that don’t need any automation

=> 이런 과정을 거치지 않고 함축하면 추후 더 공수가 드는 듯.
=> 아니면 최소한 자동화를 여러 독립적인 컴포넌트로 나누고 우선 작동하게 만든 뒤에, 각 컴포넌트를 개선하는 방식으로 진행하는 것도 좋은 듯. (위 방식은 시간이 너무 소요되므로)

## DB in Borg.

DB의 신뢰성이 매우 높아진 상태에서 Google이 MySQL DB를 Borg로 마이그레이션한 것에 관함

- Master에 대해서 failover를 수행하는데 당시 너무 오랜 시간이 걸림
  => Decider를 통해서 Master를 자동으로 failover 시키는 시스템을 만들어 해결 (K8s Operator?)

> [!NOTE] DB in K8s?
>
> Storage Issue
>
> - Statefulset
> - PV
> - Replication
> - Performance of Storage
>
> FailOver & DR Issue
>
> - Recovery Time
> - Manual Intervention
> - Master Election
>
> ...

## Cluster Turnup

### How to build a cluster

1. Fit out a datacenter building for power and cooling
2. Install and configure core switches and connections to the backbone.
3. Install a few initial racks of servers.
4. Configure basic services such as DNS and installers, then configure a lock service, storage, and computing.
5. Deploy the remaining racks of machines.
6. Assign user-facing services resources, so their teams can set up the services.

turning up a service in a new cluster gives new hires exposure to a service’s internals, this task seemed like a natural and useful training tool.
=> 상당히 좋은 방법인 것 같음. HomeLab을 통해서도 비슷한 경험을 할 수 있을 듯.

> [!NOTE] My HomeLab Turnup Idea for Machine(Node) Layer
>
> Proxmox 등과 같이 VM Solution 없이 Bare Metal 머신에 그대로 세팅.
>
> - 서버용으로 사용할 머신에 PiHole을 Container로 세팅하고 DNS+DHCP로 사용. dnsmasq로 PXE 기능 확장 (TFTP 포함됨)
> - Bare Metal 머신에 PXE Booting을 통해서 OS 설치
> - Bare Metal 머신에서 부팅 커널 로드 시 cloud-init 데이터를 받아오도록 설정. 자동으로 네트워크, 호스트 네임, 스토리지 설정

### Prodtest

- 테스트 중 하나라도 실패하면 전체가 실패하게 하거나 픽스를 수행하도록 설정
  - => 자동화 workflow에 대한 사용자의 의존성을 줄이지 않남 (더 꼼꼼하게 만들도록 유도?)

## Topic

- "많은 시스템 엔지니어들이 자신들의 경력의 출발점으로 삼는, 대학교의 컴퓨팅 시스템"
- 자동화 엔지니어링 구성 방법

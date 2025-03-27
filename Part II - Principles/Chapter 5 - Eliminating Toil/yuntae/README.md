# Chapter 5 - Eliminating Toil

## Toil

- Toil(삽질)은 단순히 하기싫은 일이 아니라 반복적이고 overhead를 만드는 일 등을 추상적으로 의미하는 것.
- Manual, Repetitive, Automatable, Tactical, No enduring value, Scale with service

=> 삽질의 정의 자체가 추상적이지만 대충 반복적이고 가치가 떨어지는 일들을 먼저 인식하라는 의미인듯  
=> 삽질을 줄이거나 적당선으로 유지하여 더 생산적인 일(개발)에 투자하라

## Calculating Toil

Google에서는 on-call을 위해 primary, secondary 인원을 두고 대응.  
최소 2명의 인원이 투입되므로 이를 업무량에 포함하여 얼마나 Toil을 처리할 것인지 계산  
=> 실시간 서비스(넓게 봐서 B2C)의 경우, 확실히 최소 3~4명의 인원이 필요하지 않을까.

## SRE activities

- Software Engineering
  - Automation scripts, modify IaC, create tool/framework
  - 여기서 SRE의 Software Engineering을 명확히 정의하는 듯
- Systems Engineering
  - config / tunning 과같이 한번만 수행하는 것들을 위주로만 잡았는데, 반복적이거나 Manual한 작업을 줄이라는 의미에서 더 명시하지 않은 것 아닐까
- Toil
  - 서비스와 관련된 삽질
- Overhead
  - 서비스와 관련되지 않은 삽질

=> 저자가 설명하듯 50%를 꾸준히 개발에 투자하는 것은 현실적이지 않으나, 적어도 이런 것들을 머리에 두고 개선할 부분을 찾으라는 듯.

## Summary

- 반복적이고 가치가 떨어지는 일들을 항상 경계하고, 이를 줄이기 위한 노력을 기울이자.
- 개인적으론 자동화를 위해 항상 험난한 삽질이 필수불가결이라고 생각하고, 모두 자동화할 수 없으니 가치 산정을 잘하는 것이 중요하다고 생각.

## Question

- 각자의 삽질 예시
- 각자 삽질을 줄이기 위해 노력한 엔지니어링 흔적

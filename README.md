# 클러스터 구성

Kubernetes 클러스터의 선언적 구성을 위한 GitOps 저장소입니다.

## 개요

이 저장소는 GitOps 원칙에 따라 Kubernetes 클러스터의 원하는 상태를 정의하는 manifest 파일들을 보관합니다.

## 저장소 구조

- **argocd/**: ArgoCD가 관리하는 Application 리소스 정의
- **clusters/**: 클러스터에서 사용하는 manifest (네임스페이스, 컨피그맵 등)
- **bootstrap.yaml**: ArgoCD Application을 참조하는 최상위 Application 

## 사용 방법

- 차트버전이 7.8.20인 ArgoCD가 클러스터에 설치되어 있어야 합니다.
- /bootstrap.yaml에 정의된 Application을 ArgoCD가 관리하도록 등록해야합니다.
- 하위 Application은 자동으로 관리 대상으로 추가됩니다.

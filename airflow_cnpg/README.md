# 빌드 및 실행 방법
k kustomize ./kustomize/airflow_cnpg/base/ --enable-helm > result.yaml
k apply -f result.yaml

# kustomization에서 Namespace 생성을 하면 안되는 이유
kustomization을 통해 네임스페이스를 생성할 수 있다.
하지만 kustomization으로 빌드된 yaml을 통해 리소스를 삭제하면,
만들어진 네임스페이스도 같이 삭제된다.

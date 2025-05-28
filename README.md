## 개요
Github Action을 통한 CI/CD 기본 flow
Local 파일 변경사항이 Github actions를 통해 EC2에 반영
## 절차
1.Local 에서 docker 파일 구성 
2.EC2 public ip 서브넷 생성(private subnet + NAT 조합 > 편의상 public)
보안그룹설정 : 22,8080 port open
3..github/workflows/deploy.yml 작성 -> Maven build,Copy jar,Docker-compose
4.이후 파일 수정 후 git add . commit push 절차진행 >> 사이트 적용

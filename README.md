### 해당 레포는 A팀의 개발 프로젝트 아카이브 용 레포지토리 입니다.
| 전체 프로젝트 설명은 [DDWU ACC 블로그](https://ddwu-aws-cloud-club.github.io/post/post-15-final-proj-a/) 에서 확인하실 수 있습니다.
   
기존 레포지토리는 [https://github.com/ACC-TEAM-A/concert-service](https://github.com/ACC-TEAM-A/concert-service) 에서 확인하실 수 있습니다.

## 1️⃣ 프로젝트 아키텍처

---

- 외부 사용자 또는 클라이언트는 API Gateway를 통해 서비스에 액세스합니다.
- 각 서비스는 독립적으로 배포되며, EC2 인스턴스에서 실행됩니다.
- 서비스 별 데이터는 각 RDS 인스턴스에 저장되며, 프라이빗 서브넷에 배치됩니다.
- API Gateway를 통해 서비스 간 통신이 이루어지며, Gateway는 각 서비스의 IP 및 포트에 대한 정보를 갖고 있습니다.
- JWT 토큰을 사용하여 인증 및 권한을 부여하고, 서브넷 및 보안 그룹으로 네트워크 보안을 강화했습니다.
- 유레카 서버는 서비스의 등록 및 검색을 관리하며, 서비스 Discovery를 지원합니다.
<img width="1007" alt="Untitled (1)" src="https://github.com/ddwu-aws-cloud-club/team-a/assets/80163835/0d7d489c-1eb5-48e3-a3a6-e2fbfe5f4591">



## 2️⃣ 프로젝트 설명

---

<table style="width: 100%;">
<tr style="border: none;">
<td style="width: 50%; vertical-align: top; border: none;">

**MSA 아키텍처**를 사용 : 서비스를 마이크로 단위로 분리 

- User Service : 유저 관련 서비스 담당
- Concert Service : 콘서트 관련 서비스 담당
- Reserve Service : 선착순 예약 서비스 담당
- Eureka Service : 디스커버리 관련 서비스 담당
- Gateway Service : 라우팅 관련 서비스 담당

</td>
<td style="width: 50%; vertical-align: top; border: none;">

<img width="252" alt="스크린샷 2024-04-14 오후 12 16 53" src="https://github.com/ddwu-aws-cloud-club/team-a/assets/80163835/e36101ae-db3b-4712-9b04-271f956c0f33">

</td>
</tr>
</table>



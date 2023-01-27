- Docker Hub란 무엇인가
    
    컨테이너 이미지들을 담는 Hub임.
    
    ref. 도커 공식문서
    
- Spring Cloud Config Server란?
    
    서버 어플리케이션이 직접 치명적인 권한 정보를 들고 있다면 보안 취약점이 발생하게 되므로 이를 해결하기 위해 사용. 
    
    그 외에도 사용하고자 하는 시스템의 환경 설정 값이 자주 바뀌는 경우에 바뀔때마다 다시 빌드, 배포를 진행해야 하는데 이러한 번거로움을 줄이기 위해서 사용함.
    
    → 따라서 보안이나 서버의 운영 측면에서 봤을 때 서버의 환경 설정 정보는 중앙에서 관리를 하고 각 서버 어플리케이션이 이를 이용하는 것이 좋음. 즉, Spring Cloud Config Server란 분산된 환경의 서버에서 환경 설정 정보를 중앙에서 모아 관리를 하는데 도움을 주는 라이브러리
    
- nginx란 무엇인가?
    
    serves as a reverse proxy server for HTTP, HTTPS, SMTP, IMAP, POP3 protocols, on the other hand, it is also used for HTTP load balancer, HTTP cache, and email proxy for IMAP, POP3, and SMTP.
    
    - reverse proxy란?
        
        사설 네트워크의 방화벽 뒤에 존재하며 client requests를 backend server로 보내주는 역할. 이를 통해 추가적인 추상화 계층으로 동작을 하며 client와 server간의 네트워크 트래픽을 매끄럽게 진행시킬 수 있음.
        
    - reverse proxy가 하는 구체적인 기능은?
        - 로드밸런싱
            
            어떠한 서버도 overloaded 되지 않았다는 것을 보장하며 속도와 용량 최적화를 진행. 만약 서버가 다운되면 로드 밸런서는 여분의 온라인 서버로 트래픽 redirect.
            
        - 웹 가속화
            
            캐시를 통해 공통적으로 요청되는 content에 대해 인바운드와 아웃 바운드 데이터 압축을 진행해 client와 server간의 트래픽 속도를 증가시킬 수 있음. 또한 웹 서버에서 부담을 줄일 수 있는 SSL 암호화 등의 부가적인 작업도 진행 가능.
            
        - 보안과 익명성
            
            백엔드 서버의 앞에서 요청을 먼저 처리하며 요청을 식별하고 사이버 공격에 추가적으로 대응할 수 있음. 또한 로컬 네트워크의 구조에 관계없이 단일 레코드 로케이터나 URL에서 다수의 서버에 접근 가능하다는 것을 보장함.
            
        
        ref. [https://www.nginx.com/resources/glossary/reverse-proxy-server/](https://www.nginx.com/resources/glossary/reverse-proxy-server/)
        
    
    ref. [https://www.javatpoint.com/nginx-introduction](https://www.javatpoint.com/nginx-introduction)
    

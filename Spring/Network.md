   ```java
  public void translate(final RequestDTO dto) throws Exception{
          // JSON 형식으로 외부 API와 통신
          ObjectMapper obj = new ObjectMapper();
          RestTemplate restTemplate = new RestTemplate();

          HttpHeaders httpHeaders = new HttpHeaders();
          httpHeaders.setContentType(new MediaType("application", "json")); // {"before" : "", "lang" : ""} 형식으로 요청 전송함

          String body = obj.writeValueAsString(dto);

          HttpEntity httpEntity = new HttpEntity(body, httpHeaders);

          // 응답은 {}
          ResponseEntity<String> responseEntity = restTemplate.exchange(url, HttpMethod.POST, httpEntity, String.class);
      }
  }
  ```
- ObjectMapper
    
    객체를 JSON으로 바꾸기 위해 사용함
    
- RestTemplate
    
    스프링에서 REST 방식 Api 호출을 위해 제공하는 내장 클래스
    
    - WebClient
        
        전통적인 `synchronous`API와 효율적인 `nonblocking asynchronous`한 API 모두 제공함.

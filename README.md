@Controller
client에서 HTTP요청을 보내서 JSON형식 name:value,name:value으로 입력하고 데이터를 서버에 전송한다 spring MVC의 @controller에서 요청을 처리 하는데 MessageConverter를 사옹ㅎ 여기서 JSON 데이터를 QueryString으로 변환하고 이때, JSON의 각 name:value 쌍을 queryString의 key=value 형식으로 변환한다. 그후에 @ModelAttribute를 사용하여 메소드의 파라미터로 자바 객체에 바인딩한다. 이때 queryString의 key는 자바객체의 필드와 매칭되어 자동으로 설정된다. 이 과정에서 lib 이용됨
@RestController
@RestController는 name:value형식으로 JSON 형식의 데이터를 HTTP 요청의 본문에 포함하여 서버로 전송하는 Stringfy를 이용하여 String형식으로 만들어준다. 서버에서 수신 후 요청 본문에서 JSON데이터를 Java객체로 변환 해주고 java객체로 매핑해준다. 이를 이용하여 컨트롤러의 핸들러메소드는 요청을 처리하여 응답(HTTPresponse)을 생성하여 다시 json데이터형식으로 바꿔서 전달한다. Client가 수신후 이 HTTPresponse를 처리한다. 즉, 클라이언트가 서버로부터 응답을 수신한다는 것은 클라이언트가 서버로부터 받은 HTTP 응답의 본문을 처리하는 것을 의미합니다. 이를 통해 클라이언트는 서버로부터 받은 데이터를 화면에 표시하거나 다음 요청에 사용할 수 있다.


[옵셔널(Optional)] : 프로그램의 안정성을 높이기 위해 사용하는 개념 </br>
- 'nil'을 사용할 수 있는 타입과 사용할 수 없는 타입을 구분하고 사용할 수 있는 타입을 '옵셔널 타입'이라고 부름
- nil : '값이 없음'을 의미

Optional() - nil인 경우 : 처리과정에서 문제가 생긴 값. 옵셔널 타입으로 정의할 수 없는 값.
           - nil이 아닌 경우 : 옵셔널 타입으로 정의할 수 있는 값.

           ex) Int("123") -> Optional(123) : 오류가 발생할 가능성이 있기만 하면, 성공적으로 처리해도 옵셔널 타입으로 반환.
               Int("안녕하세요") -> nil : 오류가 발생할 가능성이 있고, 실제로도 정상적인 변환이 불가능해서 nil값 반환.

*옵셔널 타입 : 반환하고자 하는 값을 옵셔널 객체로 다시 한 번 감싼 형태.

[옵셔널 타입 선언] : 자료형 뒤에 '?' 추가.

var optInt : Int? // 옵셔널 Int 타입 </br>
var optStr : String? // 옵셔널 String 타입 </br>
var optDouble : Double? // 옵셔널 Double 타입 </br>
var optArr : [String]? // 옵셔널 Array 타입 </br>
var optDic : [String:String]? // 옵셔널 딕셔너리 타입 </br>
var optObj : AnyObject? // 옵셔널 Class 타입 </br>

[옵셔널 강제 해제]
//옵셔널 타입은 연산 불가능
Int("123") + Int("123") 
//옵셔널 타입 + 일반 자료형 연산 불가능
Int("123") + 30 

옵셔널 해제 : '!' 사용

var optInt: Int? = 3
print("옵셔널 자체의 값 : \(optInt)") // 옵셔널 자체의 값 : Optionall(3)
print("옵셔널 자체의 값 : \(optInt!)") // 옵셔널 자체의 값 : 3

Int("123")! + Int("123")! // 246
Int("123")! + 30 // 156

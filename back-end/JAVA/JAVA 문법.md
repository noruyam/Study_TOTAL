# 문법

---

> ## Stack   
> 후입선출(LIFO, Last In First Out)
> ```java
> .push(Object item) // Stack에 객체를 저장한다.
> .pop() //  Stack의 맨 위에 저장된 객체를 꺼낸다.
> .peek() // Stack의 맨 위에 저장된 객체를 반환한다. Stack에서 꺼내지는 않고, 비었을 때 null을 반환한다.
> .empty() // Stack이 비어있는지 알려준다. 있으면 true, 없으면 false를 반환한다. 
> .search(Object o) // Stack에서 주어진 객체를 찾아서 그 위치를 반환한다. (배열과는 달리 1부터 시작)
> ```
> 
> ## Queue   
> 선입선출(FIFO, First In First Out)
> ```java
> .add(Object o) // Queue에 객체를 저장. 성공하면 true, 실패하면 false를 반환한다.
> .element() // 삭제없이 저장된 요소를 읽어온다. peek와 다른 점은 queue가 비었을 때 Exception을 발생. (peek()는 null을 반환) 
> .offer(Object o) // Queue에 객체를 저장한다. 성공하면 true, 실패하면 false를 반환.
> .peek() // 삭제없이 읽어온다. Queue가 비었을 때 null을 반환.
> .poll() // Queue에서 꺼내온다. 비어있으면 null을 반환.
> .remove() // Queue에서 꺼내온다. 비어있으면 예외를 발생시킨다.
> ```

---

> ## String 관련 메소드
> ```java
> .length() // str의 길이 반환
> .isEmpty() // str의 길이가 0이면 true, 아니면 false
> .charAt(2) // 인덱스로 문자 찾기, c 반환
> .indexOf("c") // 문자로 첫번째 인덱스 찾기, 2 반환
> .lastIndexOf("c") // 문자의 마지막 인덱스 찾기, 2 반환
> .substring(2, 4) // 2~3 위치의 문자열 "cd" 반환
> .substring(3) // 3부터 끝까지의 문자열 "de" 반환
> .replace('b', 'k') // b를 k로 변경 (akcde)
> .replaceAll(String regex, String replacement) // replace()와 비슷하나, 첫번째 인자로 정규식을 넣는다. 
> .replaceFirst(String target, String replacement) // 첫번째 발견되는 target만 치환한다.
> .equals("abcde") // str과 abcde를 비교해서 같으면 true, 다르면 false
> .contains("bc") // str에 bc가 포함되어 있으면 true, 아니면 false
> .split(" ") // 띄어쓰기로 구분된 문자열 str을 분리해서 String[] 배열 반환
> .split() // 띄어쓰기 없는 문자열 str을 한 문자씩 분리해서 String[] 배열 반환
> .trim() // str의 앞뒤 공백 제거, 문자열 사이 공백은 제거 X
> .toLowerCase() // 대문자를 모두 소문자로 변경
> .toUpperCase() // 소문자를 모두 대문자로 변경
> .compareTo("abcdd")
> /*
> str과 abcdd가 같으면 0
> str이 abcdd보다 사전순으로 앞이면 -1
> str이 abcdd보다 사전순으로 뒤면 1
> str과 abcdd가 마지막 문자만 다르면 마지막 문자의 사전순 차이 반환 (여기선 1)
> */
> ```

---

> ## StringBuilder, StringBuffer   
> StringBuilder sb = new StringBuilder(): 객체 선언   
> StringBuilder sb = new StringBuilder("aaa"): 문자열을 바로 넣을 수도 있다.
> 주요 메소드
> ```java
> .append() // 문자열을 추가한다. (sb.append("bbb"), sb.append(4))
> .insert(int offset, String str)// offset 위치에 str을 추가한다. (sb.insert(2, "ccc"))
> .replace(): 첫번째와 두번째 파라미터로 받는 숫자 인덱스에 위치한 문자열을 대체한다. (.replace(3, 6, "ye"))
> .substring(int start, (int end))// 인덱싱. 파라미터가 하나라면 해당 인덱스부터 끝까지, 두개라면 시작점과 끝점-1 까지 인덱싱 (sb.substring(5), sb.substring(3, 7))
> .deleteCharAt(int index)// 인덱스에 위치한 문자 하나를 삭제한다. (sb.deleteCharAt(3)) 
> .delete(int start, int end)// start 부터 end-1 까지의 문자를 삭제한다. (sb.delete(3, sb.length()))
> .toString()// String으로 변환한다. (sb.toString())
> .reverse()// 해당 문자 전체를 뒤집는다. (sb.reverse())
> .setCharAt(int index, String s)// index 위치의 문자를 s로 변경
> .setLength(int len)// 문자열 길이 조정, 현재 문자열보다 길게 조정하면 공백으로 채워짐, 현재 문자열보다 짧게 조정하면 나머지 문자는 삭제
> .trimToSize()// 문자열이 저장된 char[] 배열 사이즈를 현재 문자열 길이와 동일하게 조정, String 클래스의 trim()이 앞 뒤 공백을 제거하는 것과 같이 공백 사이즈를 제공하는 것, 배열의 남는 사이즈는 공백이므로, 문자열 뒷부분의 공백을 모두 제거해준다고 보면 됨
> ```

---

> ## Integer 관련 메소드
> ```java
> .parseInt(String s) // String 타입의 문자열을 int 형으로 변환
> .toString(int i) // int 타입의 문자열을 String 형으로 변환
> .toBinaryString(int i) // 10진수를 2진수로 변환해 String으로 리턴
> .toOctalString(int i) // 10진수를 8진수로 변환해 String으로 리턴
> .toHexString(int i) // 10진수를 16진수로 변환해 String으로 리턴
> .bitCount(int i) // 매개변수로 들어온 정수를 2진법으로 표현했을 때 bit 1이 몇 개있는지 리턴
> .max(int a, int b) // 입력 받은 2개 정수 중 더 큰 값을 리턴
> .min(int a, int b) // 입력 받은 2개 정수 중 더 작은 값을 리턴
> ```

---

> ## List 관련 메소드
> ```java
> List<String> list = new ArrayList<>();
> .add("서울") // list의 가장 뒤에 서울 삽입
> .add(1, "대전") // 1 위치에 대전 삽입
> .addAll(list2) // list의 뒤에 list2의 모든 값 삽입
> .get(0) // 0 위치의 값 반환 (서울)
> .set(0, "대구") // 0 위치의 값을 대구로 변경
> .indexOf("대구") // 대구의 첫번째 인덱스 반환
> .lastIndexOf("대구") // 대구의 마지막 인덱스 반환
> .remove(0) // 0 위치의 값 삭제
> .remove("대구") // 첫번째 대구 삭제
> .removeAll(list2) // list에서 list2에 들어있는 모든 값을 삭제
> .retainAll(list2) // list에서 list2에 들어있는 값을 제외한 모든 값을 삭제
> .clear() // 전체 값 삭제
> .isEmpty() // 길이가 0이면 true, 아니면 false
> .size() // 길이
> .contains("서울") // 서울이 list에 있으면 true, 없으면 false
> .containsAll(list2) // list에 list2의 모든 값이 포함되어 있으면 true
> .removeIf(k -> k % 2 != 0) // 람다식으로 홀수를 list에서 모두 제거
> ```

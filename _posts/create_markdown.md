---
layout: single
title: "Markdown 사용법과 mermaid Diagram 예제"
---
Markdown Guide : https://www.markdownguide.org/

# 폰트 사이즈
```text
# h1
## h2
### h3
#### h4
```
# h1
## h2

# 소스링크
```text
[_구성정보_](/src/main/java/configuration/configuration.java)
```

# Diagram
### mermaid > graph TD
```text
mermaid
 graph TD
 A((Start)) --> |Request| B[filter]
 B---|DB| C{is Registerd}
 P1[Insert DB]-.-> |Before service| C
 C--> |No| E1[Cant Client]--> FIN((Err Response))
 C--> |Yes| V1[Search <br/>DB]
 V1--> OK

```

 ```mermaid
 graph TD
 A((Start)) --> |Request| B[filter]
 B---|DB| C{is Registerd}
 P1[Insert DB]-.-> |Before service| C
 C--> |No| E1[Cant Client]--> FIN((Err Response))
 C--> |Yes| V1[Search <br/>DB]
 V1--> OK
 ```

### mermaid > graph LR
```text
mermaid
 graph LR
 A((A System)) --> |Request|B((B System)) --> |token|C((Auth System))
 C --> |Auth DB|B
 B --> |Auth DB caching|B

```

 ```mermaid
 graph LR
 A((A System)) --> |Request|B((B System)) --> |token|C((Auth System))
 C --> |Auth DB|B
 B --> |Auth DB caching|B
 ```
 
 ### mermaid > sequenceDiagram
```text
mermaid
sequenceDiagram
  participant A as A System
  participant B as B System
  participant C as C System
  
  A ->> B : request
  activate A
  B ->> B : save
  B ->> C : request
  C -->> B : response
  B -->> A : response

```

 ```mermaid
 sequenceDiagram
  participant A as A System
  participant B as B System
  participant C as C System
  
  A ->> B : request
  activate A
  B ->> B : save
  B ->> C : request
  C -->> B : response
  B -->> A : response
 ```
 
# 소스코드
```text
  java 로 작성
```
```java
package chap01.exam01; // 패키지 선언

public class Hello {                         // 클래스 선언
    public static void main(String[] args) { // 메소드 선언
        // 실행문, 메소드가 호출될 때 실행하는 코드
        System.out.println("Hello");           
    }
}
```

# 표


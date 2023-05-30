# Markdown 문법 사용법

## Markdown과 git을 마스터하기 위한 김제갈의 몸부림

<br>
<br>
<br>
<br>

# 1. 마크다운(markdown)이란?

- 텍스트기반의 마크업언어로 2004년 존 그루버(John Gruber)와 아론 스워츠(Aaron Swartz)가 개발
- 읽고 쓰기 쉬운 문서 양식 지향하며
- Github는 마크다운을 변형한 Github-Flavored Markdown를 사용하며, 일부 HTML 태그와 혼용이 가능
  <br>
  <br>

## 1.1 장점

1. 간결하며 별도의 도구 없이 작성 가능
2. 다양한 형태로 변환이 가능하여 호환성이 좋음
3. Text 기반이므로 용량이 작음
   <br>
   <br>

## 1.2 단점

1. 표준이 없어 생성물에 대한 일관성 부족
2. 모든 HTML 마크업을 대신할 수 없음

---

<br>
<br>
<br>

# 2. 마크다운 문법

## 2.1 헤더(Headers)

```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```

# This is a H1

## This is a H2

### This is a H3

#### This is a H4

##### This is a H5

###### This is a H6

<br>

※ H1, H2는 아래의 형식으로도 사용 가능

```
This is a H1
============
This is a H2
------------
```

<br>
<br>

## 2.2 인용문(Blockquote)

```
> This is a first blockquote
>> This is a first blockquote
>>> This is a first blockquote
```

> This is a first blockquote
>
> > This is a first blockquote
> >
> > > This is a first blockquote

<br>
<br>

## 2.3 목록(list)

### 2.3.1 순서가 있는(ordered) 목록

```
1. first list
2. second list
3. third list

1. first list
    5.first list
        6.first list
```

1. first list
2. second list
3. third list

4. first list
   1.first list
   1.first list

<br>
※ 숫자와는 관계없이 무조건 순서대로 나타남
<br>
<br>

### 2.3.2 순서가 없는(unorderd) 목록

```
+ first list
+ second list
+ third list

* list
    * second list
        * third list

- first list
- second list
- third list
```

- first list
- second list
- third list

* first list
  - second list
    - third list

- first list
- second list
- third list

※ +,\*,- 모두 가능하며, 들여쓰기를 이용하여 검정 원 / 빈 원 / 검정 사각형 순서대로 중첩된 목록 생성가능

<br>
<br>
## 2.4 코드(code)

### 2.4.1 들여쓰기(indent)

```
This is normal.

    This is code.

```

This is normal.

    This is code.

한줄 띄어쓰지 않으면 인식하지 못함

### 2.4.2 코드블럭(태그방식)

```
<pre>
<code>
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello, World!");
  }

}
</code>
</pre>
```

<pre>
<code>
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello, World!");
  }

}
</code>
</pre>

### 2.4.3 코드블럭(코드블럭코드 방식)

````
```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello, World!");
  }
}
```
````

```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello, World!");
  }
}
```

코드블럭 내부에 백틱 세개를 넣고싶다면, 코드블럭 코드의 백틱 개수를 4개이상
Github 등에서는, 코드블럭의 시작점에 사용 언어를 작성하여 문법강조가 가능

## 2.5 수평선

```
* * *
***
*****
- - -
-----------------------------
```

---

---

---

---

---

## 2.6 강조

```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```

_single asterisks_

_single underscores_

**double asterisks**

**double underscores**

~~cancelline~~
문장 중간에 사용시엔 띄어쓰기

## 2.7 띄어쓰기

3칸 이상 띄어쓰기를 하면된다.

# 3. 미디어

## 3.1 링크

### 3.1.1 참조링크

```
//형식
[link keyword][id]

[id]: URL "Optional Title here"

// 실제코드
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"

### 3.1.2 자동연결

```
일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>
```

- 외부링크: <http://example.com/>
- 이메일링크: <address@example.com>

## 3.2 이미지

```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```

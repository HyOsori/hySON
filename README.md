# hySON
hySON(~~히슨~~하이슨)은 JSON을 Object로 변환해주는 라이브러리 입니다. [google-gson](https://github.com/google/gson) 등 많은 JSON 라이브러리가 있지만, 복잡한 오브젝트를 좀 더 쉽게 파싱하기 위해 개발하였습니다.

## Goals
* 복잡한 JSON 스트링을 한 번에 오브젝트로 변환합니다.
```java
hySON hyson = new hySON()
ResponseUsers response = hyson.Parse(jsonString, ResponseUsers.class);
```
```json
{
   "result" : 0,
   "message" : "success",
   "users" : [
     {
        "name" : "ho-u",
        "age" : 22,
        "language" : "c"
     },
     {
        "name" : "osori",
        "age" : 2,
        "language" : "c#"
     },
     {
        "name" : "hyhy",
        "age" : 22,
        "language" : "java"
     }, 
   ]
}
```
```java

class ResponseUsers
{
  int result;
  String message;
  ArrayList<User> users;
}

class User
{
  String name;
  int age;
  String language;
}
```
* 다양한 언어를 지원합니다.

## Install
* maven 지원 예정

## Supports
* JAVA
* C#(Comming soon...)
* C++(Comming soon...)

## Source
* [hySON-Java](https://github.com/HyOsori/hySON-Java) : JAVA

## Contributors
* [kanak87](https://github.com/kanak87)
* [violentjy](https://github.com/violentjy)
* [seohui](https://github.com/seohui)
* [soheeee](https://github.com/soheeee)


## License
```
The MIT License (MIT)

Copyright (c) 2016 Hanyang Osori

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

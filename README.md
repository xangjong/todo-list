# To do list 작성



<p align="center"><img src ="https://user-images.githubusercontent.com/101630615/205503528-87f39c72-034a-42b9-ae41-4b6679bf30e5.gif" width="1300px"></p>



#### 필요 기능

| 1    | todo 리스트 목록에 아이템을 추가        |
| ---- | --------------------------------------- |
| 2    | todo  리스트 목록 중 특정 아이템을 조회 |
| 3    | todo 리스트 전체 목록을 조회            |
| 4    | todo 리스트 목록 중 특정 아이템을 수정  |
| 5    | todo 리스트 목록 중 특정 아이템을 삭제  |
| 6    | todo 리스트 전체 목록을 삭제            |



### api

| [method](https://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html) | endpoint | 기능                  | request                              | response                                                     |
| ------------------------------------------------------------ | -------- | --------------------- | ------------------------------------ | ------------------------------------------------------------ |
| POST                                                         | /        | todo 아이템 추가      | {     "title": "자료구조 공부하기" } | {     "id": 17,     "title": "자료구조 공부하기",     "order": 0,     "completed": false,     "url": "http://localhost:8080/17" } |
| GET                                                          | /        | 전체 todo 리스트 조회 | -                                    | [     {         "id": 1,         "title": "자바 기초 공부하기",         "order": 0,         "completed": false,         "url": "http://localhost:8080/1"     },     {         "id": 2,         "title": "알고리즘 공부하기",         "order": 0,         "completed": false,         "url": "http://localhost:8080/2"     },  ...  ] |
| GET                                                          | /{:id}   | todo 아이템 조회      | -                                    | {     "id": 17,     "title": "자료구조 공부하기",     "order": 0,     "completed": false,     "url": "http://localhost:8080/17" } |
| PATCH                                                        | /{:id}   | todo 아이템 수정      | {     "title": "반복문 공부하기" }   | {     "id": 1,     "title": "반복문 공부하기",     "order": 0,     "completed": false,     "url": "http://localhost:8080/1" } |
| DELETE                                                       | /        | 전체 todo 리스트 삭제 |                                      | [200](https://ko.wikipedia.org/wiki/HTTP_상태_코드)          |
| DELETE                                                       | /{:id}   | todo 아이템 삭제      |                                      | [200](https://ko.wikipedia.org/wiki/HTTP_상태_코드)          |



[구현 사이트](https://www.todobackend.com/client/index.html?http://todobackend-aiohttp.herokuapp.com)

[테스트 사이트](https://www.todobackend.com/specs/index.html)

##### 

~~~R
setwd("C:\\studygo")
~~~
#### getwd() : 현재 설정된 작업공간 확인
#### setwd() : 새로운 작업공간 설정 (폴더 뒤/)

#### + 데이터 불러오기
#### load(file="")

#### + 저장 위치 파일 목록 확인
#### list.files()

#### + 변수목록
#### ls()

~~~R
install.packages("KoNLP")
install.packages("wordcloud")
~~~
~~~R
library("KoNLP")
library("wordcloud")
library("RColorBrewer")
~~~
~~~R
useSejongDic()
~~~
#### 세종 한글사전 열기

#### 해당 사전이 완벽하지 않다. 단어가 인식이 안될 경우가 있을 때
#### mergeUserDic(data.frame("내가 추가하고 싶은 단어","ncn"))
#### 여기서 ncn은 명사
~~~R
A <- readLines("이름.txt")
~~~
#### 분석할 텍스트 파일 불러오기 (줄마다 읽는다.)
~~~R
B <- sapply(A, extractNoun,USE.NAMES=F)
~~~
#### sapply 함수
#### : 벡터 또는 행렬 형태로 반환

#### + lapply -> 결과를 리스트 형태로 반환

#### extractNoun -> 한글명사만 가져온다 (KoNLP소속)
#### USE.NAMES=F -> T일 경우는 원문장, 명사 뽑은 것도 같이 나온다.
#### 따라서 이 경우에는 F로 둔다.


~~~R
C <- unlist(B)
C <- Filter(function(x){nchar(x)>= 원하는 글자 수}, C)
~~~

#### unlist() 리스트를 벡터로 변환
#### 원하는 글자 수 = 2 -> 두글자 이상 단어만 추출
#### + extractNoun("문장") -> 문장에서 단어 추출
~~~R
C 
C <- gsub("삭제하고 싶은 단어","",cosmos3)
~~~
#### 먼저 확인. 삭제할 단어가 있다면: "삭제하고 싶은 단어" -> "" 공백으로 대체하는 과정
#### 삭제할 단어가 여러 개 일때 앞서 gsub로 하나하나 삭제해도 되지만 이를 for문으로도 응용할 수 있다.
####  http://www.datamarket.kr/xe/?mid=board_ecko11&sort_index=title&order_type=asc&search_target=tag&search_keyword=R&page=2&document_srl=532

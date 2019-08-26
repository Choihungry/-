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


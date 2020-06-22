​	

## 'Complete Git Guide(Udemy Lecture)' Study 1 (2020.06.22)

### 1. What is Git ?

- Git is **Distributed version-control system**.

- Git manages history of every each file in a repository. But how?

  - Git stores **key and value** as a pair. Hash of a file is converted to a key and the content of the file is pared value.
  - Apprently, **the HashMap data structure** is used in the Git system.

- Git runs based on user's local environment, not depending on the internet. In other words, Git is just **a special file management system**.

- To fully tap into this Git system for a large size project in which many developers are involved, they have to use Git platform. The most famous and widely used one is **GitHub**.

- Since Github manages remote repositories on the internet, collaborations and teamworks become possible.

  

### 2. How Git works under the hood ?

- 특정 폴더를 git init 명령어를 통해 Git Repository로 설정하면 어떤 일이 벌어지는가?
  - 해당 폴더 내 숨겨진 **".git"**이라는 폴더가 저절로 생성된다.

![image-20200622232439450](P:\[Udemy] Complete Git Guide\img\image-20200622232439450.png)

- 위 명령어에서 보이듯, 내가 mkdir 명령어로 만든 git-practice 폴더에 git init을 입력하였으며, 그 결과 empty Git repository 가 .git 안에 만들어진 것을 확인할 수 있다.
- 또한 cmd의 dir /adh-r 명령어로 숨겨진 폴더들을 확인해보면 .git의 존재를 확인할 수 있다.

![image-20200622232914173](P:\[Udemy] Complete Git Guide\img\image-20200622232914173.png)

- 저 숨겨진 .git 폴더는 오로지 Git으로만 관리되어야 하므로, 사용자가 억지로 폴더를 찾아 들어가 내부 내용을 바꾸어서는 안된다.
- .git 폴더로 들어가보면 아래와 같은 파일들이 들어있음을 확인할 수 있다.

![image-20200622233816720](P:\[Udemy] Complete Git Guide\img\image-20200622233816720.png)

- 위 파일들을 살펴보면 config, description, HEAD라는 파일이 있음을 확인할 수 있다.
- 먼저 config는 당연하게도 내 repository의 환경설정을 뜻한다. cmd의 type 명령어로 파일을 열어보면 아래와 같은 사항을 확인할 수 있다.

![image-20200622234052814](P:\[Udemy] Complete Git Guide\img\image-20200622234052814.png)

- 뭔가 잘은 모르겠지만, 6개의 설정 사항이 어떤 것은 integer로, 어떤 것은 boolean형태로 선언되어 있음을 확인할 수 있다.

- description 및 HEAD의 내용은 아래와 같다.

![image-20200622234403528](P:\[Udemy] Complete Git Guide\img\image-20200622234403528.png)

- 우리는 막 git init 명령어로 repository를 생성하였으므로, 해당 repository는 unnamed로 설정되어있다.	
- 또한 HEAD파일에는 master라는 단어가 눈에 띄는 것을 확인할 수 있다.
- 이 각각의 파일들의 의미하는 것, 그리고 각각의 directory가 의미하는 것이 무엇인지를 차차 살펴볼 계획이다.
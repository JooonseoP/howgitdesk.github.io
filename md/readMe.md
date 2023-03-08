# GitHub Desktop 사용방법 정리
Git의 설치 방법과 사용방법을 정리한다.

## GitHub Desktop 설치
참고 : https://overit.tistory.com/entry/GitHub-Desltop-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EC%82%AC%EC%9A%A9

1) 다운로드  
![다운로드 이미지](../howgitdesk.github.io/images/01_GitHubDeskTop%20다운로드.png)  
다음의 링크에 들어가 'Download for Windows (64bit)' 버튼을 눌러 GitHub Desktop을 다운로드 받는다.  
GitHub Desktop : https://desktop.github.com/

2) 설치 진행  
다운로드 받은 설치 파일을 실행하여 진행한다.


1)) 다양한 경로(GitHub 뿐만 아니라 Private 환경의 Git)에서 사용하려면, 하단의 'Skip this step' 을 눌러서 넘어간다. 


![설치 이미지1](../howgitdesk.github.io/images/02_설치_페이지_01.png)  


2)) 이름과 이메일을 입력하라고 나오는데 여기서 GitLab, Git에서 사용하는 이름과 이메일을 넣어 준다.
다 작성한뒤 'Finish'를 눌러 진행한다.


![설치 이미지2](../howgitdesk.github.io/images/03_설치_페이지_02.png)  


3)) 3가지 항목이 나오게 된다. 내용을 말하자면 다음과 같고, 상황에 맡게 선택하여 진행하면 된다. 여기서는 기본인 'Add ad Exting Repository from your hard drive...' 를 선택해보겠다. 


![설치 이미지3](../howgitdesk.github.io/images/04_설치_페이지_03.png)  


- Clone a repository from the internet... (인터넷에서 기존 리포지토리를 복사)
- Create a New Repository on your hard drive... (새로운 Git 관리 리포지토리를 생성)
- Add an Exting Repository from your hard drive... (하드 드라이드에서 기존 리포지토리를 추가)Git Bash 


4)) 'Choose...'를 눌러서 Git 을 관리중인 폴더(해당 폴더 아래의 모든 폴더의 변화된 값을 감지하기 때문에, 특정 프로젝트 폴더를 선택해서 Add 하는 것을 추천한다. 또한 나중에 repository를 추가할 수 있다.) 를 선택하고 'Add repository'를 눌러 추가한다.    


![설치 이미지4](../howgitdesk.github.io/images/05_설치_페이지_04.png)   


5)) 추가가 정상적으로 시도 되었다면 다음과 같은 창이 나오게 된다.  
![설치 이미지5](../howgitdesk.github.io/images/06_설치_페이지_05.png)


### Git의 원리
(참고 : https://shxrecord.tistory.com/179)  
  
![Git의 원리 설명 이미지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcJ9IZ5%2FbtqDY1lY72w%2FZbMyGb6E3M412A9ordJDs1%2Fimg.png)  
Git은 위와 같이 사용되는데 작업 공간에서 작업하던 프로젝트를 작업자 PC의 가상공간인 준비영역에 저장한다. 이를 'add'라고 한다. 그렇게 더해진 준비 영역의 데이터를 로컬 저장소에 저장하기 위해서 약간의 설명을 적고 원격 저장소에 저장하기를 준비한다. 이 과정이 'commit' 준비가 다 된 Commit으로 포장된 내용을 Push를 통해 원격 저장소, Git이라 불리는 저장소에 정보를 올리게 된다.  
즉 임시공간에 저장한 내용이나 commit 까지 한 내용이 전부 올라가는 것이 아니라 push를 하기 전까지는 git에 올라가지 않는다. 하지만 그 사이의 잘못된 부분이 있으면 수정이 어렵기 때문에 한사람의 프로젝트 뿐만 아닌 여러 사람이 같이 작업중이 프로젝트를 다룰수도 있는 부분이기에 사용에는 조심해서 정보를 업데이트, 커밋해주도록한다.  
  
<용어설명>  
- 작업 공간: 올리고자 하는 파일이 있는 곳. 이 공간에 Git을 생성하여 형상 관리를 하게된다.  
- 준비 영역 : add를 통해 작업공간에 파일들이 저장된다. 로컬 저장소에 commit 되기 전 거쳐가는 영역이지만 준비영역을 거치지 않고 commit도 커밋이 가능하다.  
- 로컬 저장소 : 준비 영역에 있던 파일들을 commit하게 되면 로컬 저장소에 저장되며 최종 버젼이다.  
- 원격 저장소 : 로컬 저장소의 파일들이 push를 통해 원격 저장소에 올라간다.  


#### GitHub Desktop 사용

1) 내용 Commit, Push 하기   
변경된 내용이나 자신이 작성한 내용을 원격에 저장하고자 할 때, Commit을 할 수 있다.


1))  프로젝트 안의 내용이 변경되면 다음과 같이 수정된 내용을 볼 수 있다.


![Commit1](../howgitdesk.github.io/images/07_Commit_01.png)  


2)) 변경된 점과 내용을 정리하여 다음과 같이 좌측 하단에 내용을 작성하고 'Commit to main'을 선택한다.


![Commit2](../howgitdesk.github.io/images/08_Commit_02.png)  


3)) Commit이 완료가 되었다면 현재 Git의 Local 저장소에 저장이 되었다는 의미며, 이를 원격 저장소에 올리기 위해 Push를 해주어야 한다. 좌측 상단의 'Repositoy/Push' 를 찾아 누른다.


![Commit3](../howgitdesk.github.io/images/09_Commit_03.png) 


4)) 처음 Commit을 하게 되면 Git과의 연결을 묻는다. Git Lab에서 등록한 Username 과 Password를 작성하여 
'Save and retry'를 눌러 업로드 하게 된다.


![Commit4](../howgitdesk.github.io/images/10_Commit_04.png) 


2) 내용 Pull 하기 
본인이 작성한 내용보다 원격의 내용이 좀 더 진전이 있을 때나, 외부에서 작성한 내용으로 현재 프로젝트 내용을 Update 하려 할 때 Pull을 사용해야 한다.


1)) 좌측 상단의 'Repository/Pull'을 눌러 업데이트를 진행한다.


![Pull1](../howgitdesk.github.io/images/11_Pull_01.png) 


3) Clone, 원격 저장소의 내용을 현재 PC에 복사하기
원격의 프로젝트를 현재 PC에 내리받아 작성하고 싶을 때 사용하는 기능이다.


1)) 좌측 상단의 'File/Clone repository...'를 누른다.


![Clone1](../howgitdesk.github.io/images/12_Clone_01.png) 


2)) 그럼 다음과 같은 화면이 나오게 되는 이는 복사 받고 싶은 repository를 선택하는 화면이다. 
GitHub에 원하는 repository가 있다면 'GitHub.com' Tab의 원하는 프로젝트를 선택하고, GitLab이나 다른 프로젝트를 원한다면 URL Tab에서 해당 Git 주소를 붙여넣어 복사한다. (GitLab의 경우, 'Clone' 버튼을 누르고 Clone with HTTPS로 작성나오는 곳의 주소를 복사하면 된다.)  그리고 난 뒤,
하단의 Local path를 'Choose...' 를 누르거나 작성하여 현재 복사될 폴더의 위치를 선택한 뒤, 'Clone'을 눌러 저장한다.


![Clone2](../howgitdesk.github.io/images/13_Clone_02.png)


![Clone3](../howgitdesk.github.io/images/14_Clone_03.png)


![Clone4](../howgitdesk.github.io/images/15_Clone_04.png) 

3)) Clone이 잘되었다면 다음과 같은 화면을 지난다.


![Clone5](../howgitdesk.github.io/images/16_Clone_05.png) 


4)) Clone이 완료가 되었다면 다음과 같은 화면이 나온다.


![Clone6](../howgitdesk.github.io/images/17_Clone_06.png) 


4) branch 
프로젝트를 여럿이서 작성하거나, 추가 적인 기능이 있을 때 원본을 두고 원본에서 나온 다른 '가지(branch)'를 만들어 관리를 할 때 사용하는 기능이다. 


1)) branch 만들기
상단 중간에 Current branch를 눌러 'New branch' 버튼을 누른다.


![branch1](../howgitdesk.github.io/images/18_Branch_01.png) 


2)) branch 이름 정하기 
만들어질 branch의 이름을 적는다. 주로 기능 추가 같은 목적으로 branch를 만들기 때문에 기능의 이름을 적어 완성하는 것이 좋다. 이름 작성이 되었다면 'Create branch'를 눌러 brach를 생성한다. ex) QR 생성 기능 추가의 목적을 가진 brach의 이름 'gr_generate'


![branch2](../howgitdesk.github.io/images/19_Branch_02.png) 


3)) branch가 완성 되었다면
다음과 같이 상단의 branch 에 새로 작성한 branch의 이름이 작성되었다면 'local' 상태에서 branch가 생성된 것이다. 원격 저장소에 바로 branch를 만들고 싶다면 화면 중앙에 보이는 'Publish branch'를 누른다.


![branch3](../howgitdesk.github.io/images/20_Branch_03.png) 


4)) branch 관리 
다음과 같이 Current branch의 이름이 원하는 brach에 가 있다면 현재 위치하고 있는 local 폴더에서 작성한 내용을 현재 branch로 Commit, Push, Pull 할수 있다. branch는 새로운 기능이나 별개의 프로젝트로 가져가는 경우도 있으나, 다 작성이 된 후 main 프로젝트에 하나로 종합(merge)될 수도 있다.


![branch4](../howgitdesk.github.io/images/21_Branch_04.png) 


5) branch Merge
Main으로 Merge 하는 방식은 현재 GitLab을 사용해서 진행하고 있다. 그래서 여기 GitHub Desktop의 설명과는 약간 이질 성이 있으나 추가로 설명하고자 한다. 
참고 : https://www.bearpooh.com/77


1)) Merge 순서
개발자는 개발 중, 자신의 프로젝트 혹은 팀의 Project를 brach하여 개발하게 된다. 그렇게 일정 작업을 완수한 뒤, main 프로젝트와 합쳐지기 위해 'Merge Request'를 Git 관리자에게 요청한다. 관리자나 혹은 작성자는 해당 요청을 보고 review 하게 된다. review가 완료되어 충돌이 없을 경우 관리자의 승인에 의하여 Merge 된다.


2)) Merge Request - 01
다음과 같은 'Git Lab'의 좌측 화면에서 'Merge requests'를 눌러 Merge Request 화면을 들어가서 'New merge request'를 누른다.


![merge1](../howgitdesk.github.io/images/22_Merge_01.png)


3)) Merge Request - 02
좌측의 'Source branch'는 main과 Merge될 branch를 선택하고 우측에서는 같이 합치게 될 'Target branch'를 선택한다. 선택이 되었다면 'Compare branches and continue' 버튼을 눌러 진행한다.


![merge2](../howgitdesk.github.io/images/23_Merge_02.png)


4)) Merge Request - 03
Merge 할 내용을 세밀하게 작성하게 되는데 각 내용을 설명해보자면 


- Title (required) : Merge 할 내용의 타이틀을 묻는 것으로 제목 만 봐도 내용을 알 수 있을 정도로 작성해둔다.
- Description : 상세 내용을 기술한다. branch에서 작성한 내용을 기술하며, 상세히 작성하도록 한다.
- Assignee : 승인자를 묻는다. 옆의 'Assign to me'를 누르게 되면 본인으로 되지만 본인이 Merge 권한이 없다면 사용할 수 없다.
- Reviewer : branch 내용을 리뷰할 사람으로, 개발자 본인과 관리자가 같이 봐야 할 것 같다. 이는 관리자가 위에서 승인자 역할로 있기 때문에 여기는 branch를 작성한 본인이 들어가는 것이 옳다고 생각한다.
- Milestone : 마일 스톤을 생각하는 것으로 Project의 진행 할 내용 중 어디에 작성되는 것이 옳다고 판단 되는 MileStone을 넣는다. 
- Label : 이슈 내용이나 패턴을 Label로 분류하는 것으로 작성자는 이슈를 관리중인 type 분류로 내용을 작성하였다.  아래 참고
- - feat : 신규기능 추가
- - fix: 버그수정
- - docs: 문서관련
- - chore: 빌드관련 수정, 패키지 매니저 관련 수정
- - add [some] : 기능과 문서가 아닌 리소스류
- - delete
- - update: 버전 업데이트
- - move: 소스코드 이동
- - modify: 수정
- Merge options : merge하게 되었을 때의 옵션으로 
- - Remove source branch when merge request is accepted. : Merge request가 성공하였을 때 branch를 삭제
- - Squash commits when request is accepted. About this feature : Merge 할 때 브랜치에서 커밋한 내역을 유지할 것인지 결정하는 부분이다. 체크하면 기존 브랜치에서 작업한 내역은 하나의 커밋으로 통합되고, main 에는 하나의 커밋 분기 이력만 남는다.


각 내용을 작성하고 난 뒤, 'Create merge request'를 눌러 Merge를 요청한다.


![merge3](../howgitdesk.github.io/images/23_Merge_03.png)


5)) Merge review 하기 
Merge request를 하였을 때 Merge 할 내용을 점검하는 순간이 필요한데, 여기서 Review 를 하게 되는 것이다. review 할 수 있는 건 Reviewer로 등록되거나 Asignee 로 등록된 사용자로, 둘의 Approve 가 있어야 Merge 될 수 있다. 다음 이미지를 보면 위에 있는 'Commits'에서 Commit들의 내용을 확인할 수 있고 'Changed'를 통해 작성된 코드의 변경 요소를 확인할 수 있다.


![merge4](../howgitdesk.github.io/images/24_Merge_04.png)


6)) 내용이 너무 많을 경우나 문제가 있을 경우 Conflict가 발생할 수 있다. 그럴 경우, Conflict를 해결해야 Merge를 할 수 있어, 상단의 'Resolve conflicts'를 눌러 Conflict 내용들을 확인한다. 
문제가 되는 코드들을 보여주게 되는데,


origin // their changes => 기존 main의 코드 부분

Head// our changes => 현재 branch로 추가되거나 변경된 코드

로 출력된다. 이 두 코드를 비교 하며 사용할 코드 옆의 'Use this'를 눌러 conflicts를 해결한다.

참고 : https://thsd-stjd.tistory.com/138

7)) Conflict가 끝나고 리뷰가 끝나게 되었다면 다시 Merge Request 화면에서 Approve 버튼이 활성화 되어 누를 수 있게 된다. 이를 Reviewer 와 Assignee가 둘다 Approve를 하게 되면 Merge가 된다.


![merge4](../howgitdesk.github.io/images/24_Merge_04.png)


##### 현재 작성 내용 여기 까지 (23/03/08) 내용 추가나 수정이 필요할 경우 업데이트 할 예정
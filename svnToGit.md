# SVN to Git with history  

참고한 곳 : [SVN에서 Git으로 전환하기](https://gist.github.com/ikaruce/9c8dc57849e003df6fdc)  
  [1 Git으로 이전하기 - Git과 Subversion](https://git-scm.com/book/ko/v1/Git%EC%9C%BC%EB%A1%9C-%EC%9D%B4%EC%A0%84%ED%95%98%EA%B8%B0-Git%EA%B3%BC-Subversion)
  
  
* git svn 을 통해서 svn을 git 으로 전환할 수 있다.  

* 사전 준비 : 필자의 경우 우분투에서 작업, 사전에 git 뿐 아니라 git-svn 을 추가로 설치 해야 했다.


1. git 으로 사용할 폴더를 하나 생성
~~~
  $ mkdir git-folder
  $ cd git-folder
~~~

2. git-svn을 통해 git repository 초기화
~~~
  $ git svn init [svn repository url] -T trunk -b branches -t tags
~~~
  * 설정되어 있는 svn 구조에 맞게 맞춰줘야 함.  
    필자의 경우 svn repository 안에 project folder 가 있고 그 안에 trunk, branches, tags 폴더가 있어서     
    git svn ```[svn repository url]/project``` 이렇게 해주었음.  
  * trunk, branches, tags 폴더 명도 다르게 셋팅 되어 있다면 그대로 맞춰줘야 함.  
    
      
3. svn 히스토리 가져오기
~~~
  $ git svn fetch
~~~

<img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=250&section=header&text=G.G&fontSize=90" />

---
# 팀 이름: G.G (Good Game)

### 팀 멤버 소개: 

이아진 팀장

김경돈 대리

이현준 대리

장연서 대리

---

# 필독사항

## 항상 pull 먼저 진행.
각자 개인 branch 생성후 작업 진행!!
본인 branch 에서 작업후 커밋, push 한 뒤에 팀장한테 merge요청!!
팀장이 merge 승인한걸 확인하면 local branch 삭제
브랜치를 삭제하는 이유는 원본 저장소에 Merge가 완료되면 작업공간이 더이상 필요 없으므로 삭제한다.

pull -> git branch [사용할 브랜치명] git switch [사용할 개인브랜치] -> 작업 -> add, commit -> git push origin [사용할 개인브랜치]
-git push하는 과정에서 오류가 뜰 경우 origin +main으로 해볼것.

```
 $ git pull origin main
 $ git add .
 $ git commit -m " 커밋내용 "
 $ git push origin [branch name]
 
 push error시에 바꿔봐야 할 코드
 $ git push origin +[branch name]
 
```

---
### 프로젝트 소개 및 목표 :

- JAVA를 활용해 탄막게임을 모티브로 둔 미니게임만들기.

```

### 프로젝트 진행방향:

1. 프로젝트 기획
2. UI구현 및 디자인 회의
3. 도트작업
4. 보스 구성 및 구현
5. 디버깅
6. 마무리


```


## 메인화면 주요메서드
```
- EndingCredit() 생성자: 객체 초기화 및 설정 메서드(initObject() 및 initSetting())를 호출하고, 창을 표시하기 위해 setVisible(true)을 호출

- initObject() 메서드: UI 요소와 이벤트 핸들러를 초기화

backgroundMain: 배경화면 이미지를 JLabel로 설정
backIcon 및 backhovericon: 뒤로가기 버튼에 사용할 이미지 아이콘을 로드
backButton: 뒤로가기 버튼을 생성하고 위치와 스타일을 설정 그리고 이벤트 리스너를 등록
initSetting() 메서드: 프레임의 제목, 크기, 레이아웃, 위치 및 종료 동작을 설정

코드의 주요 목적은 EndingCredit 클래스를 사용하여 엔딩 크레딧 화면을 표시하고, 뒤로가기 버튼을 클릭하면 MainFrame 클래스의 인스턴스를 만들어 표시했습니다.
```

## 게임플레이 주요메서드
```
- Game() 생성자: 게임 화면을 초기화하고 필요한 객체들을 생성. 게임의 초기 설정, 플레이어 및 몬스터의 초기 위치, 체력 등을 설정

- actionPerformed(ActionEvent e): 주요 게임 로직이 포함된 메서드/ 게임의 상태 변화, 이동, 충돌 감지 등을 처리 / 주요 동작으로는 플레이어 및 몬스터의 이동, 공격 등이 있음.아이템과의 충돌, 몬스터의 체력 및 스테이지 진행 상황을 확인 /화면을 다시 그리기 위해 repaint()를 호출

- paintComponent(Graphics g): 게임 화면을 그리기 위한 메서드. 배경, 플레이어, 몬스터, 발사체 등을 그리고 플레이어 및 몬스터의 체력, 아이템 상태 등을 화면에 표시

- keyPressed(KeyEvent e) 및 keyReleased(KeyEvent e): 키보드 이벤트를 처리하는 메서드. 사용자가 키를 누를 때와 뗄 때의 동작을 처리하고 이동 및 발사 동작에 대한 상태를 업데이트

- firePlayerProjectile(): 플레이어가 발사체를 발사하는 메서드입. 현재 플레이어의 위치 및 방향을 기반으로 발사체를 생성하고, playerProjectiles 리스트에 추가

- resetGame(): 게임을 초기 상태로 재설정하는 메서드. 플레이어와 몬스터의 위치를 초기화하고, 체력, 발사체 등을 초기화

attack1(), attack2(ActionEvent e), attack3(ActionEvent e): 몬스터의 공격 패턴을 처리하는 메서드. 각각 다른 공격 패턴에 따라 몬스터가 발사체를 생성하고, 이를 monsterProjectiles 리스트에 추가/스테이지 진행에 따라 공격 패턴이 달라짐!

위의 메서드들은 게임의 로직을 담당하고 플레이와 목스터의 동작, 공격, 이동 등을 처리하게끔 진행했습니다. 또, 키보드 이벤트를 감지해 발사체를 만들고 게임상태 초기화 등을 담당하게 했습니다.

```




# 게임 진행방향

![1](https://github.com/ohohooh123/GG_project/assets/45931408/78fef224-b389-4e9e-bac3-a802b9d9626f)

메인 페이지 게임 시작 click ->

![2](https://github.com/ohohooh123/GG_project/assets/45931408/f5bbdfc8-1b89-4b93-b8d6-af795f51862c)

맵 중 떠있는 안경을 먹을 시 갑옷(정장)을 입으며 체력 상승

![3](https://github.com/ohohooh123/GG_project/assets/45931408/28a3e789-02e6-464a-8186-09e6d28ca530)

![4](https://github.com/ohohooh123/GG_project/assets/45931408/2160da19-4858-40df-9205-e499a076fb91)

첫번째 몬스터 해치울 경우, 2번째 보스 등장 문구

![5](https://github.com/ohohooh123/GG_project/assets/45931408/5df5ab10-f88a-46ed-af4a-97a24ed53934)


# Tools
<div align=center>
  <h1>Studying !</h1>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=&logoColor=white"/>
  <img src="https://img.shields.io/badge/Github-181717?style=flat-square&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/vsCode-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tomcat-F8DC75?style=flat-square&logo=apachetomcat&logoColor=white"/>
  <img src="https://img.shields.io/badge/Eclipse-2C2255?style=flat-square&logo=eclipseide&logoColor=white"/>
  <img src="https://img.shields.io/badge/json-000000?style=flat-square&logo=json&logoColor=white"/>
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=white"/>
  <img src="https://img.shields.io/badge/python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white"/>
  <img src="https://img.shields.io/badge/git-F05032?style=flat-square&logo=git&logoColor=white"/>
</div>

# 방문자 수
<a href="https://github.com/LeeAhjin96"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FLeeAhjin96&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
더 빨라진 패턴과 다양한 공격 / 

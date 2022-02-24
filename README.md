# devops0223
20220223 TTA DevOps 저장소입니다.

## Git 초기 설정
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

## 해야할 일
- Git Commit하기 
- Git Push하기
- Jenkins 얼른 하기
- 퇴근하기

## 로그인 기능 개발
// 코드라고 가정....6자리인지 로지
// 아이디에 한글 있는지 확인....


## Jenkins 에서 커버리지 표현하기
### 플러그인 설치
- Cobertura 플러그인 설치

## Unittest 결과를 Jenkins에서 보기
### Unitetest 결과의 xml 저장 도구 설치
pip install unittest-xml-reporting

### 실행
```
del testReport /s /f /q
python -m xmlrunner discover -o testReport
```

### Jenkins
Junit 테스트 결과와 매핑
![image](https://user-images.githubusercontent.com/8405564/155468303-37c4951d-b48e-4832-a899-0acaabe87460.png)

![image](https://user-images.githubusercontent.com/8405564/155468454-a899cd37-9b07-4dbe-ac50-4964e9331ecb.png)

```
testReport/TEST-*.xml
```


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


## Liazrd 설치 (순환복잡도 분석)
```
pip install lizard
```

### Lizard 실행해서 엑셀파일로 저장 (순환복잡도 10 이상)
```
lizard.exe -C 10 --csv > lizard_result.csv
```

### Jenkins를 위한 실행
```
lizard -C 10 -L 80 --xml > lizard.xml
```

### Jenkins 플러그인
CppNCSS 플러그인 이용

### Jenkins 설정
![image](https://user-images.githubusercontent.com/8405564/155474775-10bacab5-6bc3-43ee-9d11-49e2cd7a75e9.png)


## CPD 실행
100 Token 이상, C++ 을 대상으로 분석, 엑셀에서 확인하기 위해 csv로 출력해서 저장
```
cpd.bat --minimum-tokens 100 --files . --language py --format csv > cpd_result.csv
```

### Jenkins를 위한 실행
```
cpd --minimum-tokens 100 --files . --language py --format xml > cpd.xml
```

### Jenkins를 위한 설정
- Warning Next Generation 플러그인 이용
- 내부에서 CPD 지정


## CPPChcek 실행
```
"c:\Program Files\Cppcheck\cppcheck.exe" --enable=all --inconclusive --xml --xml-version=2 src 2> cppcheck.xml
```



## CLOC 다운로드
https://github.com/AlDanial/cloc/releases/tag/v1.90

## CLOC 실행
```
cloc-1.90.exe --by-file --csv . > cloc_result.csv
```

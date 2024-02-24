# 파이썬 3 설치 (Install Python 3)
## 파이썬 3 설치 (Install Python 3)
- mac에서 brew로 설치
```
brew install python@3.11
```

## 파이썬 설치 확인
```
python --version or python3 --version
```
​
## [에러] zsh: command not found: python or 파이썬 버전 변경
- 파이썬 설치된 위치 찾기
```
which python3
// or
ls -l /usr/local/bin/python*
// or
ls -l /opt/homebrew/bin/python*
​```

## 알리아스 설정해 주기
```
echo "alias python=설치된위치경로" >> ~/.zshrc
// or
ln -s -f /usr/local/bin/python3.9 /usr/local/bin/python
// or
ln -s -f /opt/homebrew/bin/python3.9 /opt/homebrew/bin/python
```
​

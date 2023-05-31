# Python SMTP Server 연동 에러 해결

## 문제
### 1. smtp 호스트 서버 연결시
UnicodeDecodeError: 'utf-8' codec can't decode byte 0xc1 in position 0: invalid start byte
에러

### 해결 방법
- 컴퓨터 호스트명을 영문으로 바꾸면 해결
-> 모든 사람의 PC를 바꿔야 하는 문제 발생

- python lib의 socket.py에서 소스 코드 수정
-> hostname을 제대로 인코딩시켜줌

```python
def getfqdn(name=''):
    name = name.strip()
    if not name or name == '0.0.0.0':
        name = gethostname()
    try:
        hostname, aliases, ipaddrs = gethostbyaddr(name)
    except error:
        pass
```
```python
def getfqdn(name=''):
    name = name.strip()
    if not name or name == '0.0.0.0':
        name = gethostname()
    try:
        hostname, aliases, ipaddrs = gethostbyaddr(name.encode('ascii', 'ignore'))
    except error:
        pass
```

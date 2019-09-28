# MapleLib

1. 단순 함수는 함수 호출자만 가지고 있고 get과 set은 suffix에 ~를 적고 그 뒤에 접근 가능한 방식을 기입합니다.
2. prefix가 없다면 public 입니다. 사용자가 접근 가능합니다.
3. prefix \* is private.
4. prefix # is internal

## WzLib

### WzFile

#### new(short gameVersion, WzMapleVersion version)
gameVersion: 게임의 버전을 나타냅니다.  
version: enum 타입의 WzMapleVersion로 나타낸 메이플스토리 wz의 국가별 encoding 방식입니다. 이 값을 통해 wz를 파싱합니다.

=> 기본 초기화를 시도합니다.

#### new(string filePath, WzMapleVersion version)
filePath: wz 파일의 string 경로입니다.  
version: enum 타입의 WzMapleVersion로 나타낸 메이플스토리 wz의 국가별 encoding 방식입니다. 이 값을 통해 wz를 파싱합니다.

#### new(string filePath, short gameVersion, WzMapleVersion version)
filePath: wz 파일의 string 경로입니다.  
gameVersion: 게임의 버전을 나타냅니다.  
version: enum 타입의 WzMapleVersion로 나타낸 메이플스토리 wz의 국가별 encoding 방식입니다. 이 값을 통해 wz를 파싱합니다.

#### ParseWzFile()
=> 메인 Wz 디렉토리를 파싱하고 가비지 컬렉터를 실행합니다.  
> 참조: #Fn ParseMainWzDirectory()

#### ParseWzFile(byte[] WzIv)
=> WzIv를 지정한 다음 non parameter fn과 동일하게 ParseMainWzDirectory를 실행하여 wz를 파싱합니다.  
> 참조: #Fn ParseMainWzDirectory()

#### WzDirectory ~ get
내부 wzDir을 반환합니다.

#### Name ~ get, set
내부 Name을 반환합니다.


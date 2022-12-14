# SVN 이란?

SVN은 SubVersion의 줄임말로 중앙집중관리식 형상관리 소스 관리 툴이다.
로컬 pc에서 커밋 시 중앙 저장소에 바로 반영

1. SVN 필요성
   - 기존의 파일 시스템 공유 등으로 문제 발생 시 복구
   - 프로젝트 진행 중 과거의 특정 시점으로 돌아가야 하는 경우
   - 여러 사람이 같은 프로젝트에 참여 할 경우, 각자가 수정한 부분을 팀원 전체가 동기화하는 과정을 자동화
   - 소스 코드의 변경 사항을 추적
   - 소스 코드에서 누가 수정했는지 추적
   - 대규모 수정 작업을 더욱 안전하게 진행
   - 마이너 버전(branch)로 프로젝트에 영향을 최소화하면서 새로운 부분을 개발


2. SVN 장점  
   - 원자적 커밋을 지원하므로 다른 사용자의 커밋과 엉키지 않음. 실패 시 롤백 가능
   - 직관적이다.
   - 파일과 디렉토리의 삭제, 이동, 이름 변경, 복사 지원
   - 소스파일 이외에 이진 파일(텍스트파일이 아닌, 컴퓨터 파일)도 효율적으로 저장 가능
   - 디렉터리도 버전 관리를 할 수 있다.
   - 저장소의 크기에 상관없이 일정한 시간 안에 가지치기나 태그를 할 수 있다.
   - 처리 속도가 상대적으로 빠르다.


3. SVN 단점  
   - 소스코드는 merge(병합)이 가능하지만 이진파일은 어느 한쪽을 버릴 수밖에 없다.
   - 개별 개발자만의 개발 이력을 가질 수 없다.
   - .svn 디렉터리로 인해 저장소가 다소 지저분한 느낌을 준다.
   - 잦은 커밋으로 인해 리비전 번호가 크게 증가할 수 있다.
   - 충돌이 일어날 확률이 높다.




4. SVN 용어 정리
   - CheckOut : 저장소에서 최신 버전의 소스코드를 최초로 받아오는 것
   - Update : 로컬 저장소에 있는 파일들을 저장소의 최신 버전으로 받아오기
   - Commit : 로컬 저장소의 변경된 내용을 서버로 전송
   - Merge : 내가 작업한 부분과 다른 사람이 작업한 부분을 병합한다.
   - Repository : 프로젝트 파일 및 변경 정보가 저장되는 장소
   - Revision :  수정 후 Commit 하면 숫자가 증가
   - Import : 빈 Repository에 맨 처음 파일을 채우는 것
   - Export : 버전 관리 파일들을 뺸 순수 파일만 빼내는 것
   - Revert : 로컬 저장소의 내용을 이전 상태로 돌림
   - Add : 버전 관리 대상으로 파일 등록
   - Shelve : 로컬 작업 내용을 잠시 백업
   - Trunk : 개발 소스를 commit 했을 때 개발 소스가 모이는 곳
   - Branch : trunk에서 분리/복사한 소스로 버전별 배포판을 만들거나 trunk와 별도로 운영환경을 위한 안정화된 소스 관리 목적으로 사용
   - Tag : 버전 별로 소스코드를 따로 관리하는 공간 

[참고](https://truecode-95.tistory.com/18)

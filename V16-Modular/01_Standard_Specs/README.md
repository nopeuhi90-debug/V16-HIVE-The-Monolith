📁 01_Standard_Specs: 물리적·전기적 성전
업체들이 "우리 제품에 구멍을 어디 뚫어야 해?"라고 물을 때 던져줄 문서입니다.

Module_Interface_V1.pdf:

육각형 모듈 외형 (지름 38mm, 변의 길이 21.94mm).

40핀 BTB 커넥터 실장 좌표: Center (0,0) 기준 정중앙 배치.

PCB 두께: 1.6mm ~ 2.0mm (구조적 강성 확보 필수).

V16_Pinout_Master.csv:

L1~L16: 독립 16레인 전원 출력 (각 레인당 최대 2A 설계).

HIVE-Link Data (SDA/SCL): 모듈 인식 및 데이터 통신용.

Clock Sync (REF+ / REF-): 마스터 클럭 동기화 차동 신호.



📁 02_Hardware_Design: 3D 설계의 정수
"백문이 불여일견", 업체들이 자기네 CAD 소프트웨어에서 바로 불러올 파일입니다.

V16_Module_Base_Model.step:

육각형 모듈의 표준 3D 형상 데이터.

Thermal_Coupling_Guide.md:

상단 나노 탄소 패드 부착 영역 설계도.

"레이어 6 CNC 쉴드와 밀착 시 0.1mm 프리로드(Pre-load)를 유지할 것" 명시.



📁 03_Schematics: 전기적 DNA
업체들이 회로를 짤 때 무조건 복사해서 붙여넣어야 할 레퍼런스입니다.

LT3045_Killer_Bank_Ref.pdf:

LT3045 8개를 병렬로 묶어 리플 노이즈를 살해하는 마스터 회로도.

HIVE_Link_Reference_Circuit.png:

본체와 통신하기 위한 최소한의 MCU(또는 Logic IC) 구성도.

"이 회로가 없으면 본체는 전력을 공급하지 않음" 경고 문구 삽입.



📁 04_BOM: 품질의 마지노선
"가성비 찾다가 쓰레기 부품 쓰지 마라"고 명령하는 명단입니다.

Uncompromising_BOM_List.xlsx:

LDO: Analog Devices LT3045 (Fixed).

Resistors: Vishay Dale 0.1% 정밀 저항 권장.

Connectors: Hirose 또는 Samtec 정품 40핀 BTB 필수.

Anti_Counterfeit_Guide.md:

알리익스프레스 등 검증되지 않은 곳에서의 부품 조달 금지 조항.

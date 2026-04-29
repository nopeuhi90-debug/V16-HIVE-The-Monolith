# 🔌 Adapters & Interposers (호환성 확장 어댑터)

This directory contains design data for adapting standard PC components and third-party hardware to the **V16-HIVE** 40-pin modular slot.
이 카테고리에는 기존 PC 부품 및 타사 하드웨어를 **V16-HIVE** 40핀 모듈러 슬롯에 호환시키기 위한 어댑터 설계 데이터가 포함되어 있습니다.

---

## 🚀 Concept (개념)
We aim to break the boundaries of audio hardware by providing interposers for:
우리는 다음과 같은 인터포저(어댑터)를 통해 오디오 하드웨어의 경계를 허물고자 합니다:

* **M.2 to HIVE:** For high-speed data buffers or specialized audio clocks. (고속 데이터 버퍼 또는 특수 오디오 클럭용)
* **SO-DIMM Interface:** Utilizing the RAM form factor for high-density filter modules. (고밀도 필터 모듈을 위한 램 슬롯 형태 활용)
* **PCIe Bridge:** Connecting external DSP or high-end sound cards. (외부 DSP 또는 하이엔드 사운드카드 연결)

## ⚠️ Guidelines (설계 지침)
1. **Signal Integrity:** All adapters must maintain differential impedance rules (100Ω).
   (모든 어댑터는 차동 임피던스 규칙(100Ω)을 준수해야 합니다.)
2. **Power Isolation:** Adapters must not introduce noise back into the Hive Command mainboard.
   (어댑터는 메인보드로 노이즈가 역유입되지 않도록 설계되어야 합니다.)


# 🛠️ V16-HIVE Adapter & Interposer Guide
본 폴더는 V16-HIVE의 40핀 슬롯을 활용한 다양한 모듈 설계 지침을 다룹니다.

## 1. "Killer Chipset" Strategy (킬러 칩셋 전략)
시중의 중구난방인 기성 DAC 보드에서 '영혼(칩셋)'만 추출하여 V16-HIVE에 통합하는 핵심 전략입니다.

* **Power Purge (전원 숙청):** - 기성 보드의 저가형 레귤레이터를 우회(Bypass)합니다.
    - 40핀 슬롯의 **LT3045** 초저노이즈 전원을 DAC 칩셋에 직접 공급합니다.
* **Signal Direct Injection (신호 직결):** - 기성 보드의 입력을 무시하고, 메인보드의 순수 I2S/DSD 신호를 칩셋에 직접 주입합니다.
* **Analog Extraction (아날로그 추출):** - 칩셋의 로우(Raw) 출력을 메인보드의 **Monolith Output Stage**로 직접 전달합니다.

## 2. Module Categories (분류)
* **DAC Modules:** ESS Sabre, AKM, Burr-Brown, R-2R Discrete.
* **Storage/Buffer:** M.2 SSD Interface for ultra-low latency audio serving.
* **Clock Modules:** External OCXO/Atomic clock integration.
* **Analog Buffers:** Vacuum Tube, Class-A Discrete buffers.

## 3. Design Template
- 육각형 PCB 템플릿(Altium/KiCad)은 본 폴더의 `/Templates`를 확인하십시오.

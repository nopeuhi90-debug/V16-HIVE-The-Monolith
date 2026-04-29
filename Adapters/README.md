# 🛠️ Adapters & Interposers (호환성 확장 어댑터)

This directory contains design data for adapting third-party hardware to the **V16-HIVE** 40-pin modular slot. 
(이 카테고리에는 타사 하드웨어를 V16-HIVE 40핀 모듈러 슬롯에 호환시키기 위한 설계 지침이 포함되어 있습니다.)

## 1. "Killer Chipset" Strategy (킬러 칩셋 전략)
시중의 중구난방인 기성 DAC 보드에서 '영혼(칩셋)'만 추출하여 V16-HIVE에 통합하는 핵심 전략입니다.

* **Power Purge (전원 숙청):** Ignore low-quality on-board regulators. Power only the essential DAC chipset using V16-HIVE's ultra-low noise **LT3045** power rails. (기성 보드의 조잡한 전원부는 무시하고, 본체의 LT3045 전원만을 칩셋에 공급합니다.)
* **Signal Direct Injection (신호 직결):** Bypass on-board inputs. Inject pure I2S/DSD signals from the **Hive Command** directly into the chipset. (기성 보드의 입력을 무시하고 메인보드의 순수 디지털 신호를 칩셋에 직접 주입합니다.)
* **Analog Extraction (아날로그 추출):** Send raw analog output directly to the **Monolith Output Stage** on the mainboard. (칩셋의 출력을 본체의 모노리스 출력단으로 직접 전달합니다.)

## 2. Module Categories (분류)
* **DAC Modules:** ESS Sabre, AKM, R-2R Discrete, etc.
* **Clock Modules:** External OCXO/Atomic clock integration.
* **I/O Bridges:** M.2 to HIVE, PCIe Bridge for high-end sound cards.

## 3. Design Guidelines (설계 지침)
1. **Signal Integrity:** All adapters must maintain differential impedance rules (100Ω).
2. **Power Isolation:** Adapters must not introduce noise back into the Hive Command mainboard.

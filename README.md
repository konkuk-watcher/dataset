data for classifier

---

Russia: armata, bmpt, bmpt_72, bmt_72, bmpt_84, drozd, pt76, sprut_sd, sprut_sdm1, t12, t55, t55_enigma, t62, t64, t64b1m, t64bm_bulat, t64e, t72, t72b3, t72b4, t72m2, t72m4, t72ua1, t80, t80b, t80bvm, t80u, t80ud, t80um1, t84, t84_yatagan, t90, t90m, t90m_tagil, t95


China: gl5, mbt_3000, type_62, type_63, type_63a, type_74, type_80, type_90, type_90-2, type_96, type_98, type_99, type_99g, vt2, vt4, vt5, zbd_2000, ztq_15


Iran: karrar, sabalan, tosan, zulfiqar_1, zulfiqar_2, zulfiqar_3


North Korea: m1985, m2002, st2, unidentified


South Korea: k1, k1a1, k2, k21_105, k21_with_xc8

---
현실적으로 너무 종류가 많아 성능이 굉장히 낮을것으로 예상되어 데이터셋을 재구성한다.

북한이 많이 운용하며, 한국전쟁 재발시에 개입 현실성이 제일 높은 중국의 육군을 대상으로 진행할것이다.

| 클래스 번호 | 클래스명              | 설명              | 예시 장비                 |
| ------ | ----------------- | --------------- | --------------------- |
| 1      | **MBT (주력전차)**    | 전장의 주력 전차       | ZTZ-99A, ZTZ-99, ZTZ-96, ZTZ-96, ZTZ-88 |
| 2      | **Light Tank (경전차)**    | 전장의 경전차       | ZTQ-15, ZTQ-05 |
| 3      | **IFV (보병전투차)**   | 보병 수송 + 전투      | ZBD-04, ZBL-08, ZTL-11, BMP-1         |
| 4      | **AAV (돌격장갑차)**   | 보병 수송, 무장 적음    | ZSL-92, ZBD-05, ZSL-92B      |
| 5      | **APC (수송장갑차)**   | 보병 수송, 무장 적음    | ZSD-89, ZSL-10, ZSL-92A      |
| 6      | **MLRS (다연장 로켓)** | 대량 로켓 발사 시스템    | PHL-16, PHL-03, PHL-11          |
| 7      | **SPG (자주포)**     | 자주포탑/차량  | PLZ-05, PCL-181, PLZ-07, PLL-09, PCL-171, PCL-09, PLZ-89, PPZ-10, PLL-05          |
| 8      | **Towned Gun (견인포)** | 견인포 | Type-66, Type-59, Type-96   |
| 9      | **SAM** | 견인포 | HQ-16, HQ-17, HQ-7   |
| 10      | **Others (기타)**   | 군용 트럭, 레이더 등 기타 | Ural-375, Dongfeng EQ |
---
데이터셋 구조 수정

시각적으로 유사한 클래스들을 묶어서 정확성을 올림

| 클래스 번호 | 클래스명              | 설명              | 예시 장비                 |
| ------ | ----------------- | --------------- | --------------------- |
| 1      | **Tank**    | 주력전차+경전차       | ZTZ-99A, ZTZ-99, ZTZ-96A, ZTZ-96, ZTZ-88, ZTQ-15, ZTQ-05 |
| 2      | **Armored Vehicle**   | 장갑차계열(IFV, AAV, APC)      | ZBD-04, ZBL-08, ZTL-11, BMP-1, ZSL-92, ZBD-05, ZSL-92B, ZSD-89, ZSL-10, ZSL-92A         |
| 3      | **MLRS** | 대량 로켓 발사 시스템    | PHL-16, PHL-03, PHL-11          |
| 4      | **SPG**     | 자주포탑/차량  | PLZ-05, PCL-181, PLZ-07, PLL-09, PCL-171, PCL-09, PLZ-89, PPZ-10, PLL-05          |
| 5      | **Towed Gun** | 견인포 | Type-66, Type-59, Type-96   |
| 6      | **Air Defence System** | SAM+대공 | HQ-16, HQ-17, HQ-7, HQ-6, PGL-12, PGZ-09   |
| 7      | **Others**   | 군용 트럭, 레이더 등 기타 | Ural-375, Dongfeng EQ |

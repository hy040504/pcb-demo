# 샘플 PCB 이미지 (공개 데이터셋)

데모(`demo.html`)의 검사 이력·PCB 검사 화면에 쓰는 이미지입니다. 모두 공개 데이터셋에서 가져와 **4:3.4 비율로 잘라 760px(DeepPCB는 640px) JPG로 줄인 것**이며, 이미지 내용은 수정하지 않았습니다.

| 파일 | 출처 | 라이선스 | 장수 |
|---|---|---|---|
| `visa_pcb1_normal_NN.jpg` | VisA `pcb1` 정상 이미지 | CC BY 4.0 | 14 |
| `visa_pcb1_anomaly_NN_<유형>.jpg` | VisA `pcb1` 이상 이미지 (유형: melt · missing · bent · scratch) | CC BY 4.0 | 15 |
| `deeppcb_NN_<원본번호>.jpg` | DeepPCB 시험 이미지 (단선·단락·쥐물림·돌기·잉여 구리·핀홀) | **연구용만** (아래 참고) | 6 |

## 출처 표기

- **VisA**: Zou, Y., Jeong, J., Pemula, L., Zhang, D., Dabeer, O. *SPot-the-Difference Self-Supervised Pre-training for Anomaly Detection and Segmentation.* ECCV 2022. 저장소 <https://github.com/amazon-science/spot-diff> · 데이터 라이선스 CC BY 4.0 (`LICENSE-VisA-CC-BY-4.0.txt`).
- **DeepPCB**: Tang, S., He, F., Huang, X., Yang, J. *Online PCB Defect Detector On A New PCB Defect Dataset.* 2019. 저장소 <https://github.com/tangsanli5201/DeepPCB> — README에 "You can only use this dataset for research purpose."라고 명시되어 있습니다.

## 사용 시 주의

- **DeepPCB 이미지(`deeppcb_*.jpg`)는 연구·시연 목적으로만** 쓰세요. 상업적 배포·서비스에 포함하려면 원저자 허락이 필요합니다. 상업 용도가 생기면 이 6장을 삭제하고 `demo.html`의 `SAMPLES`에서 `'D'` 항목을 제거하면 됩니다(나머지 기능은 그대로 동작).
- VisA 이미지는 출처 표기(위 인용)만 지키면 상업 이용도 가능합니다. 데모 화면(PCB 검사 하단 안내)과 README에도 출처를 적어 두었습니다.
- 데모의 **의심 영역 박스는 각 데이터셋의 정답(VisA 마스크, DeepPCB 주석)에서 계산한 값**입니다. 실제 PatchCore가 낸 결과가 아니며, 정상·불량 점수도 샘플 정답에 맞춰 정한 시연 값입니다. 파일명이 같으면(이 폴더의 파일을 PCB 검사 화면에 끌어다 놓으면) 같은 박스가 표시되고, 그 외 파일은 시연용 위치가 쓰입니다.
- 정답 유형(melt 등)은 데이터셋 라벨이며, 실제 API는 유형을 분류하지 않고 점수·영역만 제공할 예정입니다.

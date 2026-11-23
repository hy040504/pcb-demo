# CircuitEye (써킷아이) 데모

PCB 외관검사 웹 MVP의 UI 시안(단일 HTML)입니다. 실제 서비스가 아니며 모든 데이터는 가상입니다.

- 기본 화면: [index.html](https://hy040504.github.io/pcb-demo/)
- 리디자인 시안(같은 기능, 화면 스타일만 변경): [demo2.html](https://hy040504.github.io/pcb-demo/demo2.html)

## 샘플 이미지 출처

데모의 PCB 사진은 공개 데이터셋에서 고른 컬러 기판 사진입니다. 의심 영역 박스와 정상/불량 판정은 데이터셋 정답에 맞춘 **시연 값**이며 실제 AI 결과가 아닙니다.

| 용도 | 데이터셋 | 라이선스 |
|---|---|---|
| 정상 기판 (16장) | **PCB DSLR Dataset** — Christopher Pramerdorfer, Martin Kampel (TU Wien CVL). https://zenodo.org/records/3886553 (DOI 10.5281/zenodo.3886553) | CC BY 4.0 |
| 정상 기판 (8장) | **Roboflow Universe `pcb_component_detection_2`** v2 — https://universe.roboflow.com/project2-ccajc/pcb_component_detection_2 | CC BY 4.0 |
| 정상 기판 (6장) · 불량 시연 (24장) | **PKU-Market-PCB** — 베이징대 로보틱스 연구실. https://robotics.pkusz.edu.cn/resources/dataset/ (hyper.ai 미러에서 수령) | **라이선스 미확인** |

- PKU-Market-PCB는 실제 기판 사진 위에 불량을 **인위적으로 합성**한 데이터셋입니다. 실제 생산 불량 사진이 아닙니다.
- 이미지는 데모용으로 잘라서 줄인 사본입니다(내용 수정 없음). 파일별 출처·변경 내용: [`docs/assets/demo_images/SOURCES.md`](./docs/assets/demo_images/SOURCES.md)
- 권리자의 요청이 있거나 라이선스 문제가 확인되면 해당 이미지를 즉시 제거합니다.
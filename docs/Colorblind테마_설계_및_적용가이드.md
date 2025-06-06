# 👁️OpenWebUI Colorblind 테마 설계 및 적용 가이드

## **📌 설명**

**Colorblind 테마**는 단순한 색상 테마 변경이 아니라, **모든 사용자**가 정보에 동등하게 접근할 수 있도록 설계된 **고명도 대비 다크 테마입니**다.

저시력·색각 이상 사용자뿐 아니라 장시간 사용하는 일반 사용자에게도 피로를 줄이는 UX를 목표로 하였습니다.

---

## 🎯 테마 디자인 고려 사항

1. **접근성은 일부 사용자를 위한 것이 아닌, 모두를 위한 보편적 기준**
    - 저시력, 색각 이상 등 다양한 사용자를 고려하였습니다.
    - 색상의 인식보다, **밝기(명도) 차이에 의한 정보 구분**이 더 중요하다고 판단했습니다.
      
2. **WCAG AAA 등급을 준수하는 명도 대비**
    - WCAG의 핵심인 **텍스트와 배경 간의 대비를 확보했습니다.**
    - AAA 등급(7:1 이상)을 목표로 하여 다양한 시각 조건에서도 가독성을 유지하도록 디자인하였습니다.
    - [명도 체크 도구](https://www.getcolorlab.com/color-contrast-checker)
      
3. **배경 색상을 다크모드로 선택한 이유**
    - 어두운 환경에서 **눈부심을 줄이고**, 장시간 사용 시 **시각적 피로를 감소**시킬 수 있습니다. (2025년 국제 환경 연구 및 공중 보건 저널에 발표된 연구에 따르면, 사용자들이 다크 모드를 사용할 때 시각적 피로와 안구 건조 증상이 감소하는 경향이 있다는 연구가 있습니다. 또한, 깜박임 빈도와 동공 조절이 증가하여 시각적 피로가 감소하는 것으로 나타났습니다.[[1]](https://pubmed.ncbi.nlm.nih.gov/40283833/))
    - 다크모드는 **기기 배터리 절약**(OLED 디스플레이)과 **세련된 시각 스타일** 측면에서도 사용자 선호도가 높습니다.[[2]](https://arxiv.org/pdf/2409.10895)
    - 다만 다크모드에서도 **명도 대비가 충분히 확보되지 않으면** 오히려 인식성이 떨어지므로, 반드시 대비 기준을 우선하였습니다.

---

## 📐 WCAG AAA 명도 대비 기준

| 요소 | AAA 기준 대비 비율 |
| --- | --- |
| 일반 텍스트 | **7:1 이상** |
| 큰/굵은 텍스트 (18pt 이상 등) | **4.5:1 이상** |
| 아이콘 등 비텍스트 요소 | **3:1 이상** |
| 텍스트적 기능 겸할 경우 | **7:1 권장** |

---

## 🎨 기본 색상안

| 역할 | 색상 코드 | 설명 |
| --- | --- | --- |
| **기본 배경 색상** | `#0B1824` | 어두운 다크모드 배경, 눈부심 최소화, 95%의 색각이상자는 적록색약에 해당하며[[3]](https://www.kci.go.kr/kciportal/landing/article.kci?arti_id=ART001705754) 블루 베이스의 색상은 잘 인식되는 색상에 해당 |
| **레이어 색상** | `#263945` | 배경 대비 약 1.5:1텍스트 대비 약 12:1 이상 ※ 다크모드에서는 배경보다 소폭 밝은 색상으로 시각 계층 표현 |
| **텍스트 색상** | `#FFFFFF` | 레이어 및 배경과 모두 AAA 대비(7:1 이상) 만족 |

- 기본 배경 색상 - 레이어(왼쪽 탭) 색상

![배경_레이어](https://github.com/user-attachments/assets/f351f1de-fdc8-4f0c-a6bb-2b8966736e01)

- 기본 배경 색상- 텍스트 색상

![배경_텍스트](https://github.com/user-attachments/assets/321b6eea-d922-470c-b117-387bb676d062)

- 레이어 색상 - 텍스트 색상

![레이어_텍스트](https://github.com/user-attachments/assets/2df70df9-e951-4e8e-8052-41cf26c5fdab)

---

## 🟦 포인트 컬러 리디자인

| 역할 | 기존 색상 | 수정 색상 | AAA 대비 7:1 만족 여부 | 설명 |
| --- | --- | --- | --- | --- |
| 파랑색 | `#26ABED` | `#41A7FF` | ✅ 만족 (수정 후) | 대비 부족 → 수정 |
| 노랑색 | `#F5D742` | 유지 | ✅ 만족 | 유지 |
| 주황색 | `#F5D742` | 유지 | ✅ 만족 | 유지 |
| 보라색 | `#9E44C4` | `#EF6EF3` | ✅ 만족 (수정 후) | 대비 개선됨 |

- **파랑색** #26ABED(기존값) → #41a7ff(수정값) : 7:1 기준 만족하도록 수정 

![포인트(블루)](https://github.com/user-attachments/assets/880a3d44-68ca-4b97-afdb-e4c4e231d6d2)


- **노랑색** #f5d742 이미 만족

![포인트(옐로)](https://github.com/user-attachments/assets/6c0c255e-7c05-424f-af62-70ad556cb067)


- **주황색**

![image](https://github.com/user-attachments/assets/c0127f44-335f-446e-8f52-4b009a66e689)


- **보라색** #9E44C4(기존값) → #ef6ef3(수정값) : 7:1 기준 만족하도록 수정

![포인트(퍼플)](https://github.com/user-attachments/assets/fcac965c-31a0-47f0-9660-bd9c8611af69)

---

## 📸 Colorblind 테마 적용 화면

- 접속 화면
  <img width="1512" alt="접속화면" src="https://github.com/user-attachments/assets/27e6ab4c-fd0f-4b3b-b9b0-504cdfe52e83" />

- 기본 채팅 화면 UI
  <img width="1510" alt="채팅화면(기존)" src="https://github.com/user-attachments/assets/26515e0e-bd64-438b-b29e-a13e82c1b907" />

---

## 🧩 OpenWebUI 실제 적용 방식

- 설정 > 일반 > WebUI설정 > 테마에서 **👁️Colorblind** 테마 선택 시, 적용이 가능합니다.
  <img width="903" alt="KakaoTalk_20250523_222154903" src="https://github.com/user-attachments/assets/578de8ac-5402-4c40-9c1b-3e38c82ba77f" />

---

## 📚 참고 문헌 및 근거 자료

[1] Sengsoon P, Intaruk R. *Immediate Effects of Light Mode and Dark Mode Features on Visual Fatigue in Tablet Users*. Int J Environ Res Public Health. 2025 Apr 12;22(4):609. https://doi.org/10.3390/ijerph22040609

[2] Rahman, M. M., Sultana, S., & Hossain, M. S. *Dark Mode in e-Learning: Perception, Preferences, and Fatigue*. arXiv:2409.10895

[3] Lee, M. G., & Jin, W. *Improvements in the Color Universal Design of Mobile Web Sites for Colorblind People*. J. Korean Society of Design Science, 25(3), 118–127. https://doi.org/10.17280/jdd.2012.12.4.019

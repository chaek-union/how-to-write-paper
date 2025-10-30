# 2장. 논문 작성 시작하기

## 논문 작성의 순서

논문을 처음 쓰는 학생들이 가장 먼저 묻는 질문은 "어디서부터 시작해야 하나요?"다. 서론(Introduction)부터 써야 한다고 생각하는 사람이 많은데, 실제로는 그렇지 않다.

**추천하는 작성 순서:**

1. **논문 폴더 세팅** - 드롭박스에 논문 작성을 위한 폴더를 만들고, 지도교수와 공동저자들에게 공유한다.

2. **Main Figure 준비와 Results 작성** - Main Figure 2개 이상이 준비되면 Results 섹션을 작성하기 시작한다. 또한 Table S1 (샘플 메타 정보)를 작성한다. 

3. **전체 Figure 완성** - 모든 Main Figure를 완성한다. Figure 1개당 Results 서브섹션 1개를 작성하는 형태로 진행하며, Methods를 병렬적으로 작성한다.

4. **Introduction과 Discussion 작성** - 이 두 섹션은 서로 수미상관의 관계를 갖기 때문에 동시에 작성하는 것이 중요하다. Introduction에서 제기한 문제를 Discussion에서 해석하기 때문이다.

왜 이런 순서일까? 분석결과를 Figure로 만드는 것은 상대적으로 간단한 작업이다. Figure는 지도교수와 미팅을 하던 자료 (주로 슬라이드)에서 추출하여 작업을 할 수 있다. Figure를 바탕으로 각 Results 섹션을 쓴다. 몇개의 섹션을 쓰다보면, 자신이 발견한 것을 명확히 정리할 수 있다. 그 다음에 Introduction과 Discussion을 동시에 작성하면서 "왜 이 질문이 중요한가"를 설명하는 것이 더 쉽다. Figure가 먼저 완성되어야 Results를 쓸 수 있고, Results가 명확해야 Discussion을 논리적으로 전개할 수 있다.

---

## 논문 폴더 만들기

지금까지 실험을 하거나 데이터를 분석하면서 수많은 파일들을 만들어왔을 것이다. 그래프도 그려보고, 표도 만들어보고, 코드도 돌려보고... 그런데 막상 논문을 쓰려고 하면 어떤 파일이 최신 버전인지, 어떤 그림을 논문에 넣어야 할지 헷갈리기 시작한다. 

"어? 이 그래프 어디 있더라?"
"이게 최종 버전이었나? 아니면 저게 최종이었나?"
"공동저자들에게 보낸 파일이 어느 거였지?"

이런 상황을 방지하기 위해, 논문 작성을 본격적으로 시작하기 전에 반드시 해야 할 일이 있다. 바로 **논문 전용 폴더를 만드는 것**이다.

지금까지 작업했던 폴더들을 한번 떠올려보자. 아마도 이런 식으로 구성되어 있을 것이다:

```
(작업 폴더의 예시)

내_연구/
  ├── 실험1_20240101/
  ├── 실험1_재실험_20240215/
  ├── 분석_코드_최종/
  ├── 분석_코드_최종_진짜최종/
  ├── 그래프_모음/
  └── 참고자료/
```

이런 구조는 **작업 폴더(working folder)**로는 괜찮지만, 논문을 쓰기에는 적합하지 않다. 너무 많은 파일들이 섞여 있고, 최신 버전을 찾기 어려우며, 협업이 어렵다. 지도교수나 공동연구자가 "지금 현재 논문에 들어갈 Figure 1을 보여주세요"라고 하면 바로 보여줄 수 있는가? 논문 제출 시에는 Figure, Table, Supplementary 파일들을 정확하게 제출해야 하는데, 어떤 파일을 올려야 할지 헷갈린다.

파일 크기 문제도 있다. 작업 폴더에는 bam, vcf와 같은 파일이 있거나, fastq와 같은 raw data가 들어있다. 이런 시퀀싱 데이터는 수백 GB에 달할 수 있다. 이런 거대한 파일들을 논문 폴더에 넣으면 드롭박스 용량도 부족하고, 동기화도 느려진다. 논문 작성과 제출에는 이런 raw data가 직접적으로 필요하지 않다. 대신 분석 결과를 정리한 **summary data**(요약 데이터)만 있으면 된다.

그래서 우리는 **논문 폴더**와 **작업 폴더**를 명확히 구분해야 한다.

**작업 폴더(Working Folder)**는 실험과 분석을 하는 공간이다. 시행착오의 흔적이 모두 남아있고, 수많은 버전의 파일들이 존재하며, 본인만 이해할 수 있는 구조로 되어 있다. 크기가 큰 raw data(원시 데이터)를 보관하는 곳이기도 하다. 시퀀싱 리드 파일, 이미지 원본 파일 등이 여기에 있으며, 로컬 서버나 클라우드에 저장한다.

반면 **논문 폴더(Paper Folder)**는 논문에 들어갈 최종 결과물만 정리하는 공간이다. 현재 시점의 "최신 버전"만 보관하고, 누구나 한눈에 이해할 수 있는 명확한 구조를 가지고 있다. 협업자들과 공유하는 공간이며, 작고 정리된 summary data(요약 데이터)만 보관한다. 통계 결과 테이블, 그래프용 데이터 등이 여기에 해당하며, 드롭박스에 저장하여 실시간 동기화한다.

논문을 쓰고 저널에 제출할 때는 500GB의 raw data를 직접 제출하지 않는다. 대신 Figure와 Table에 들어간 **summary data**를 제출하고(보통 수 MB), raw data는 GEO, SRA 같은 공개 데이터베이스에 업로드한 후 논문에는 **accession number**만 적는다. 그러니까 논문 폴더에는 "논문 작성과 제출에 실제로 필요한 가벼운 파일들"만 넣으면 된다.

생각해보자. 주방에서 요리를 하는 공간(작업 폴더)과 손님에게 내놓는 식탁(논문 폴더)은 다르다. 주방은 어질러져 있어도 괜찮지만, 식탁은 깔끔하게 정리되어 있어야 한다. 마찬가지로 작업 폴더에는 수백 GB의 재료(raw data)가 있지만, 논문 폴더에는 완성된 요리(summary data와 Figure/Table)만 담겨있다.

---

## 논문 폴더의 기본 구조

이제 본격적으로 논문 폴더를 만들어보자.

### 폴더 이름 정하기

논문 폴더의 이름은 `paper_프로젝트명` 형식으로 짓는다. 예를 들면 `paper_ASD_WGS_2024`, `paper_SingleCell_Organoid`, `paper_RareVariant_Analysis` 같은 식이다. `paper_`로 시작하면 여러 폴더들 중에서 논문 폴더를 바로 찾을 수 있고, 프로젝트명을 넣으면 나중에 여러 논문을 쓸 때 구분이 쉽다. 간결하면서도 내용을 알아볼 수 있어야 한다. 리뷰 논문의 경우엔 `review_`로 폴더를 만든다. 

### 드롭박스(Dropbox)에 폴더 만들기

논문 폴더는 반드시 **드롭박스**에 만들어야 한다. 개인적인 취향이지만, 구글 드라이브는 동기화가 느리다. 드롭박스의 유연성을 따라가기 어렵다. 자동 백업으로 컴퓨터가 고장나도 파일이 안전하고, 버전 관리로 실수로 파일을 지워도 복구할 수 있다. 협업이 용이해서 지도교수나 공동연구자와 실시간으로 파일을 공유할 수 있으며, 학교, 집, 외부에서도 같은 파일에 접근할 수 있다.

드롭박스의 가장 큰 장점은 실시간 협업이다. 여러 사람이 동시에 같은 폴더를 보면서 작업할 수 있다. Figure 1을 업데이트하면, 지도교수의 컴퓨터에도 즉시 반영된다. 교수가 원고에 코멘트를 달면, 바로 확인할 수 있다. 공동연구자가 Table을 수정하면, 모든 팀원이 최신 버전을 볼 수 있다. 이메일로 파일을 주고받으면 "어? 제가 받은 게 최신 버전인가요?" 같은 혼란이 생기지만, 드롭박스를 사용하면 **항상 모든 사람이 같은 최신 버전**을 보게 된다.

드롭박스 폴더를 만들었다면, 지도교수, 공동 1저자, 특정 부분에 기여하는 공동연구자들을 초대하자. 폴더를 공유하는 방법은 간단하다. 드롭박스에서 해당 폴더를 우클릭하고 "공유(Share)"를 선택한 후, 초대하고 싶은 사람의 이메일 주소를 입력하고 "편집 가능(Can edit)" 권한으로 초대하면 된다. 이렇게 하면 파일을 업데이트할 때마다 자동으로 동기화되고, 모든 팀원이 협업할 수 있다.

### 기본 폴더 구조 만들기

논문 폴더 안에는 다음과 같은 하위 폴더들을 만든다:
```
paper_프로젝트명/
  ├── Figures/
  ├── Supplementary_Figures/
  ├── Supplementary_Tables/
  ├── Scripts/
  └── (나중에 만들 폴더: Data/)
```

각 폴더의 역할을 자세히 알아보자.

---

## Figures 폴더

이 폴더는 논문 본문에 들어갈 Figure들의 최신 버전을 보관하는 곳이다. 중요한 것은, 이 폴더는 "논문에 들어갈 현재 최신 버전의 Figure"를 저장하는 곳이라는 점이다. 분석 과정에서 나온 수많은 그래프들을 저장하는 곳이 **아니다**. 예를 들어, 10가지 다른 방법으로 데이터를 시각화해봤다면, 그 10개의 그래프는 작업 폴더에 있어야 한다. 그 중에서 "이게 논문에 들어갈 거야!"라고 결정한 하나만 이 Figures 폴더에 넣는 것이다. 파일 이름은 `Figure1_v1.pdf`, `Figure2_v1.pdf`, `Figure3_v1.pdf` 형식으로 버전 번호(`v1`, `v2`, `v3`...)를 붙여서 관리한다. 수정할 때마다 버전을 올리면, 나중에 "아, 이전 버전이 더 나았는데..."라고 생각될 때 돌아갈 수 있다.

실제 폴더 구조는 다음과 같다:
```
Figures/
  ├── Figure1_v3.pdf (← 현재 최신)
  ├── Figure2_v2.pdf (← 현재 최신)
  ├── Figure3_v1.pdf (← 현재 최신)
  └── old/
      ├── Figure1_v1.pdf
      ├── Figure1_v2.pdf
      └── Figure2_v1.pdf
```

현재 최신 버전은 Figures 폴더 바로 아래에 두고, 이전 버전들은 `old` 서브폴더에 보관한다. 이렇게 하면 폴더를 열었을 때 현재 사용 중인 Figure들만 바로 볼 수 있어서 명확하다. 누군가 "지금 시점에서 최신 버전의 Figure들을 달라"고 하면, Figures 폴더의 최상위에 있는 파일들을 주면 된다.

### Figures는 Scripts 폴더의 코드로 재현 가능해야 함

Figures 폴더에 들어가는 모든 Figure는 **Scripts 폴더에 저장된 코드를 실행하면 누구든지 똑같이 그릴 수 있어야 한다**. 이것이 재현 가능한 연구(reproducible research)의 핵심이다. 예를 들어 `Figures/Figure1_v3.pdf`는 `Scripts/Figure1.R`을 실행하면 만들어져야 하고, `Figures/Figure2_v2.pdf`는 `Scripts/Figure2.R`을 실행하면 만들어져야 한다. 이렇게 하면 리뷰어가 "Figure 1이 어떻게 만들어졌나요?"라고 물으면 코드를 보여줄 수 있고, 나중에 Figure를 수정해야 할 때 코드를 조금만 고치면 된다. 공동연구자가 Figure를 재생성할 수 있으며, 논문 출판 후 다른 연구자들이 방법론을 정확히 이해할 수 있다. Cell 이나 Nature 계열의 저널에서는 Code Reproducibility를 확인하기 위하여, 이와 같은 script 작성이 필수적이다. 

---

## Supplementary_Figures 폴더

본문에는 들어가지 않지만, Supplementary Information에 들어갈 Figure들을 보관한다. 본문에 들어가기엔 너무 자세하거나, 추가적인 분석 결과들이 여기에 들어간다. Supplementary Figure도 Main Figure와 **동일한 수준의 퀄리티**로 작성되어야 한다. "Supplementary"라고 해서 대충 만들면 안 된다. 리뷰어들은 Supplementary도 꼼꼼히 본다. Main Figure에는 논문의 핵심 메시지를 전달하는 Figure, 독자가 반드시 봐야 하는 결과, 논문의 스토리 전개에 필수적인 Figure가 들어간다. 반면 Supplementary Figure에는 Main Figure를 뒷받침하는 추가 증거, 통계적 검증 결과(예: QC plots, validation plots), 대체 분석 방법의 결과, 세부적인 기술적 디테일이 들어간다. 예를 들어 Main Figure 2가 "우리가 발견한 새로운 유전자 변이"라면, Supplementary Figure S2는 "해당 변이의 검증 실험 결과"가 될 수 있다. Supplementary Figure도 `Scripts/FigureS1.R` 같은 코드로 재현 가능해야 한다.

```
Supplementary_Figures/
  ├── FigureS1_v1.pdf (← 현재 최신)
  ├── FigureS2_v2.pdf (← 현재 최신)
  ├── FigureS3_v1.pdf (← 현재 최신)
  └── old/
      └── FigureS2_v1.pdf
```



---

## Supplementary_Tables 폴더

본문에는 들어가지 않지만, Supplementary Information에 들어갈 Table들을 보관한다. 우리가 작성하는 주제의 논문들에서는 Table을 Main manuscript에 거의 넣지 않고, **거의 모든 Table을 Supplementary에 정리**한다. Table은 공간을 많이 차지하고, Main manuscript는 Figure 중심으로 스토리를 전개하는 것이 더 효과적이며, 상세한 데이터는 Supplementary에서 제공하는 것이 일반적이기 때문이다. Supplementary Table의 전형적인 구성을 살펴보면, **Table S1**은 샘플 메타데이터로 거의 모든 논문에 필수다. 보통 여러 개의 Sheet로 구성되는데, Sheet 1에는 각 Sheet에 대한 설명을, Sheet 2 (Table S1A)에는 샘플 기본 정보(나이, 성별, 진단 등)를, Sheet 3 (Table S1B)에는 샘플 QC 정보(시퀀싱 depth, mapping rate 등)를, Sheet 4 (Table S1C)에는 필요시 추가 메타데이터를 넣는다. **Table S2**에는 주요 분석 결과(예: 통계적으로 유의한 유전자 목록)를, **Table S3**에는 추가 분석 결과(예: pathway enrichment 결과)를 넣는다. Supplementary Table도 `Scripts/TableS1.R` 같은 코드로 자동 생성되어야 한다.

```
Supplementary_Tables/
  ├── TableS1_v1.xlsx (← 현재 최신)
  ├── TableS2_v2.xlsx (← 현재 최신)
  ├── TableS3_v1.xlsx (← 현재 최신)
  └── old/
      └── TableS2_v1.xlsx
```

---

## Scripts 폴더

이 폴더는 Figure와 Table을 만드는 코드를 저장하는 곳으로, **논문의 재현성(reproducibility)을 보장하는 핵심 폴더**다. 많은 저널들이 요즘 재현성을 강조하면서 분석 코드 제출을 요구하며, 논문 심사에서도 매우 중요하게 다뤄진다. 주의할 점은, 여기에는 **모든 분석 코드**를 넣는 것이 아니라는 것이다. 실제 작업 폴더에서 데이터를 분석한 코드는 거기에 그대로 두면 된다. Scripts 폴더에 들어가는 코드는 Figure를 조합하고 레이아웃을 만드는 코드, Table을 최종 포맷으로 정리하고 엑셀로 저장하는 코드, 여러 분석 결과를 모아서 하나의 Figure/Table로 만드는 코드다.

```
Scripts/
  ├── Figure1.R          # Main Figure 1 생성
  ├── Figure2.R          # Main Figure 2 생성
  ├── Figure3.R          # Main Figure 3 생성
  ├── FigureS1.R         # Supplementary Figure S1 생성
  ├── FigureS2.R         # Supplementary Figure S2 생성
  ├── TableS1.R          # Supplementary Table S1 생성
  ├── TableS2.R          # Supplementary Table S2 생성
  └── utils.R            # 공통으로 사용하는 함수들
```

### 언제부터 Scripts 폴더를 사용하나?

답은 논문 작성 초기부터다. 많은 학생들이 "논문이 거의 다 끝나면 코드를 정리해야지"라고 생각하는데, 이것은 큰 실수다. Scripts 폴더의 코드는 **처음부터 작성하고 계속 업데이트**해야 한다. Figure를 수정할 때마다 코드만 조금 고치면 되고, 리뷰어가 수정을 요구하면 코드를 실행만 하면 되며, 나중에 "이 Figure를 어떻게 만들었더라?" 하고 헤맬 일이 없기 때문이다. 논문을 제출할 때는 Scripts 폴더의 코드를 GitHub에 업로드하거나 Zenodo에 업로드하여 DOI를 받는다. 그리고 논문의 "Data and Code Availability" 섹션에 다음과 같이 적는다:

> "All code used to generate figures and tables is available at GitHub (https://github.com/username/project) and archived at Zenodo (DOI: 10.5281/zenodo.1234567)."

이것은 논문 심사에서 매우 중요한 요소다. 리뷰어들은 재현 가능한 연구를 선호하며, 코드가 잘 정리되어 있으면 긍정적인 평가를 받는다.

### Scripts 예시 1: Multi-panel Figure 만들기 (cowplot 사용)

논문의 Figure는 보통 여러 개의 panel을 조합한 multi-panel plot이다. R의 `cowplot` 패키지를 사용하면 이를 쉽게 만들 수 있다. 다음은 Figure 1을 만드는 코드 예시다 (`Scripts/Figure1.R`):

```r
# Figure1.R
# Figure 1: Overview of study design and sample characteristics
# Author: [Your Name]
# Date: 2024-01-15

# Load libraries
library(ggplot2)
library(cowplot)
library(readr)

# Load data
sample_data <- read_csv("../Data/sample_metadata.csv")
seq_stats <- read_csv("../Data/sequencing_statistics.csv")

# Panel A: Study design schematic
# (이 부분은 보통 일러스트레이터로 만들어서 이미지 파일로 불러옴)
panel_a <- ggdraw() + 
  draw_image("../Data/study_design.png")

# Panel B: Sample distribution by diagnosis
panel_b <- ggplot(sample_data, aes(x = diagnosis, fill = diagnosis)) +
  geom_bar() +
  theme_cowplot() +
  labs(x = "Diagnosis", y = "Number of samples")

# Panel C: Sequencing depth distribution
panel_c <- ggplot(seq_stats, aes(x = mean_depth)) +
  geom_histogram(bins = 30, fill = "steelblue") +
  theme_cowplot() +
  labs(x = "Mean sequencing depth", y = "Count")

# Combine panels
figure1 <- plot_grid(
  panel_a, panel_b, panel_c,
  labels = c("A", "B", "C"),
  ncol = 3,
  rel_widths = c(1, 1, 1)
)

# Save
ggsave("../Figures/Figure1_v1.pdf", 
       figure1, 
       width = 12, 
       height = 4, 
       dpi = 300)
```

이 코드를 실행하면 `Figures/Figure1_v1.pdf`가 생성된다. 나중에 Figure를 수정하고 싶으면 코드를 고치고 다시 실행하면 된다.

### Scripts 예시 2: Table S1 만들기

Table S1 (샘플 메타데이터)는 거의 모든 논문에 필수다. 이것도 코드로 자동 생성해야 한다. 다음은 Table S1을 만드는 코드 예시다 (`Scripts/TableS1.R`):

```r
# TableS1.R
# Supplementary Table S1: Sample metadata
# Author: [Your Name]
# Date: 2024-01-15

# Load libraries
library(openxlsx)
library(readr)
library(dplyr)

# Create a new workbook
wb <- createWorkbook()

# Sheet 1: Description
addWorksheet(wb, "Description")
description <- data.frame(
  Sheet = c("Table S1A", "Table S1B", "Table S1C"),
  Description = c(
    "Basic sample information (age, sex, diagnosis)",
    "Quality control metrics (sequencing depth, mapping rate)",
    "Additional metadata (ethnicity, medication)"
  )
)
writeData(wb, "Description", description)

# Sheet 2: Table S1A - Basic information
addWorksheet(wb, "Table S1A")
basic_info <- read_csv("../Data/sample_basic_info.csv") %>%
  select(sample_id, age, sex, diagnosis, batch)
writeData(wb, "Table S1A", basic_info)

# Sheet 3: Table S1B - QC metrics
addWorksheet(wb, "Table S1B")
qc_metrics <- read_csv("../Data/sample_qc_metrics.csv") %>%
  select(sample_id, mean_depth, mapping_rate, duplication_rate)
writeData(wb, "Table S1B", qc_metrics)

# Sheet 4: Table S1C - Additional metadata
addWorksheet(wb, "Table S1C")
additional_meta <- read_csv("../Data/sample_additional_metadata.csv") %>%
  select(sample_id, ethnicity, medication, family_history)
writeData(wb, "Table S1C", additional_meta)

# Save
saveWorkbook(wb, "../Supplementary_Tables/TableS1_v1.xlsx", overwrite = TRUE)
```

이 코드를 실행하면 `Supplementary_Tables/TableS1_v1.xlsx`가 생성된다.

---

## 원고 파일 만들기

논문 폴더를 만들었다면, 이제 실제로 글을 쓸 원고 파일을 만들어야 한다.

### Main Manuscript 파일

Main manuscript는 세 개의 분리된 워드 파일로 작성한다:

1. Manuscript_[프로젝트명]_Main_v1.docx - Title, Abstract, Introduction, Results, Discussion, References를 포함한다.
2. Manuscript_[프로젝트명]_Methods_v1.docx - Methods 섹션만 별도로 작성한다. Methods는 보통 매우 길고 기술적이어서, Main manuscript와 분리하는 것이 편리하다.
3. Supplementary_Information_v1.docx - Supplementary Figure legends, Supplementary Table legends, 추가적인 Methods 등을 포함한다.
왜 세 개로 분리할까? Main manuscript가 너무 길면 편집이 어렵고, Methods는 기술적 디테일이 많아서 분리하는 것이 깔끔하며, 저널 제출 시 보통 Main manuscript와 Supplementary를 별도 파일로 제출하기 때문이다. 예를 들어, `paper_ASD_WGS_2024` 폴더에는 다음과 같은 파일들이 있어야 한다:

```
paper_ASD_WGS_2024/
  ├── Manuscript_ASD_WGS_Main_v1.docx
  ├── Manuscript_ASD_WGS_Methods_v1.docx
  ├── Supplementary_Information_v1.docx
  └── ...
```

### 버전 관리 규칙

원고 파일도 버전 관리를 해야 한다. 파일명에 버전 번호를 붙이는 방식은 다음과 같다:

**기본 버전 형식**: `v1.0`, `v1.1`, `v1.2`, ...
- 첫 번째 숫자(1)는 major version - 큰 변경이 있을 때 올린다
- 두 번째 숫자(0, 1, 2)는 minor version - 작은 수정이 있을 때 올린다

**실제 예시**:
```
Manuscript_Main_v1.0.docx (초안)
Manuscript_Main_v1.1.docx (교수님 코멘트 반영)
Manuscript_Main_v1.2.docx (공동저자 코멘트 반영)
Manuscript_Main_v2.0.docx (구조를 크게 바꿈)
Manuscript_Main_v2.1.docx (리뷰어 코멘트 반영)
```

**이전 버전은 old 폴더로**: 새 버전을 만들 때마다 이전 버전은 `old/` 폴더로 옮긴다. 이렇게 하면 논문 폴더의 최상위에는 현재 작업 중인 최신 버전만 보인다.

---

## EndNote 라이브러리 관리

논문을 쓸 때 reference 관리는 매우 중요하다. 우리는 EndNote를 사용한다. 35만원 가량 되는 프로그램을 고려대에서는 무료로 제공한다...  

### EndNote 라이브러리 파일 위치

EndNote 라이브러리는 두 개의 파일로 구성된다:
- `.enl` 파일 (EndNote 라이브러리 파일)
- `.Data` 폴더 (PDF 파일들이 저장된 폴더)

이 두 파일은 **반드시 논문 폴더에 함께 있어야 한다**. 예를 들면:
```
paper_ASD_WGS_2024/
  ├── References_ASD_WGS.enl
  ├── References_ASD_WGS.Data/
  │   ├── PDF/
  │   │   ├── paper1.pdf
  │   │   ├── paper2.pdf
  │   │   └── ...
  └── ...
```

EndNote 라이브러리를 논문 폴더에 두면 여러 가지 장점이 있다. 다른 저자들도 같은 reference를 볼 수 있고, 드롭박스로 자동 백업되며, 논문 제출 시 필요한 모든 파일이 한 곳에 모여 있다.

### EndNote 사용 팁

**Cite While You Write**: 워드에서 글을 쓸 때 EndNote의 "Insert Citation" 기능을 사용한다. 이렇게 하면 reference가 자동으로 formatting되고, 나중에 저널을 바꿔도 reference style을 쉽게 변경할 수 있다.

**Reference 정리**: 논문을 쓰면서 계속 새로운 reference를 추가하게 된다. EndNote 라이브러리를 깔끔하게 유지하려면, 각 reference에 Keywords를 추가하고(예: "autism", "WGS", "de novo"), Rating을 매기고(중요한 논문은 5점), Notes에 간단한 메모를 추가한다(예: "이 논문은 우리 Discussion에서 인용").

---

## 공동저자와 원고 공유하기

논문 폴더를 만들고 원고를 작성하기 시작했다면, 적절한 시점에 공동저자들과 공유해야 한다.

### 언제 공유할까?

**너무 이른 시점**: 초안도 없이 빈 폴더만 공유하면 공동저자들이 뭘 해야 할지 모른다.
**적절한 시점**: Main Figure 2개 이상이 완성되고, Results 초안이 어느 정도 작성되었을 때다. 이 시점이면 논문의 방향이 명확하고, 공동저자들이 구체적인 피드백을 줄 수 있다.
**너무 늦은 시점**: 논문을 거의 다 쓰고 제출 직전에 공유하면, 공동저자들의 피드백을 반영할 시간이 부족하다.

### 워드 파일의 Track Changes 기능

공동저자들과 원고를 주고받을 때는 **Track Changes** 기능을 반드시 사용해야 한다.

**Track Changes란?**: 워드의 기능으로, 문서의 모든 수정사항(추가, 삭제, 변경)을 자동으로 기록한다. 누가 언제 무엇을 바꿨는지 모두 보인다.

**Track Changes 켜는 방법**: 
- 워드 상단 메뉴에서 Review → Track Changes 클릭
- 이제 수정하는 모든 내용이 자동으로 tracking된다

**왜 필요할까?**: 
- 누가 무엇을 바꿨는지 명확하다
- 수정사항을 Accept 또는 Reject할 수 있다
- 수정 전 원본을 볼 수 있다
- 여러 사람의 피드백을 효율적으로 통합할 수 있다

### 본인(1저자)이 원고를 업데이트할 때

1저자로서 원고를 수정하고 새 버전을 만들 때의 규칙이다.

**버전 번호 올리기**

수정할 때마다 버전을 올린다. 예를 들어:
```
Manuscript_Main_v2.6.docx (공동저자에게 보낸 버전)

         ↓ (피드백 받고 수정)

Manuscript_Main_v2.7.docx (새 버전)
```

minor version (두 번째 숫자)을 하나씩 올린다. 작은 수정은 v2.6.1, v2.6.2 같은 식으로 세 번째 숫자를 사용할 수도 있다.

**Track Changes의 수정사항 Accept/Reject**

공동저자가 Track Changes로 수정한 파일을 받으면, 각 수정사항을 검토하고 Accept(수락) 또는 Reject(거절)한다. 모든 수정사항을 처리했으면, **새 버전을 만들 때 Track Changes를 모두 Accept**한다. 그래야 다음 버전에서 깨끗한 상태로 시작할 수 있다. 새로운 버전을 공유할 때 이전 버전의 수정사항이 그대로 남아있으면 어떤 것이 새로운 수정인지 알 수 없고, 파일이 지저분해 보이며, 검토자가 혼란스러워한다.

**해결된 코멘트 삭제하기**

원고를 버전 업하여 회람할 때, **반드시 해결된 코멘트는 삭제**한다. 예를 들어 다른 저자가 v2.0에 "이 문장 불명확함. 다시 써주세요"라는 코멘트를 달았고, 그 문장을 수정했다면, v2.1을 만들 때 그 코멘트를 삭제한다. 남겨두는 코멘트는 아직 해결하지 못한 문제, 논의가 더 필요한 부분, 다음 버전에서 다룰 예정인 사항이다. 이렇게 하면 검토자가 "아직 처리되지 않은 것"만 보게 되어 효율적이다.

**파일명에서 이니셜 삭제**

이전 버전에서 누군가 수정해준 파일명에 이니셜이 있다면, 새 버전을 만들 때 이니셜을 삭제한다. 예시:
```
Manuscript_Main_v2.6_JYA.docx (다른 저자가 수정한 버전)
         
         ↓ (수정사항 반영 후)

Manuscript_Main_v2.7.docx (1저자가 정리한 새 버전)
```

이렇게 하면 "이니셜 없는 파일 = 공식 최신 버전"이라는 것이 명확해진다.

### 다른 사람의 원고를 수정할 때 (공동연구자, 공동저자의 경우)

반대로, 누군가의 원고를 검토하고 수정할 때는 이렇게 한다.

**Track Changes 반드시 켜기**

절대 규칙은 다른 사람의 원고를 수정할 때는 반드시 워드의 **Review → Track Changes**를 켜야 한다는 것이다. Track Changes를 켜지 않고 직접 수정하면 원저자가 무엇이 바뀌었는지 알 수 없고, 원저자가 동의하지 않는 수정도 강제로 들어가며, 논의의 여지가 없어진다.

**파일명에 본인 이니셜 추가**

원고를 수정한 후 저장할 때는 버전을 한 단계 올리고(예: v2.6 → v2.6.1), 파일명 맨 뒤에 **본인 이니셜을 추가**한다. 예시:
```
받은 파일: Manuscript_Main_v2.6.docx
수정 후: Manuscript_Main_v2.6.1_HJL.docx
```

이렇게 하면 누가 수정했는지 명확하고, 원본 파일은 보존되며, 1저자가 여러 사람의 피드백을 쉽게 통합할 수 있다.

**코멘트 적극 활용**

수정 외에 의견을 남길 때는 코멘트를 사용한다. "이 부분 데이터가 정확한가요?", "이 문장을 이렇게 바꾸는 건 어떨까요?", "Figure 2를 여기로 옮기면 어떨까요?" 같은 경우다. 코멘트는 제안이고, Track Changes는 수정이다. 둘을 적절히 섞어서 사용하자.

### 실전 예시: 버전 관리 워크플로우

현실적인 상황을 예로 들어보자.

**1단계**: 학생(1저자)이 초안을 작성한다
```
Manuscript_Main_v1.0.docx → 공동저자께 공유
```

**2단계**: 다른 저자가 수정한다
```
Manuscript_Main_v1.0.docx (받음)
→ (Track Changes로 수정)
→ Manuscript_Main_v1.0.1_JYA.docx (저장 후 학생에게 공유)
```

**3단계**: 학생이 수정사항을 반영한다
```
Manuscript_Main_v1.0.1_JYA.docx (받음)
→ (수정사항 검토 → Accept/Reject → 추가 수정)
→ Manuscript_Main_v1.1.docx (정리 완료, 다시 공동저자께 공유)
```

**4단계**: 공동연구자도 검토를 요청한다
```
Manuscript_Main_v1.1.docx → 공동연구자 A, B에게 공유
```

**5단계**: 두 공동연구자가 각각 수정한다
```
공동연구자 A: Manuscript_Main_v1.1.1_KSM.docx
공동연구자 B: Manuscript_Main_v1.1.2_LHJ.docx
```

**6단계**: 학생이 모든 피드백을 통합한다
```
두 파일을 모두 검토 → 수정사항 반영 → 새 버전 생성
→ Manuscript_Main_v1.2.docx (통합 완료)
```

이런 식으로 계속 순환하면서 논문이 발전한다.

---

## 실전 예시: 논문 폴더 완성본

자, 이제 모든 것을 종합해서 완성된 논문 폴더가 어떻게 생겼는지 보자:
```
paper_ASD_WGS_2024/
  │
  ├── Manuscript_ASD_WGS_Main_v3.docx (← 현재 작업 중)
  ├── Manuscript_ASD_WGS_Methods_v2.docx (← 현재 작업 중)
  ├── Supplementary_Information_v1.docx (← 현재 작업 중)
  ├── References_ASD_WGS.enl
  ├── References_ASD_WGS.Data/
  │
  ├── old/
  │   ├── Manuscript_ASD_WGS_Main_v1.docx
  │   ├── Manuscript_ASD_WGS_Main_v2.docx
  │   └── Manuscript_ASD_WGS_Methods_v1.docx
  │
  ├── Figures/
  │   ├── Figure1_v3.pdf (← 현재 최신)
  │   ├── Figure2_v2.pdf (← 현재 최신)
  │   ├── Figure3_v1.pdf (← 현재 최신)
  │   ├── Figure4_v1.pdf (← 현재 최신)
  │   └── old/
  │       ├── Figure1_v1.pdf
  │       ├── Figure1_v2.pdf
  │       └── Figure2_v1.pdf
  │
  ├── Supplementary_Figures/
  │   ├── FigureS1_v1.pdf (← 현재 최신)
  │   ├── FigureS2_v2.pdf (← 현재 최신)
  │   ├── FigureS3_v1.pdf (← 현재 최신)
  │   └── old/
  │       └── FigureS2_v1.pdf
  │
  ├── Supplementary_Tables/
  │   ├── TableS1_v1.xlsx (← 현재 최신)
  │   ├── TableS2_v2.xlsx (← 현재 최신)
  │   ├── TableS3_v1.xlsx (← 현재 최신)
  │   └── old/
  │       └── TableS2_v1.xlsx
  │
  └── Scripts/
      ├── Figure1.R
      ├── Figure2.R
      ├── Figure3.R
      ├── FigureS1.R
      ├── FigureS2.R
      ├── TableS1.R
      ├── TableS2.R
      └── utils.R
```

이 폴더를 보면 어떤 파일이 최신인지 한눈에 알 수 있고, Figure와 Table이 몇 개인지 명확하며, 누구에게나 공유하기 쉽고, 저널 제출 준비가 간단하다.

---

## 학생들이 하는 흔한 실수들

### 파일 관리 실수

**작업 폴더와 논문 폴더를 구분하지 않음**: 논문 폴더에 테스트 코드, 실패한 분석 결과, 중간 산물들을 모두 넣으면 폴더가 금방 지저분해진다. 작업 폴더와 논문 폴더를 엄격히 분리하자. 논문 폴더에는 "현재 논문에 들어갈 것"만 넣고, 작업 과정의 모든 것은 작업 폴더에 남겨두고 최종 결과물만 논문 폴더로 복사한다.

**"final"이라는 단어 사용**: 파일 이름을 `Figure1_final.pdf`, `Figure1_final2.pdf`, `Figure1_final_final.pdf`로 짓는 것도 문제다. 항상 `_v1`, `_v2`, `_v3` 형식으로 버전을 관리하자. "final"이라는 단어는 절대 쓰지 말자. 논문에서 "final"은 없다. 항상 수정이 필요하니까.

### 초기 준비 실수

**Table S1을 나중에 만들려고 함**: 논문을 거의 다 쓰고 나서 Table S1 (샘플 메타데이터)을 만들려고 하면, 샘플 정보를 다시 정리해야 하고 때로는 분석을 다시 해야 할 수도 있다. 논문 작성을 시작하는 첫날 `TableS1_v1.xlsx`를 만들자. 처음에는 불완전해도 괜찮다. 논문을 쓰면서 계속 업데이트하면 된다.

**드롭박스를 사용하지 않음**: 로컬 컴퓨터에만 파일을 저장하면, 다른 저자들에게 파일을 매번 이메일로 보내야 하고 버전 관리가 엉망이 된다. 논문 폴더를 만들자마자 드롭박스에 올리고 지도교수와 공유하자. 그러면 파일을 업데이트할 때마다 자동으로 동기화되고, 다른 저자들은 항상 최신 버전을 볼 수 있다.

**모든 것을 하나의 파일에 작성**: Title부터 References, Methods, Supplementary까지 모든 것을 하나의 파일에 쓰면 파일이 너무 길어지고 편집이 어렵다. Main manuscript, Methods, Supplementary를 세 개의 분리된 파일로 작성하자. 이렇게 하면 각 부분에 집중할 수 있고, 나중에 저널 제출 시에도 편리하다.

### 협업 실수

**Track Changes를 사용하지 않음**: 다른 저자가 Track Changes 없이 원고를 직접 고쳐서 보내면, 1저자는 무엇이 바뀌었는지 알 수 없다. 협업 초기에 모든 팀원에게 "반드시 Track Changes를 켜고 수정해주세요"라고 명확히 안내한다.

**동시에 같은 파일 편집**: 여러 저자가 동시에 같은 파일을 받아서 수정하면 버전 충돌이 발생할 수 있다. 한 사람씩 순차적으로 검토하도록 요청하거나, 서로 다른 부분(예: 한 사람은 Introduction, 다른 사람은 Discussion)을 맡기거나, 명확히 다른 버전 번호를 부여한다(v1.0.1_A, v1.0.2_B).

**해결된 코멘트를 삭제하지 않음**: 이미 수정한 부분의 코멘트를 삭제하지 않으면 파일에 수십 개의 코멘트가 쌓여서 혼란스럽다. 새 버전을 만들 때마다 해결된 코멘트는 과감히 삭제하자. 필요하면 "v1.1에서 수정 완료" 같은 메모를 남기고 삭제한다.

**"최종 버전" 여러 개**: 여러 사람이 각자 "최종 버전"이라고 생각하는 파일을 만들면, 어떤 것이 진짜인지 알 수 없다. 처음부터 "1저자가 공식 버전을 관리한다"는 규칙을 명확히 하고, 이니셜 없는 파일만 공식 버전으로 인정한다.

---

## 자주 묻는 질문

### 언제 논문 폴더를 만들어야 하나?

지금 당장! 많은 학생들이 "분석이 다 끝나면 논문 폴더를 만들어야지"라고 생각한다. 하지만 이것은 잘못된 생각이다. **논문 폴더는 분석을 시작할 때 함께 만들어야 한다.**

분석하면서 동시에 정리할 수 있다. 좋은 결과가 나올 때마다 바로 논문 폴더에 정리하면, 나중에 "어떤 결과가 어디 있더라?" 하고 헤맬 일이 없다. Table S1을 먼저 만들 수 있다. Supplementary Table S1 (샘플 메타데이터)은 초반에 만들어야 한다. Methods를 바로 작성할 수 있다. 실험이나 분석을 하자마자 Methods를 쓰면, 세부 사항을 잊어버리지 않는다. "음... 6개월 전에 이 분석을 어떻게 했더라?" 하고 기억을 더듬을 필요가 없다. 논문 쓰기가 덜 막막하다. 논문 폴더가 미리 준비되어 있고, Table S1과 Methods가 어느 정도 작성되어 있으면, 나중에 본격적으로 논문을 쓸 때 심리적 부담이 훨씬 줄어든다.

### 어느 시점에 저널을 결정하는 것이 좋을까?

연구를 시작할 때 지도교수와 논의하면 좋다. Figure가 2개 정도 준비되면, 지도교수가 "이제 논문을 쓸 때가 되었다"라고 할 텐데, 그때 타겟 저널을 지도교수와 상의하고 대략 정하는 것이 좋다. 타겟 저널이 정해지면 그 저널의 Author Guidelines를 확인하고, Figure 개수 제한, 단어 수 제한, 포맷 요구사항 등을 미리 파악할 수 있다.

### 논문 전체 분량은 어떤 기준으로 정하나?

분량은 투고하고자 하는 저널의 가이드라인에서 확인하고, 그 분량에 맞춰서 작성한다. 다만 분량을 맞춰서 작성한다고 생각하지 말고, 우선은 글을 쓰자. 이후에 문장을 교정하고 재배치하면서 분량을 조절하면 된다. 처음부터 "3,000단어 안에 써야 해"라고 생각하면 글쓰기가 위축된다. 먼저 하고 싶은 말을 다 쓰고, 나중에 다듬자.

### Figure를 먼저 그리고 본문을 쓰는 것이 효율적인가, 아니면 본문을 먼저 작성한 뒤 Figure를 그리는 것이 좋을까?

일반적으로는 Figure를 작성하고, 이후에 본문을 쓰는 것이 좋다. Figure가 있으면 Results를 쓸 때 "이 Figure는 이런 것을 보여준다"라고 설명할 수 있기 때문이다. 그러나 본문을 먼저 스토리처럼 작성하고, 그 흐름에 맞춰 결과를 배치하면서 Figure를 작성할 수도 있다. 그 과정에서 본문의 내용을 정확하게 기입하며 수정할 수 있다. 본인에게 맞는 방식을 연습해보는 것이 좋다.

### Figure 작업 시 사용하는 툴(예: Illustrator)은 새로 배워야 하나?

우리 연구실은 일러스트레이터로 Figure를 작업한다. 일러스트레이터 작업 능력은 필수다. R이나 Python으로 그래프를 그린 후, 일러스트레이터에서 레이아웃을 조정하고 레이블을 추가하는 방식으로 작업한다. 처음에는 어렵게 느껴지지만, 몇 번 연습하면 금방 익숙해진다.

### Main Figure와 Supplementary Figure를 구분할 때, 어떤 기준으로 배치 결정을 하나?

처음에는 Main Figure를 염두에 두고 Figure를 준비한다. 그렇게 그리다 보면, 스토리 전개상 우선순위가 높은 Figure들이 선별된다. 그렇게 주전과 후보 선수를 선별해 가며 Figure를 그리면 된다. 논문의 핵심 메시지를 전달하는 데 꼭 필요한 Figure는 Main Figure로, 추가적인 검증이나 세부 사항을 보여주는 Figure는 Supplementary Figure로 분류한다.

---

이제 논문 작성을 시작할 준비가 되었다. 논문 폴더를 만들고, 드롭박스에 올리고, 지도교수와 공유하자. 그리고 Table S1을 만드는 것부터 시작하자. 작은 한 걸음이 첫 논문으로 이어질 것이다.
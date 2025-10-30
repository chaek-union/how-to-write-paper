# 2장. 논문 작성 시작하기

## 논문 작성의 순서

논문을 처음 쓰는 학생들이 가장 먼저 묻는 질문은 "어디서부터 시작해야 하나요?"입니다. 많은 사람들이 Introduction부터 써야 한다고 생각하지만, 실제로는 그렇지 않습니다.

**추천하는 작성 순서:**

1. **논문 폴더 세팅** - 드롭박스에 폴더 구조를 만들고 공동저자들과 공유합니다.

2. **Main Figure 준비와 Results 작성** - Main Figure 2개 이상이 준비되면 Results 섹션을 작성하기 시작합니다. 또한 Table S1 (샘플 메타 정보)를 작성합니다. 

3. **전체 Figure 완성** - 모든 Main Figure를 완성합니다. Figure 1개당 Results 서브섹션 1개를 작성하는 형태로 진행하며, Methods를 병렬적으로 작성합니다.

4. **Introduction과 Discussion 작성** - 이 두 섹션은 서로 수미상관의 관계를 갖기 때문에 동시에 작성하는 것이 중요합니다. Introduction에서 제기한 문제를 Discussion에서 해석합니다.

왜 이런 순서일까요? 분석결과를 Figure로 만드는 것은 상대적으로 간단한 작업입니다. 그것을 바탕으로 각 Results 섹션을 쓰면 자신이 발견한 것을 명확히 정리할 수 있습니다. 그 다음에 Introduction과 Discussion을 동시에 작성하면서 "왜 이 질문이 중요한가"를 설명하는 것이 더 쉽습니다. Figure가 먼저 완성되어야 Results를 쓸 수 있고, Results가 명확해야 Discussion을 논리적으로 전개할 수 있습니다.

---

## 논문 폴더 만들기

여러분은 지금까지 실험을 하거나 데이터를 분석하면서 수많은 파일들을 만들어왔을 것입니다. 그래프도 그려보고, 표도 만들어보고, 코드도 돌려보고... 그런데 막상 논문을 쓰려고 하면 어떤 파일이 최신 버전인지, 어떤 그림을 논문에 넣어야 할지 헷갈리기 시작합니다. 

"어? 이 그래프 어디 있더라?"
"이게 최종 버전이었나? 아니면 저게 최종이었나?"
"공동저자들에게 보낸 파일이 어느 거였지?"

이런 상황을 방지하기 위해, 논문 작성을 본격적으로 시작하기 전에 반드시 해야 할 일이 있습니다. 바로 **논문 전용 폴더를 만드는 것**입니다.

여러분이 지금까지 작업했던 폴더들을 한번 떠올려보세요. 아마도 이런 식으로 구성되어 있을 겁니다:
```
내_연구/
  ├── 실험1_20240101/
  ├── 실험1_재실험_20240215/
  ├── 분석_코드_최종/
  ├── 분석_코드_최종_진짜최종/
  ├── 그래프_모음/
  └── 참고자료/
```

이런 구조는 **작업 폴더(working folder)**로는 괜찮지만, 논문을 쓰기에는 적합하지 않습니다. 너무 많은 파일들이 섞여 있고, 최신 버전을 찾기 어려우며, 협업이 어렵습니다. 지도교수나 공동연구자가 "지금 현재 논문에 들어갈 Figure 1을 보여주세요"라고 하면 바로 보여줄 수 있나요? 논문 제출 시에는 Figure, Table, Supplementary 파일들을 정확하게 제출해야 하는데, 어떤 파일을 올려야 할지 헷갈립니다.

파일 크기 문제도 있습니다. 작업 폴더에는 raw data(원시 데이터)가 들어있습니다. 예를 들어 시퀀싱 데이터는 수백 GB에 달할 수 있죠. 이런 거대한 파일들을 논문 폴더에 넣으면 드롭박스 용량도 부족하고, 동기화도 느려집니다. 논문 작성과 제출에는 이런 raw data가 직접적으로 필요하지 않습니다. 대신 분석 결과를 정리한 **summary data**(요약 데이터)만 있으면 됩니다.

그래서 우리는 **논문 폴더**와 **작업 폴더**를 명확히 구분해야 합니다.

**작업 폴더(Working Folder)**는 실험과 분석을 하는 공간입니다. 시행착오의 흔적이 모두 남아있고, 수많은 버전의 파일들이 존재하며, 본인만 이해할 수 있는 구조로 되어 있습니다. 크기가 큰 raw data(원시 데이터)를 보관하는 곳이기도 합니다. 시퀀싱 raw reads, 이미지 원본 파일 등이 여기에 있으며, 로컬 서버나 외장하드에 저장합니다.

반면 **논문 폴더(Paper Folder)**는 논문에 들어갈 최종 결과물만 정리하는 공간입니다. 현재 시점의 "최신 버전"만 보관하고, 누구나 한눈에 이해할 수 있는 명확한 구조를 가지고 있습니다. 협업자들과 공유하는 공간이며, 작고 정리된 summary data(요약 데이터)만 보관합니다. 통계 결과 테이블, 그래프용 데이터 등이 여기에 해당하며, 드롭박스에 저장하여 실시간 동기화합니다.

데이터 크기 차이가 왜 중요한지 생각해보세요. 여러분이 whole-genome sequencing 데이터를 분석했다면, 작업 폴더에는 500GB의 FASTQ 파일, BAM 파일 등이 로컬 서버에 보관되어 있습니다. 하지만 논문 폴더에는 2MB의 variant 통계 테이블, Figure용 summary data만 드롭박스에 보관하면 됩니다.

논문을 쓰고 저널에 제출할 때는 500GB의 raw data를 직접 제출하지 않습니다. 대신 Figure와 Table에 들어간 **summary data**를 제출하고(보통 수 MB), raw data는 GEO, SRA 같은 공개 데이터베이스에 업로드한 후 논문에는 **accession number**만 적습니다. 그러니까 논문 폴더에는 "논문 작성과 제출에 실제로 필요한 가벼운 파일들"만 넣으면 됩니다.

생각해보세요. 주방에서 요리를 하는 공간(작업 폴더)과 손님에게 내놓는 식탁(논문 폴더)은 다릅니다. 주방은 어질러져 있어도 괜찮지만, 식탁은 깔끔하게 정리되어 있어야 하죠. 마찬가지로 작업 폴더에는 수백 GB의 재료(raw data)가 있지만, 논문 폴더에는 완성된 요리(summary data와 Figure/Table)만 담겨있습니다.

---

## 논문 폴더의 기본 구조

이제 본격적으로 논문 폴더를 만들어봅시다.

### 폴더 이름 정하기

논문 폴더의 이름은 `paper_프로젝트명` 형식으로 짓습니다. 예를 들면 `paper_ASD_WGS_2024`, `paper_SingleCell_Organoid`, `paper_RareVariant_Analysis` 같은 식입니다. `paper_`로 시작하면 여러 폴더들 중에서 논문 폴더를 바로 찾을 수 있고, 프로젝트명을 넣으면 나중에 여러 논문을 쓸 때 구분이 쉽습니다. 간결하면서도 내용을 알아볼 수 있어야 합니다.

### 드롭박스(Dropbox)에 폴더 만들기

논문 폴더는 반드시 **드롭박스**에 만들어야 합니다. 자동 백업으로 컴퓨터가 고장나도 파일이 안전하고, 버전 관리로 실수로 파일을 지워도 복구할 수 있습니다. 협업이 용이해서 지도교수나 공동연구자와 실시간으로 파일을 공유할 수 있으며, 학교, 집, 외부에서도 같은 파일에 접근할 수 있습니다.

드롭박스의 가장 큰 장점은 실시간 협업입니다. 여러 사람이 동시에 같은 폴더를 보면서 작업할 수 있습니다. 여러분이 Figure 1을 업데이트하면, 지도교수의 컴퓨터에도 즉시 반영됩니다. 교수가 원고에 코멘트를 달면, 여러분은 바로 확인할 수 있습니다. 공동연구자가 Table을 수정하면, 모든 팀원이 최신 버전을 볼 수 있습니다. 이메일로 파일을 주고받으면 "어? 제가 받은 게 최신 버전인가요?" 같은 혼란이 생기지만, 드롭박스를 사용하면 **항상 모든 사람이 같은 최신 버전**을 보게 됩니다.

드롭박스 폴더를 만들었다면, 지도교수, 공동 1저자, 특정 부분에 기여하는 공동연구자들을 초대하세요. 폴더를 공유하는 방법은 간단합니다. 드롭박스에서 해당 폴더를 우클릭하고 "공유(Share)"를 선택한 후, 초대하고 싶은 사람의 이메일 주소를 입력하고 "편집 가능(Can edit)" 권한으로 초대하면 됩니다. 이렇게 하면 여러분이 파일을 업데이트할 때마다 자동으로 동기화되고, 모든 팀원이 협업할 수 있습니다.

### 기본 폴더 구조 만들기

논문 폴더 안에는 다음과 같은 하위 폴더들을 만듭니다:
```
paper_프로젝트명/
  ├── Figures/
  ├── Supplementary_Figures/
  ├── Supplementary_Tables/
  ├── Scripts/
  └── (나중에 만들 폴더: Data/)
```

각 폴더의 역할을 자세히 알아봅시다.

---

## Figures 폴더

이 폴더는 논문 본문에 들어갈 Figure들의 최신 버전을 보관하는 곳입니다. 중요한 것은, 이 폴더는 "논문에 들어갈 현재 최신 버전의 Figure"를 저장하는 곳이라는 점입니다. 분석 과정에서 나온 수많은 그래프들을 저장하는 곳이 **아닙니다**.

예를 들어, 여러분이 10가지 다른 방법으로 데이터를 시각화해봤다면, 그 10개의 그래프는 작업 폴더에 있어야 합니다. 그 중에서 "이게 논문에 들어갈 거야!"라고 결정한 하나만 이 Figures 폴더에 넣는 것입니다.

파일 이름은 `Figure1_v1.pdf`, `Figure2_v1.pdf`, `Figure3_v1.pdf` 형식으로 버전 번호(`v1`, `v2`, `v3`...)를 붙여서 관리합니다. 수정할 때마다 버전을 올리면, 나중에 "아, 이전 버전이 더 나았는데..."라고 생각될 때 돌아갈 수 있습니다.

실제 폴더 구조는 다음과 같습니다:
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

현재 최신 버전은 Figures 폴더 바로 아래에 두고, 이전 버전들은 `old` 서브폴더에 보관합니다. 이렇게 하면 폴더를 열었을 때 현재 사용 중인 Figure들만 바로 볼 수 있어서 명확합니다. 누군가 "지금 시점에서 최신 버전의 Figure들을 달라"고 하면, Figures 폴더의 최상위에 있는 파일들을 주면 됩니다.

### Figures는 Scripts 폴더의 코드로 재현 가능해야 함

Figures 폴더에 들어가는 모든 Figure는 **Scripts 폴더에 저장된 코드를 실행하면 누구든지 똑같이 그릴 수 있어야 합니다**. 이것이 재현 가능한 연구(reproducible research)의 핵심입니다.

예를 들어 `Figures/Figure1_v3.pdf`는 `Scripts/Figure1.R`을 실행하면 만들어져야 하고, `Figures/Figure2_v2.pdf`는 `Scripts/Figure2.R`을 실행하면 만들어져야 합니다.

이렇게 하면 심사자가 "Figure 1이 어떻게 만들어졌나요?"라고 물으면 코드를 보여줄 수 있고, 나중에 Figure를 수정해야 할 때 코드를 조금만 고치면 됩니다. 공동연구자가 Figure를 재생성할 수 있으며, 논문 출판 후 다른 연구자들이 방법론을 정확히 이해할 수 있습니다.

---

## Supplementary_Figures 폴더

본문에는 들어가지 않지만, Supplementary Information에 들어갈 Figure들을 보관합니다. 본문에 들어가기엔 너무 자세하거나, 추가적인 분석 결과들이 여기에 들어갑니다.
```
Supplementary_Figures/
  ├── FigureS1_v1.pdf (← 현재 최신)
  ├── FigureS2_v2.pdf (← 현재 최신)
  ├── FigureS3_v1.pdf (← 현재 최신)
  └── old/
      └── FigureS2_v1.pdf
```

Supplementary Figure도 Main Figure와 **동일한 수준의 퀄리티**로 작성되어야 합니다. "Supplementary"라고 해서 대충 만들면 안 됩니다. 심사자들은 Supplementary도 꼼꼼히 봅니다.

Main Figure에는 논문의 핵심 메시지를 전달하는 Figure, 독자가 반드시 봐야 하는 결과, 논문의 스토리 전개에 필수적인 Figure가 들어갑니다. 반면 Supplementary Figure에는 Main Figure를 뒷받침하는 추가 증거, 통계적 검증 결과(예: QC plots, validation plots), 대체 분석 방법의 결과, 세부적인 기술적 디테일이 들어갑니다.

예를 들어 Main Figure 2가 "우리가 발견한 새로운 유전자 변이"라면, Supplementary Figure S2는 "해당 변이의 검증 실험 결과"가 될 수 있습니다. Supplementary Figure도 `Scripts/FigureS1.R` 같은 코드로 재현 가능해야 합니다.

---

## Supplementary_Tables 폴더

본문에는 들어가지 않지만, Supplementary Information에 들어갈 Table들을 보관합니다. 대부분의 생물학 논문에서 Table은 Main manuscript에 거의 넣지 않고, **거의 모든 Table을 Supplementary에 정리**합니다. Table은 공간을 많이 차지하고, Main manuscript는 Figure 중심으로 스토리를 전개하는 것이 더 효과적이며, 상세한 데이터는 Supplementary에서 제공하는 것이 일반적이기 때문입니다.
```
Supplementary_Tables/
  ├── TableS1_v1.xlsx (← 현재 최신)
  ├── TableS2_v2.xlsx (← 현재 최신)
  ├── TableS3_v1.xlsx (← 현재 최신)
  └── old/
      └── TableS2_v1.xlsx
```

Supplementary Table의 전형적인 구성을 살펴보면, **Table S1**은 샘플 메타데이터로 거의 모든 논문에 필수입니다. 보통 여러 개의 Sheet로 구성되는데, Sheet 1에는 각 Sheet에 대한 설명을, Sheet 2 (Table S1A)에는 샘플 기본 정보(나이, 성별, 진단 등)를, Sheet 3 (Table S1B)에는 샘플 QC 정보(시퀀싱 depth, mapping rate 등)를, Sheet 4 (Table S1C)에는 필요시 추가 메타데이터를 넣습니다.

**Table S2**에는 주요 분석 결과(예: 통계적으로 유의한 유전자 목록)를, **Table S3**에는 추가 분석 결과(예: pathway enrichment 결과)를 넣습니다. Supplementary Table도 `Scripts/TableS1.R` 같은 코드로 자동 생성되어야 합니다.

---

## Scripts 폴더

이 폴더는 Figure와 Table을 만드는 코드를 저장하는 곳으로, **논문의 재현성(reproducibility)을 보장하는 핵심 폴더**입니다. 많은 저널들이 요즘 재현성을 강조하면서 분석 코드 제출을 요구하며, 논문 심사에서도 매우 중요하게 다뤄집니다.

주의할 점은, 여기에는 **모든 분석 코드**를 넣는 것이 아니라는 것입니다. 실제 작업 폴더에서 데이터를 분석한 코드는 거기에 그대로 두면 됩니다. Scripts 폴더에 들어가는 코드는 Figure를 조합하고 레이아웃을 만드는 코드, Table을 최종 포맷으로 정리하고 엑셀로 저장하는 코드, 여러 분석 결과를 모아서 하나의 Figure/Table로 만드는 코드입니다.
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

### 언제부터 Scripts 폴더를 사용하나요?

답은 논문 작성 초기부터입니다. 많은 학생들이 "논문이 거의 다 끝나면 코드를 정리해야지"라고 생각하는데, 이것은 큰 실수입니다. Scripts 폴더의 코드는 **처음부터 작성하고 계속 업데이트**해야 합니다.

Figure를 수정할 때마다 코드만 조금 고치면 되고, 심사자가 수정을 요구하면 코드를 실행만 하면 되며, 나중에 "이 Figure를 어떻게 만들었더라?" 하고 헤맬 일이 없기 때문입니다.

논문을 제출할 때는 Scripts 폴더의 코드를 GitHub에 업로드하거나 Zenodo에 업로드하여 DOI를 받습니다. 그리고 논문의 "Data and Code Availability" 섹션에 다음과 같이 적습니다:

> "All code used to generate figures and tables is available at GitHub (https://github.com/username/project) and archived at Zenodo (DOI: 10.5281/zenodo.1234567)."

이것은 논문 심사에서 매우 중요한 요소입니다. 심사자들은 재현 가능한 연구를 선호하며, 코드가 잘 정리되어 있으면 긍정적인 평가를 받습니다.

### Scripts 예시 1: Multi-panel Figure 만들기 (cowplot 사용)

논문의 Figure는 보통 여러 개의 panel을 조합한 multi-panel plot입니다. R의 `cowplot` 패키지를 사용하면 이를 쉽게 만들 수 있습니다.

다음은 Figure 1을 만드는 코드 예시입니다 (`Scripts/Figure1.R`):
```r
# Figure1.R
# Figure 1: Overview of study design and sample characteristics
# Author: [Your Name]
# Date: 2024-01-15

# Load libraries
library(ggplot2)
library(cowplot)
library(dplyr)

# Load common functions and color schemes
source("Scripts/utils.R")

# Set working directory to project root
# setwd("/path/to/paper_project/")

# Load data from working folder
# (실제 분석은 작업 폴더에서 이미 완료되었고, 여기서는 summary data만 불러옴)
sample_info <- read.csv("../working_folder/results/sample_summary.csv")
qc_metrics <- read.csv("../working_folder/results/qc_summary.csv")

# Panel A: Study design schematic
# (일러스트레이터로 만든 schematic을 PDF로 저장한 경우)
panel_a <- ggdraw() + 
  draw_image("Figures/Figure1_schematic.pdf")

# Panel B: Sample demographics
panel_b <- ggplot(sample_info, aes(x = diagnosis, fill = sex)) +
  geom_bar(position = "dodge") +
  labs(x = "Diagnosis", y = "Number of samples", fill = "Sex") +
  theme_minimal() +
  scale_fill_manual(values = c("Male" = "#3498db", "Female" = "#e74c3c"))

# Panel C: QC metrics
panel_c <- ggplot(qc_metrics, aes(x = read_depth, y = mapping_rate)) +
  geom_point(alpha = 0.5) +
  labs(x = "Read depth (M)", y = "Mapping rate (%)") +
  theme_minimal()

# Combine panels
figure1 <- plot_grid(
  panel_a, panel_b, panel_c,
  ncol = 3,
  labels = c("A", "B", "C"),
  label_size = 16
)

# Save figure
ggsave("Figures/Figure1_v3.pdf", figure1, 
       width = 12, height = 4, units = "in")
```

이 코드는:
1. 각 panel을 개별적으로 생성합니다
2. `cowplot::plot_grid()`로 panel들을 조합합니다
3. 최종 Figure를 PDF로 저장합니다

코드에 주석을 충분히 달아서, 나중에 다시 봐도 이해할 수 있도록 합니다.

### Scripts 예시 2: Supplementary Table 만들기

Supplementary Table도 R 코드로 자동 생성하면 매우 편리합니다. 특히 여러 개의 Sheet가 있는 Excel 파일을 만들 때는 `openxlsx` 패키지를 사용합니다.

다음은 Table S1을 만드는 코드 예시입니다 (`Scripts/TableS1.R`):
```r
# TableS1.R
# Table S1: Sample metadata
# Author: [Your Name]
# Date: 2024-01-15

library(openxlsx)
library(dplyr)

# Load data
sample_info <- read.csv("../working_folder/metadata/sample_info.csv")
qc_metrics <- read.csv("../working_folder/results/qc_metrics.csv")

# Create workbook
wb <- createWorkbook()

# Sheet 1: Description
addWorksheet(wb, "Description")
writeData(wb, "Description", 
          data.frame(
            Sheet = c("Table S1A", "Table S1B"),
            Description = c(
              "Basic demographic and clinical information for all samples",
              "Quality control metrics for sequencing data"
            )
          ))

# Sheet 2: Table S1A - Sample information
addWorksheet(wb, "Table S1A")
table_s1a <- sample_info %>%
  select(Sample_ID, Age, Sex, Diagnosis, IQ, ADOS_Total) %>%
  arrange(Diagnosis, Sample_ID)
writeData(wb, "Table S1A", table_s1a)

# Sheet 3: Table S1B - QC metrics
addWorksheet(wb, "Table S1B")
table_s1b <- qc_metrics %>%
  select(Sample_ID, Total_Reads, Mapped_Reads, Mapping_Rate, 
         Mean_Coverage, Duplicate_Rate) %>%
  arrange(Sample_ID)
writeData(wb, "Table S1B", table_s1b)

# Format headers (bold)
headerStyle <- createStyle(textDecoration = "bold", border = "bottom")
addStyle(wb, "Table S1A", headerStyle, rows = 1, cols = 1:ncol(table_s1a), 
         gridExpand = TRUE)
addStyle(wb, "Table S1B", headerStyle, rows = 1, cols = 1:ncol(table_s1b), 
         gridExpand = TRUE)

# Save workbook
saveWorkbook(wb, "Supplementary_Tables/TableS1_v1.xlsx", overwrite = TRUE)

cat("Table S1 created successfully!\n")
cat("Total samples:", nrow(table_s1a), "\n")
```

이 코드는:
1. 여러 개의 Sheet를 가진 Excel 파일을 생성합니다
2. 각 Sheet에 데이터를 정리해서 넣습니다
3. Header를 Bold로 포맷팅합니다
4. 최종 파일을 저장합니다

이렇게 코드로 Table을 만들면, 데이터가 업데이트되었을 때 코드만 다시 실행하면 되므로 매우 편리합니다.

### Scripts 예시 3: 공통 함수 정리 (utils.R)

여러 Figure에서 공통으로 사용하는 설정이나 함수는 `utils.R`에 정리합니다.

```r
# utils.R
# Common functions and settings for all figures
# Author: [Your Name]
# Date: 2024-01-15

# Color palettes
color_diagnosis <- c(
  "ASD" = "#e74c3c",
  "Control" = "#3498db",
  "Other" = "#95a5a6"
)

color_sex <- c(
  "Male" = "#3498db",
  "Female" = "#e74c3c"
)

# Common theme
theme_paper <- function() {
  theme_minimal() +
  theme(
    text = element_text(size = 12, family = "Arial"),
    axis.title = element_text(size = 14, face = "bold"),
    axis.text = element_text(size = 12),
    legend.title = element_text(size = 12, face = "bold"),
    legend.text = element_text(size = 11),
    panel.grid.minor = element_blank()
  )
}

# Function to format p-values
format_pval <- function(p) {
  ifelse(p < 0.001, "p < 0.001",
         ifelse(p < 0.01, sprintf("p = %.3f", p),
                sprintf("p = %.2f", p)))
}

# Function to add significance stars
add_stars <- function(p) {
  ifelse(p < 0.001, "***",
         ifelse(p < 0.01, "**",
                ifelse(p < 0.05, "*", "ns")))
}
```

이렇게 공통 설정을 `utils.R`에 정리하면:
1. 모든 Figure에서 일관된 색상과 테마를 사용할 수 있습니다
2. 코드 중복을 줄일 수 있습니다
3. 나중에 전체 Figure의 스타일을 한 번에 바꿀 수 있습니다

---

## 원고 파일 관리

이제 Figure와 Table 폴더를 만들었으니, 실제 논문 원고(manuscript) 파일을 어떻게 관리할지 알아봅시다.

### 원고 파일 분리하기

논문 원고는 **세 개의 분리된 파일**로 작성하는 것을 권장합니다:

1. **Manuscript_Main** (본문): Title, Abstract, Introduction, Results, Discussion, References
2. **Manuscript_Methods** (방법론): 모든 Methods 섹션
3. **Supplementary_Information** (보조자료): Supplementary Note, Figure legends, Table legends

왜 파일을 나누는 것이 좋을까요?

**편집의 용이성**: Methods는 보통 매우 길기 때문에, 본문과 분리하면 본문을 편집할 때 훨씬 편합니다. 한 파일에 모든 것을 넣으면 스크롤하는 데만 시간이 걸립니다.

**저널 제출 요구사항**: 많은 저널들이 Main manuscript와 Methods를 분리된 파일로 제출하라고 요구합니다. 처음부터 분리해서 작성하면 제출 준비가 쉽습니다.

**협업 효율성**: 한 사람이 Introduction을 쓰는 동안 다른 사람이 Methods를 쓸 수 있습니다. 파일이 분리되어 있으면 버전 충돌이 적습니다.

**집중력 향상**: 한 번에 하나의 섹션에만 집중할 수 있습니다. "지금은 Results만 쓰자"라고 결심하고 Manuscript_Main.docx만 열면 됩니다.

### 파일 이름 규칙

원고 파일의 이름은 다음 형식을 따릅니다:
```
Manuscript_프로젝트명_섹션_v버전.docx
```

예시:
```
Manuscript_ASD_WGS_Main_v1.0.docx
Manuscript_ASD_WGS_Methods_v1.0.docx
Supplementary_Information_v1.0.docx
```

버전 번호는 `v1.0`, `v1.1`, `v2.0` 형식으로 관리합니다. 마이너 업데이트(작은 수정)는 `v1.0` → `v1.1` → `v1.2`, 메이저 업데이트(큰 수정)는 `v1.3` → `v2.0`처럼 올립니다.

### EndNote 라이브러리 관리

EndNote로 참고문헌을 관리하는 경우, EndNote 라이브러리 파일도 논문 폴더에 넣습니다:
```
paper_ASD_WGS_2024/
  ├── Manuscript_ASD_WGS_Main_v1.0.docx
  ├── References_ASD_WGS.enl (← EndNote 라이브러리)
  └── References_ASD_WGS.Data/ (← EndNote 데이터 폴더)
```

EndNote 라이브러리는 `.enl` 파일과 `.Data` 폴더가 함께 있어야 작동합니다. 이 두 가지를 모두 논문 폴더에 넣어서 드롭박스로 동기화하면, 여러 컴퓨터에서 작업할 때도 참고문헌이 일관되게 관리됩니다.

주의: EndNote 라이브러리를 여러 사람이 동시에 편집하면 충돌이 발생할 수 있습니다. 보통 1저자가 EndNote 라이브러리를 관리하고, 다른 저자들이 참고문헌을 추가하고 싶으면 1저자에게 요청하는 것이 안전합니다.

---

## 버전 관리와 협업 규칙

논문은 혼자 쓰는 것이 아닙니다. 지도교수, 공동저자, 공동연구자들과 함께 작업하게 됩니다. 이때 버전 관리와 협업 규칙이 명확하지 않으면 큰 혼란이 생깁니다.

### 버전 관리의 핵심 원칙

**핵심 원칙은 1저자가 버전을 총괄 관리한다는 것입니다.** 논문 폴더의 모든 파일 버전은 **제1저자(주로 여러분)가 관리**합니다. 즉, 다른 저자가 원고를 수정해주면 **1저자가 그 수정사항을 검토하고 최종 버전으로 만듭니다**. 여러 사람의 의견이 들어와도 **1저자가 통합하고 정리해서 하나의 최신 버전을 만듭니다**. 논문 폴더에 있는 "이니셜 없는 파일"(예: `Manuscript_Main_v2.docx`)은 **항상 1저자가 관리하는 공식 버전**입니다.

이렇게 하는 이유는 버전 충돌을 방지하고, "최신 버전"이 무엇인지 명확하게 하며, 1저자가 논문의 모든 내용을 파악할 수 있게 하기 위함입니다.

### 내 원고를 공동연구자에게 회람할 때

여러분이 작성한 원고를 다른 저자에게 보내서 검토를 요청할 때는 이렇게 합니다.

**버전 업데이트 기준**

마이너 업데이트(작은 수정)는 오타 수정, 문장 다듬기, 참고문헌 추가 등으로, 버전 번호를 `v1.2` → `v1.3`처럼 올립니다. 메이저 업데이트(큰 수정)는 Figure 교체, 섹션 추가/삭제, 분석 결과 추가 등으로, 버전 번호를 `v1.3` → `v2.0`처럼 올립니다.

예시:
```
Manuscript_Main_v1.0.docx (초안)
Manuscript_Main_v1.1.docx (오타 수정)
Manuscript_Main_v1.2.docx (참고문헌 추가)
Manuscript_Main_v2.0.docx (Figure 1 교체, Results 재작성)
Manuscript_Main_v2.1.docx (Discussion 문장 다듬기)
```

**이전 버전의 수정사항 처리**

다른 저자가 이전 버전에 Track Changes로 수정해준 경우, 회람 전에 반드시 해야 할 일이 있습니다. 모든 수정사항(tracked changes)을 확인하고, 동의하는 수정은 "Accept", 동의하지 않는 수정은 "Reject"(단, 공동저자께 이유 설명 필요)합니다. 모든 tracked changes를 처리하고 깨끗한 버전으로 만듭니다.

새로운 버전을 공유할 때 이전 버전의 수정사항이 그대로 남아있으면 어떤 것이 새로운 수정인지 알 수 없고, 파일이 지저분해 보이며, 검토자가 혼란스러워합니다.

**해결된 코멘트 삭제하기**

원고를 버전 업하여 회람할 때, **반드시 해결된 코멘트는 삭제**합니다. 예를 들어 다른 저자가 v2.0에 "이 문장 불명확함. 다시 써주세요"라는 코멘트를 달았고, 여러분이 그 문장을 수정했다면, v2.1을 만들 때 그 코멘트를 삭제합니다.

남겨두는 코멘트는 아직 해결하지 못한 문제, 논의가 더 필요한 부분, 다음 버전에서 다룰 예정인 사항입니다. 이렇게 하면 검토자가 "아직 처리되지 않은 것"만 보게 되어 효율적입니다.

**파일명에서 이니셜 삭제**

이전 버전에서 누군가 수정해준 파일명에 이니셜이 있다면, 새 버전을 만들 때 이니셜을 삭제합니다. 예시:
```
Manuscript_Main_v2.6_JYA.docx (다른 저자가 수정한 버전)
         ↓ (수정사항 반영 후)
Manuscript_Main_v2.7.docx (1저자가 정리한 새 버전)
```

이렇게 하면 "이니셜 없는 파일 = 공식 최신 버전"이라는 것이 명확해집니다.

### 다른 사람의 원고를 수정할 때 (공동연구자, 공동저자의 경우)

반대로, 여러분이 누군가의 원고를 검토하고 수정할 때는 이렇게 합니다.

**Track Changes 반드시 켜기**

절대 규칙은 다른 사람의 원고를 수정할 때는 반드시 워드의 **Review → Track Changes**를 켜야 한다는 것입니다. Track Changes를 켜지 않고 직접 수정하면 원저자가 무엇이 바뀌었는지 알 수 없고, 원저자가 동의하지 않는 수정도 강제로 들어가며, 논의의 여지가 없어집니다.

**파일명에 본인 이니셜 추가**

원고를 수정한 후 저장할 때는 버전을 한 단계 올리고(예: v2.6 → v2.6.1), 파일명 맨 뒤에 **본인 이니셜을 추가**합니다. 예시:
```
받은 파일: Manuscript_Main_v2.6.docx
수정 후: Manuscript_Main_v2.6.1_HJL.docx
```

이렇게 하면 누가 수정했는지 명확하고, 원본 파일은 보존되며, 1저자가 여러 사람의 피드백을 쉽게 통합할 수 있습니다.

**코멘트 적극 활용**

수정 외에 의견을 남길 때는 코멘트를 사용합니다. "이 부분 데이터가 정확한가요?", "이 문장을 이렇게 바꾸는 건 어떨까요?", "Figure 2를 여기로 옮기면 어떨까요?" 같은 경우입니다. 코멘트는 제안이고, Track Changes는 수정입니다. 둘을 적절히 섞어서 사용하세요.

### 실전 예시: 버전 관리 워크플로우

현실적인 상황을 예로 들어봅시다.

**1단계**: 학생(1저자)이 초안을 작성합니다
```
Manuscript_Main_v1.0.docx → 공동저자께 공유
```

**2단계**: 다른 저자가 수정합니다
```
Manuscript_Main_v1.0.docx (받음)
→ (Track Changes로 수정)
→ Manuscript_Main_v1.0.1_JYA.docx (저장 후 학생에게 공유)
```

**3단계**: 학생이 수정사항을 반영합니다
```
Manuscript_Main_v1.0.1_JYA.docx (받음)
→ (수정사항 검토 → Accept/Reject → 추가 수정)
→ Manuscript_Main_v1.1.docx (정리 완료, 다시 공동저자께 공유)
```

**4단계**: 공동연구자도 검토를 요청합니다
```
Manuscript_Main_v1.1.docx → 공동연구자 A, B에게 공유
```

**5단계**: 두 공동연구자가 각각 수정합니다
```
공동연구자 A: Manuscript_Main_v1.1.1_KSM.docx
공동연구자 B: Manuscript_Main_v1.1.2_LHJ.docx
```

**6단계**: 학생이 모든 피드백을 통합합니다
```
두 파일을 모두 검토 → 수정사항 반영 → 새 버전 생성
→ Manuscript_Main_v1.2.docx (통합 완료)
```

이런 식으로 계속 순환하면서 논문이 발전합니다.

---

## 실전 예시: 논문 폴더 완성본

자, 이제 모든 것을 종합해서 완성된 논문 폴더가 어떻게 생겼는지 봅시다:
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

이 폴더를 보면 어떤 파일이 최신인지 한눈에 알 수 있고, Figure와 Table이 몇 개인지 명확하며, 누구에게나 공유하기 쉽고, 저널 제출 준비가 간단합니다.

---

## 학생들이 하는 흔한 실수들

### 파일 관리 실수

**작업 폴더와 논문 폴더를 구분하지 않음**: 논문 폴더에 테스트 코드, 실패한 분석 결과, 중간 산물들을 모두 넣으면 폴더가 금방 지저분해집니다. 작업 폴더와 논문 폴더를 엄격히 분리하세요. 논문 폴더에는 "현재 논문에 들어갈 것"만 넣고, 작업 과정의 모든 것은 작업 폴더에 남겨두고 최종 결과물만 논문 폴더로 복사합니다.

**"final"이라는 단어 사용**: 파일 이름을 `Figure1_final.pdf`, `Figure1_final2.pdf`, `Figure1_final_final.pdf`로 짓는 것도 문제입니다. 항상 `_v1`, `_v2`, `_v3` 형식으로 버전을 관리하세요. "final"이라는 단어는 절대 쓰지 마세요. 논문에서 "final"은 없습니다. 항상 수정이 필요하거든요.

### 초기 준비 실수

**Table S1을 나중에 만들려고 함**: 논문을 거의 다 쓰고 나서 Table S1 (샘플 메타데이터)을 만들려고 하면, 샘플 정보를 다시 정리해야 하고 때로는 분석을 다시 해야 할 수도 있습니다. 논문 작성을 시작하는 첫날 `TableS1_v1.xlsx`를 만드세요. 처음에는 불완전해도 괜찮습니다. 논문을 쓰면서 계속 업데이트하면 됩니다.

**드롭박스를 사용하지 않음**: 로컬 컴퓨터에만 파일을 저장하면, 다른 저자들에게 파일을 매번 이메일로 보내야 하고 버전 관리가 엉망이 됩니다. 논문 폴더를 만들자마자 드롭박스에 올리고 지도교수와 공유하세요. 그러면 파일을 업데이트할 때마다 자동으로 동기화되고, 다른 저자들은 항상 최신 버전을 볼 수 있습니다.

**모든 것을 하나의 파일에 작성**: Title부터 References, Methods, Supplementary까지 모든 것을 하나의 파일에 쓰면 파일이 너무 길어지고 편집이 어렵습니다. Main manuscript, Methods, Supplementary를 세 개의 분리된 파일로 작성하세요. 이렇게 하면 각 부분에 집중할 수 있고, 나중에 저널 제출 시에도 편리합니다.

### 협업 실수

**Track Changes를 사용하지 않음**: 다른 저자가 Track Changes 없이 원고를 직접 고쳐서 보내면, 1저자는 무엇이 바뀌었는지 알 수 없습니다. 협업 초기에 모든 팀원에게 "반드시 Track Changes를 켜고 수정해주세요"라고 명확히 안내합니다.

**동시에 같은 파일 편집**: 여러 저자가 동시에 같은 파일을 받아서 수정하면 버전 충돌이 발생할 수 있습니다. 한 사람씩 순차적으로 검토하도록 요청하거나, 서로 다른 부분(예: 한 사람은 Introduction, 다른 사람은 Discussion)을 맡기거나, 명확히 다른 버전 번호를 부여합니다(v1.0.1_A, v1.0.2_B).

**해결된 코멘트를 삭제하지 않음**: 이미 수정한 부분의 코멘트를 삭제하지 않으면 파일에 수십 개의 코멘트가 쌓여서 혼란스럽습니다. 새 버전을 만들 때마다 해결된 코멘트는 과감히 삭제하세요. 필요하면 "v1.1에서 수정 완료" 같은 메모를 남기고 삭제합니다.

**"최종 버전" 여러 개**: 여러 사람이 각자 "최종 버전"이라고 생각하는 파일을 만들면, 어떤 것이 진짜인지 알 수 없습니다. 처음부터 "1저자가 공식 버전을 관리한다"는 규칙을 명확히 하고, 이니셜 없는 파일만 공식 버전으로 인정합니다.

---

## 자주 묻는 질문

### 언제 논문 폴더를 만들어야 하나요?

지금 당장! 많은 학생들이 "분석이 다 끝나면 논문 폴더를 만들어야지"라고 생각합니다. 하지만 이것은 잘못된 생각입니다. **논문 폴더는 분석을 시작할 때 함께 만들어야 합니다.**

분석하면서 동시에 정리할 수 있습니다. 좋은 결과가 나올 때마다 바로 논문 폴더에 정리하면, 나중에 "어떤 결과가 어디 있더라?" 하고 헤맬 일이 없습니다. Table S1을 먼저 만들 수 있습니다. Supplementary Table S1 (샘플 메타데이터)은 초반에 만들어야 합니다. Methods를 바로 작성할 수 있습니다. 실험이나 분석을 하자마자 Methods를 쓰면, 세부 사항을 잊어버리지 않습니다. "음... 6개월 전에 이 분석을 어떻게 했더라?" 하고 기억을 더듬을 필요가 없습니다. 논문 쓰기가 덜 막막합니다. 논문 폴더가 미리 준비되어 있고, Table S1과 Methods가 어느 정도 작성되어 있으면, 나중에 본격적으로 논문을 쓸 때 심리적 부담이 훨씬 줄어듭니다.

### 어느 시점에 저널을 결정하는 것이 좋을까요?

연구를 시작할 때 지도교수와 논의하면 좋습니다. Figure가 2개 정도 준비되면, 지도교수가 "이제 논문을 쓸 때가 되었다"라고 할 텐데, 그때 타겟 저널을 지도교수와 상의하고 대략 정하는 것이 좋습니다. 타겟 저널이 정해지면 그 저널의 Author Guidelines를 확인하고, Figure 개수 제한, 단어 수 제한, 포맷 요구사항 등을 미리 파악할 수 있습니다.

### 논문 전체 분량은 어떤 기준으로 정하나요?

분량은 투고하고자 하는 저널의 가이드라인에서 확인하고, 그 분량에 맞춰서 작성합니다. 다만 분량을 맞춰서 작성한다고 생각하지 말고, 우선은 글을 쓰십시오. 이후에 문장을 교정하고 재배치하면서 분량을 조절하면 됩니다. 처음부터 "3,000단어 안에 써야 해"라고 생각하면 글쓰기가 위축됩니다. 먼저 하고 싶은 말을 다 쓰고, 나중에 다듬으세요.

### Figure를 먼저 그리고 본문을 쓰는 것이 효율적인가요, 아니면 본문을 먼저 작성한 뒤 Figure를 그리는 것이 좋을까요?

일반적으로는 Figure를 작성하고, 이후에 본문을 쓰는 것이 좋습니다. Figure가 있으면 Results를 쓸 때 "이 Figure는 이런 것을 보여준다"라고 설명할 수 있기 때문입니다. 그러나 본문을 먼저 스토리처럼 작성하고, 그 흐름에 맞춰 결과를 배치하면서 Figure를 작성할 수도 있습니다. 그 과정에서 본문의 내용을 정확하게 기입하며 수정할 수 있습니다. 본인에게 맞는 방식을 연습해보는 것이 좋습니다.

### Figure 작업 시 사용하는 툴(예: Illustrator)은 새로 배워야 하나요?

우리 연구실은 일러스트레이터로 Figure를 작업합니다. 일러스트레이터 작업 능력은 필수입니다. R이나 Python으로 그래프를 그린 후, 일러스트레이터에서 레이아웃을 조정하고 레이블을 추가하는 방식으로 작업합니다. 처음에는 어렵게 느껴지지만, 몇 번 연습하면 금방 익숙해집니다.

### Main Figure와 Supplementary Figure를 구분할 때, 어떤 기준으로 배치 결정을 하나요?

처음에는 Main Figure를 염두에 두고 Figure를 준비합니다. 그렇게 그리다 보면, 스토리 전개상 우선순위가 높은 Figure들이 선별됩니다. 그렇게 주전과 후보 선수를 선별해 가며 Figure를 그리면 됩니다. 논문의 핵심 메시지를 전달하는 데 꼭 필요한 Figure는 Main Figure로, 추가적인 검증이나 세부 사항을 보여주는 Figure는 Supplementary Figure로 분류합니다.

---

이제 여러분은 논문 작성을 시작할 준비가 되었습니다. 논문 폴더를 만들고, 드롭박스에 올리고, 지도교수와 공유하세요. 그리고 Table S1을 만드는 것부터 시작하세요. 작은 한 걸음이 여러분의 첫 논문으로 이어질 것입니다.
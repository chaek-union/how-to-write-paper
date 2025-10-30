# 4장. Results — 데이터가 말하게 하기

Results 섹션을 쓸 때 가장 먼저 해야 할 일은 무엇일까? 많은 학생들이 첫 번째 분석 결과부터 순서대로 적기 시작한다. 하지만 좋은 Results는 **전체 구조를 먼저 설계**하고 시작해야 한다. 이번 장에서는 Results 섹션 전체의 뼈대를 어떻게 짜야 하는지, 각 subsection을 어떻게 배치하고 연결해야 하는지를 다룬다. 문장 레벨의 작성 기술은 다음 장에서 다룰 것이고, 여기서는 큰 그림에 집중한다.

## Results의 핵심 원칙: 데이터가 주인공이다

**Results vs Methods vs Discussion**

Results를 쓰기 전에 먼저 명확히 해야 할 것이 있다. Results, Methods, Discussion은 각각 다른 역할을 한다.

| 섹션 | 질문 | 예시 |
|------|------|------|
| **Methods** | 어떻게 했는가? | We performed NMF clustering using proteomic, phosphoproteomic, and acetylproteomic data |
| **Results** | 무엇을 발견했는가? | We identified five multiomics subtypes characterized by distinct molecular pathways |
| **Discussion** | 무엇을 의미하는가? | These subtypes have important implications for personalized treatment strategies |

Results는 오직 **"무엇을 발견했는가"**에만 집중해야 한다.

**실제 논문에서의 예시**

우리가 작성한 한국인 NSCLC 환자의 proteogenomics 연구 논문에서 가져온 예다 ([Song et al. 2024, Nature Communications](https://www.nature.com/articles/s41467-024-54434-4)).

잘못된 Results (Methods가 섞임):
```
To establish comprehensive multiomics subtypes, we integrated proteomic, 
phosphoproteomic, and acetylproteomic data and conducted non-negative matrix 
factorization (NMF) clustering to identify multiomics subtypes.
```

이것은 거의 전부 Methods에 들어가야 할 내용이다. "To establish", "we integrated", "we conducted" - 이런 표현들은 모두 **과정**을 설명하는 것이다.

올바른 Results:
```
We identified five multiomics subtypes: metabolic (Subtype 1), alveolar-like 
(Subtype 2), proliferative (Subtype 3), hypoxic (Subtype 4), and immunogenic 
(Subtype 5), characterized based on genetic mutations, clinical phenotypes, 
and molecular pathways.
```

**발견**에만 집중한다. 어떻게 분석했는지는 Methods에 있다.

내가 학생들에게 자주 남기는 코멘트다:

> "이런 내용은 쓰지 않아도 되고요. 서브타입을 정의한 기준은 Methods에 넣으면 됩니다."

> "바로 이전 문장들도 많이 Methods 같아요 ~ 수정을 해주세요. NMF clustering을 어떻게 수행했는지가 아니라, 무엇을 발견했는지를 써야 합니다."

> "사용했던 multiomics 데이터를 Table S1으로 정리하기. 현재 산발적으로 언급했는데, 이걸 통합해서 넣으면 좋겠습니다. 그리고 Method에도 데이터 생성 과정을 기술해주세요."

**원칙: Results에는 발견만, Methods에는 방법만**

Results에 적합한 동사:
- showed, demonstrated, revealed
- observed, identified, found
- consisted of, comprised, included
- differed, increased, decreased

Results에 부적합한 동사 (Methods용):
- performed, conducted, analyzed
- established, constructed, developed
- optimized, benchmarked, validated
- collected, generated, processed

분석 도구의 사용법, parameter 설정, input/output 형식 등은 모두 Methods 섹션에 포함해야 한다.

## 섹션 구성과 논리적 흐름

**섹션 제목은 발견을 담아야 한다**

각 subsection의 제목이 너무 일반적이면 독자의 관심을 끌기 어렵다.

평범한 제목:
- "Subtype identification"
- "Immune cell analysis"
- "Survival analysis"

발견을 담은 제목 ([Song et al. 2024, Nature Communications](https://www.nature.com/articles/s41467-024-54434-4)에서):
- "A NSCLC subtype associated with poor prognosis and frequent metastasis"
- "Proteogenomic features underlying whole-genome doubling in NSCLC subtypes"
- "Multiomics profiling of neoantigens and immune clusters"

**좋은 제목의 특징:**

1. **구체적이다** - "Subtype identification"이 아니라 "A NSCLC subtype associated with poor prognosis"
2. **발견을 담는다** - 분석 방법이 아니라 무엇을 발견했는지
3. **관계를 보여준다** - "A affects B" 혹은 "A underlying B" 형태로 연관성 제시

제목만 읽어도 무엇을 발견했는지 알 수 있어야 한다.

**섹션 간 연결성: 논문 제목과의 일관성**

각 섹션이 자연스럽게 이어져야 한다. 독자가 "왜 갑자기 이 이야기?"라고 느끼면 안 된다.

내가 학생에게 남긴 코멘트:

> "여기도 마찬가지인데, 논문의 제목도 'NSCLC subtypes'이고, 첫 섹션도 'Identification of subtypes'로 시작했는데요. 갑자기 2번째, 3번째 섹션에서 뜬금없이 일반적인 immune cell 분석을 이야기합니다. 실지어 이 내용은 이미 다른 연구들에서 다 나온 이야기들이고요. 우리가 논문을 투고하면, 에디터가 2번째 혹은 3번째 페이지까지 보고 '이 연구 이미 다 한거네. 왜 또 해?'라고 할거고, 바로 리젝될겁니다. 다른게 없어요. 저라면, 2,3번을 합치고 바로 'Subtype-specific immune landscape'라는 주제로 두번째 섹션을 시작합니다. 그래야 1번째에서 웅장하게 시작한 Subtypes 이야기가 이어지죠."

**Song et al., 2024 논문의 섹션 구조 분석:**

논문 제목: "Proteogenomic analysis reveals non-small cell lung cancer **subtypes** predicting chromosome instability, and tumor microenvironment"

Results 섹션 구성:
1. Identification of **subtypes** in NSCLC patients by multiomics
2. A NSCLC **subtype** associated with poor prognosis and frequent metastasis
3. Cellular landscape of the five **subtypes** of NSCLC
4. Proteogenomic features underlying whole-genome doubling in NSCLC **subtypes**
5. Heterogeneous immune landscapes in NSCLC
6. Multiomics profiling of neoantigens and immune clusters

모든 섹션이 "subtypes"라는 중심 주제를 유지한다. 첫 섹션에서 5개 서브타입을 소개하고, 이후 섹션들이 각 서브타입의 특성을 다양한 관점(예후, 세포 구성, WGD, 면역 환경)에서 다룬다.

**섹션의 첫 문장이 중요하다**

각 섹션의 첫 문장은 해당 섹션의 방향을 제시한다.

내가 학생에게 남긴 코멘트:

> "각 섹션명을 적었는데, 이 섹션들을 이어서 읽으면 전혀 내용이 이어지지 않습니다. 첫번째 섹션은 'NSCLC multiomics subtypes'라고 했는데요. 그러고 바로 뒷 섹션은 'Kinase activity in cancer'라고 되었어요. Kinase가 암에서 중요하다는걸 모르는 사람이 있나요? 전혀 연결이 안되요. 우리가 발견한 subtypes와 kinase의 관계를 설명해야죠. 저만 이해를 못하는건지요?"


**Song et al., 2024의 좋은 예시:**

섹션 2의 첫 문장:
```
To replicate our subtype classification, we utilized multiomics or proteomics 
data from 462 patients with NSCLC obtained from previous studies.
```

섹션 3의 첫 문장:
```
Exploring the tumor microenvironment is crucial for understanding the mechanisms 
underlying cancer progression and for developing effective therapeutic strategies 
to target not only cancer cells but also the surrounding microenvironment.
```

두 번째 섹션이 첫 번째 섹션의 발견(5개 서브타입)을 다른 코호트에서 검증하겠다고 명확히 밝히고, 세 번째 섹션은 "왜 이제 종양 미세환경을 봐야 하는가"를 설명하면서 자연스럽게 연결된다.

각 섹션의 첫 문장에서 "왜 이 내용이 지금 필요한가"를 명확히 해야 한다.

**독자의 시선으로 읽기**

논문을 다 쓴 후, 각 섹션의 제목만 순서대로 읽어보자.

잘못된 흐름:
```
1. Multiomics subtype identification
2. Kinase activity analysis
3. Cell type analysis
4. Survival analysis
```

독자 반응: "2번이 왜 갑자기? 1번에서 서브타입 이야기하다가 왜 갑자기 kinase?"

좋은 흐름 ([Song et al. 2024, Nature Communications](https://www.nature.com/articles/s41467-024-54434-4)):
```
1. Identification of subtypes in NSCLC patients by multiomics
2. A NSCLC subtype associated with poor prognosis and frequent metastasis
3. Cellular landscape of the five subtypes of NSCLC
4. Proteogenomic features underlying whole-genome doubling in NSCLC subtypes
5. Heterogeneous immune landscapes in NSCLC
6. Multiomics profiling of neoantigens and immune clusters
```

독자 반응: "1번에서 5개 서브타입 소개, 2번에서 특히 예후가 나쁜 서브타입 집중 분석, 3번에서 서브타입별 세포 특성, 4번에서 증식성 서브타입의 WGD 특징, 5-6번에서 면역 환경 분석. 논리적이네!"

## 문단 구성의 원칙

### 문단 한개는 하나의 완결된 아이디어

너무 짧은 문단은 대부분 앞뒤 문단과 합칠 수 있다.

> "한가지 궁금한게 (manuscript 전반적으로), 문단이 짧은데요. 여기도 문장 2개가 한 문단이라... 특별한 이유가 있을지?"

1-2문장으로 끝나는 문단은 피하자. 하나의 발견이나 개념을 설명하는 데 보통 3-5문장이 필요하다.

**Song et al., 2024의 문단 구조 예시:**

```
[문단 1: Subtype 4의 인산화 특징 - 6문장]
To examine the molecular characteristics of Subtype 4, we extracted distinct 
features (proteins, phosphorylation, or acetylation) of the subtypes in our 
NMF clustering analysis. We found that the majority of NMF features present 
in Subtype 4 were phosphorylated sites (96%, 178/186), indicating that 
phospho-kinase interactions are a major signature. Therefore, we investigated 
the kinase activity of this subtype using phosphoproteomic data. We found 
significant enrichment of two kinases, CSNK2A1 (FDR = 2.3 × 10−7) and GSK3B 
(FDR = 1.9 × 10−2), which are known to phosphorylate various proteins in 
the PI3K-AKT signaling pathway, in Subtype 4 compared to other subtypes. 
Upon evaluating the relationship between the activity and expression levels 
of significant kinases (P < 0.05), we observed a moderate correlation. 
Survival analysis based on feature expression showed that most of the 
unfavorable prognostic factors were phosphorylated sites differentially 
expressed in Subtype 4 (91%, 104/114).

[문단 2: SLK 인산화와 예후 - 5문장]
Notably, STE20-like serine/threonine-protein kinase at serine 347 (SLK (S347)), 
a protein phosphorylated by CSNK2A1, was significantly upregulated in Subtype 4 
(adjusted P = 8.0 × 10−3) and associated with unfavorable prognostic features 
(P = 3.0 × 10−6). In the combined CPTAC dataset, we also found increased 
phosphorylation of SLK (S347) in Subtype 4 and poor survival outcomes. SLK 
mediates apoptosis downstream of the ErbB2 and PI3K pathways and is activated 
in a CSNK2A1-dependent manner. Recent studies have reported that high SLK 
expression is associated with reduced overall survival in HER2-positive patients 
and in glioma. Collectively, these results suggest that SLK participates in 
tumor progression and could be a key marker specific to Subtype 4.
```

각 문단이 하나의 완결된 발견을 담고 있다. 첫 번째 문단은 Subtype 4의 전반적인 인산화 특징을, 두 번째 문단은 특정 마커(SLK)에 대한 상세 분석을 다룬다.

### 각 문단의 첫 문장 = Topic Sentence

문단의 첫 문장(topic sentence)이 해당 문단의 핵심을 담아야 한다.

독자는 각 문단의 첫 문장만 읽어도 대략적인 흐름을 파악할 수 있어야 한다.

Song et al., 2024의 "A NSCLC subtype associated with poor prognosis" 섹션에서 각 문단의 첫 문장만 추출해보면:

```
Paragraph 1: To examine the molecular characteristics of Subtype 4, we extracted distinct features...
Paragraph 2: Notably, STE20-like serine/threonine-protein kinase at serine 347 (SLK (S347))...
Paragraph 3: Furthermore, Subtype 4 showed a significant upregulation of leucine-rich repeat...
Paragraph 4: Subtype 4 included numerous prognostic features in the HIF-1 and PI3K-AKT signaling pathways...
Paragraph 5: We evaluated the clinical significance of Subtype 4 according to the survival rates...
```

각 문단의 첫 문장만 읽어도 "Subtype 4의 분자적 특징 → SLK 마커 → LRRFIP1 마커 → 신호전달 경로 → 생존율 분석" 순서로 분석이 진행되었음을 알 수 있다.

## 용어 사용의 정확성과 일관성

### 개념을 명확히 구분한다

비슷해 보이는 용어들도 과학적으로는 다른 의미를 가진다. 정확하게 구분해서 사용해야 한다.

내가 학생들에게 남긴 코멘트:

> "이건 불필요한 설명이에요. 단순하게 proteomics를 보겠다는게 아니라 마치 phosphoproteomics만 보겠다는 의도 같구요. 그러면 이 섹션의 첫 부분에는 왜 phosphoproteomics가 중요한지 설명이 나와야하는거죠."

> "그리고 나서 global proteome을 보고, 마지막으로 acetylome을 보겠다고 하고, PTM 분석을 들어가면 됩니다. 각각의 역할이 다르니까요."

**Song et al., 2024가 구분하는 용어들:**

**Neoantigen vs Cryptic MAP**
- Neoantigen: 체세포 돌연변이에서 유래한 종양 특이적 항원
- Cryptic MAP: 비코딩/비주석 전사체에서 유래한 MHC class I 결합 펩타이드

논문에서 이 둘을 명확히 구분하여 사용한다:
```
We inferred 85,430 neoantigen candidates and 775 cryptic MAPs and annotated 
the origin of the cryptic MAPs based on the matched transcripts. Interestingly, 
only confirmed cryptic MAPs showed a strong positive correlation with improved 
survival, although the number of cryptic MAPs was notably low across patients.
```

**HTE vs CTE (면역 클러스터)**
- HTE (hot-tumor-enriched): 면역세포가 풍부한 "뜨거운" 종양
- CTE (cold-tumor-enriched): 면역세포가 적은 "차가운" 종양

### 용어 일관성이 중요한 이유: 독자의 인지적 색인

논문은 단순히 데이터를 나열하는 문서가 아니다. 독자의 머릿속에 **개념의 지도**를 그려주는 일이다. 

논문을 읽는 독자는 마치 제품 브로셔를 보듯, 핵심 용어를 통해 전체 내용을 이해한다. 특정 용어가 반복될 때마다 독자는 이전에 읽었던 맥락을 다시 떠올린다. 이것을 **인지적 색인(cognitive index)**이라고 부를 수 있다. 

**Song et al., 2024의 좋은 예:**

논문 전체에서 "multiomics subtypes"라는 용어를 일관되게 사용한다:
- Abstract: "...reveals five molecular subtypes"
- Introduction: "...to define the molecular subtypes of NSCLC"
- Results 섹션 1: "Identification of subtypes in NSCLC patients by multiomics"
- Results 섹션 2: "A NSCLC subtype associated with poor prognosis"
- Results 섹션 3: "Cellular landscape of the five subtypes"
- Discussion: "...the five NSCLC subtypes enriched for WGD, oncogenes..."

독자는 "subtypes"라는 단어를 볼 때마다 "아, 저 5개 그룹을 말하는구나"라고 즉시 이해한다.

**핵심 용어는 논문 초반에 확립한다**

독자의 머릿속 색인을 만들려면, 핵심 용어를 Results 첫 섹션에서 명확히 정의해야 한다.

Song et al., 2024의 첫 Results 섹션:
```
We identified five multiomics subtypes: metabolic (Subtype 1), alveolar-like 
(Subtype 2), proliferative (Subtype 3), hypoxic (Subtype 4), and immunogenic 
(Subtype 5), characterized based on genetic mutations, clinical phenotypes, 
and molecular pathways.
```

이 한 문장이 논문 전체의 **인지적 프레임워크**를 설정한다. 독자는 이후 "Subtype 3"을 볼 때마다 "proliferative한 그 그룹"을 떠올린다.

**일관성이 깨지면 독자는 길을 잃는다**

만약 같은 개념을 다르게 부르면:
- 첫 섹션: "multiomics subtypes"
- 중간 섹션: "molecular clusters"  
- 마지막 섹션: "patient groups"

독자는 "이게 같은 건가? 다른 건가?"라며 계속 뒤로 돌아가서 확인해야 한다. 인지적 부담이 커진다.

**용어 일관성 체크리스트:**

논문을 다 쓴 후, 다음을 확인하자:
1. 핵심 개념을 나타내는 용어가 전체 논문에서 동일한가?
2. 약어를 한번 정의한 후 계속 사용하는가?
3. Figure legend에서도 동일한 용어를 사용하는가?
4. Supplementary Material에서도 일관된 용어를 쓰는가?

### 용어를 통일한다

한 논문 내에서 같은 개념을 다른 용어로 표현하면 독자가 혼란스러워한다.

**Fig vs Figure:**

> "Fig도 쓰는 것도 있고 Figure로 쓰는것도 있는데, 통일을 시켜주면 좋겠습니다."

**Cell subtype vs Molecular subtype vs Genomic subtype:**

> "바로 아래 문단에는 'molecular subtype'이라는 표현을 썼고, 여기는 그냥 'subtype'인데, 통일을 하면 좋겠습니다."

> "저는 molecular subtype은 아닌것 같아요. 왜냐면, RNA, protein expression을 측정한건 아니니까요. 그래서 genomic subtype이라는 표현을 쓰는게 좋을것 같아요."

**Song et al., 2024가 잘한 점:**

논문 전체에서 용어를 일관되게 사용한다:
- Multiomics subtypes (일관되게 Subtype 1-5)
- WGD (whole genome doubling)
- TMB (tumor mutational burden)
- HTE/CTE (hot/cold-tumor-enriched)

한번 약어를 정의하면 논문 전체에서 동일하게 사용한다.


## Figure와 Table의 효과적 배치

### 본문에서 구체적으로 언급한다

Figure나 Table을 언급할 때는 구체적인 정보와 함께 제시해야 한다.

잘못된 예:
```
Results are shown in Figure 2.
```

올바른 예 ([Song et al. 2024, Nature Communications](https://www.nature.com/articles/s41467-024-54434-4)):
```
We found significant enrichment of two kinases, CSNK2A1 (FDR = 2.3 × 10−7) 
and GSK3B (FDR = 1.9 × 10−2), which are known to phosphorylate various 
proteins in the PI3K-AKT signaling pathway, in Subtype 4 compared to other 
subtypes (Fig. 2d, Supplementary Fig. 2d and Supplementary Data 2c).
```

구체적인 숫자와 통계값을 본문에 제시하고, Figure는 시각적 확인을 위해 인용한다.

### 순서대로 언급한다 (당연하게도..)

Figure와 Table은 본문에 등장하는 순서대로 번호를 매겨야 한다. Figure 1A, 1B, 1C 순서로 언급하다가 갑자기 Figure 3을 언급하면 안 된다. 논문을 쓰다보면, 자주 순서가 바뀌는데, 부지런히 바꾸어야 한다. 동숲에서 꽃밭에 물을 주듯.. 매일 매일 모닝커피와 함께 부지런히 확인한다. 

**Song et al., 2024의 Figure 배치:**

```
Results 섹션 1: Fig. 1a, 1b, 1c, 1d, 1e (Subtype identification)
Results 섹션 2: Fig. 2a, 2b, 2c, 2d, 2e, 2f, 2g, 2h, 2i, 2j (Subtype 4 특성)
Results 섹션 3: Fig. 3a, 3b-m (Cellular landscape)
Results 섹션 4: Fig. 4a-i (WGD features)
Results 섹션 5: Fig. 5a-g (Immune landscape)
Results 섹션 6: Fig. 6a-g (Neoantigens)
```

논리적인 순서로 배치되어 있다.

### Figure 내용이 본문과 일치해야 한다

내가 학생에게 남긴 코멘트:

> "히트맵하고 이 부분의 서술이 매칭이 안됩니다. 여기서는 GO 결과 같은게 들어간 것 같은데 (제가 이해한게 맞다면), 그런 부분이 히트맵에 표시가 되어야 할 것 같아요."

본문에서 설명한 내용이 Figure에서 시각적으로 확인 가능해야 한다.

**Supplementary vs Main Figure**

저널의 가이드라인을 확인해야 한다.

> "투고하려는 논문 사이트에서 author guideline 확인해주세요. Supplementary Figure 라고 쓰는지 Figure S 라고 쓰는지 확인을 해주세요."

일반적으로:
- **Main Figure**: 핵심 발견
- **Supplementary Figure**: 보조 데이터, 검증 실험, 추가 분석

Song et al., 2024의 경우:
- Main Figures (1-6): 서브타입 정의, 예후 분석, 세포 특성, WGD, 면역 환경
- Supplementary Figures: TMB 분포, 추가 kinase 분석, 검증 코호트 결과

## 저널별 요구사항 확인

Journal은 각자의 Author guideline이 있다. 투고 전에 반드시 저널의 가이드라인을 읽어야 한다.

확인할 사항:
- Results 섹션의 길이 제한
- Figure와 Table 개수 제한
- Supplementary Material 형식
- 인용 스타일
- 약어 사용 규칙


# 4장. Results — 데이터가 말하게 하기

Results 섹션을 쓸 때 가장 먼저 해야 할 일은 무엇일까? 많은 학생들이 첫 번째 분석 결과부터 순서대로 적기 시작한다. 하지만 좋은 Results는 **전체 구조를 먼저 설계**하고 시작해야 한다.

이 장에서는 Results 섹션 전체의 뼈대를 어떻게 짜야 하는지, 각 subsection을 어떻게 배치하고 연결해야 하는지를 다룬다. 문장 레벨의 작성 기술은 다음 장에서 다룰 것이고, 여기서는 큰 그림에 집중한다.

## Results의 핵심 원칙: 데이터가 주인공이다

**Results vs Methods vs Discussion**

Results를 쓰기 전에 먼저 명확히 해야 할 것이 있다. Results, Methods, Discussion은 각각 다른 역할을 한다.

| 섹션 | 질문 | 예시 |
|------|------|------|
| **Methods** | 어떻게 했는가? | We performed quality control using Hail 0.2 and filtered variants with GQ ≥ 20 |
| **Results** | 무엇을 발견했는가? | We identified 696 individuals with autism (5.6 male-to-female ratio) |
| **Discussion** | 무엇을 의미하는가? | This ratio suggests differential ascertainment bias across sexes |

Results는 오직 **"무엇을 발견했는가"**에만 집중해야 한다.

**실제 논문에서의 예시**

한국인 자폐 가족 WGS 연구 논문에서 가져온 예다 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)).

잘못된 Results (Methods가 섞임):
```
To establish a comprehensive resource, we constructed an atlas comprising 
approximately 3.6 million cells. We integrated 40 previously published datasets. 
To optimize the integration, we benchmarked batch correction methods.
```

이것은 거의 전부 Methods에 들어가야 할 내용이다. "To establish", "we constructed", "we integrated", "to optimize", "we benchmarked" - 이런 표현들은 모두 **과정**을 설명하는 것이다.

올바른 Results:
```
The Korean autism WGS data consists of 673 families of total 2,255 individuals, 
encompassing 21 multiplex families with more than two autistic children. Of the 696 
individuals with autism, 590 were males and 106 were females (5.6 male-to-female ratio). 
Siblings included 90 male and 123 female individuals (0.74 male-to-female ratio).
```

**숫자와 발견**만 제시한다. 어떻게 모았는지는 Methods에 있다.

내가 학생들에게 자주 남기는 코멘트다:

> "이런 내용은 쓰지 않아도 되고요. 셀타입을 명명한 것은 기준을 사용해서 메쏘드에 넣으면 됩니다."

> "바로 이전 문장들도 많이 메쏘드 같아요 ~ 수정을 해주세요."

> "사용했던 데이터를 Table S1으로 정리하기. HCA 형태로 현재 정리했을텐데, 그걸 통일해서 넣으면 좋겠습니다. 그리고 Method에도 HCA sample metainformation 형태로 정리했다고 기술해주세요."

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

또 다른 학생 논문에서 남긴 코멘트:

> "CWAS-Plus package가 annotation 하는것 같진 않은데요? Annotation 된 데이터를 넣는것 아닌가요? 그러면 이 패키지에서 annotation을 한다고 말하긴 어려울것 같아요. 이 부분은 Input requirement가 되어야 할 것 같아요."

분석 도구의 사용법, parameter 설정, input/output 형식 등은 모두 Methods 섹션에 포함해야 한다.

## 섹션 구성과 논리적 흐름

**섹션 제목은 발견을 담아야 한다**

각 subsection의 제목이 너무 일반적이면 독자의 관심을 끌기 어렵다.

평범한 제목:
- "Sex differences in ASD"
- "Gene expression analysis"
- "Subtype identification"

발견을 담은 제목 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)에서):
- "Sex differences of autism-associated genetic burden"
- "Intellectual disability and total symptom severity affect sex differences in genetic burden"
- "Tolerance of polygenic burden for multiple autism traits in females within families"

**좋은 제목의 특징:**

1. **구체적이다** - "Sex differences"가 아니라 "Sex differences of autism-associated genetic burden"
2. **발견을 담는다** - 분석 방법이 아니라 무엇을 발견했는지
3. **관계를 보여준다** - "A affects B" 형태로 인과관계나 연관성 제시

제목만 읽어도 무엇을 발견했는지 알 수 있어야 한다.

**섹션 간 연결성: 논문 제목과의 일관성**

각 섹션이 자연스럽게 이어져야 한다. 독자가 "왜 갑자기 이 이야기?"라고 느끼면 안 된다.

내가 학생에게 남긴 코멘트:

> "여기도 마찬가지인데, 논문의 제목도 'sex-bias'이고, 첫 섹션도 'sex bias in Korean ASD'로 시작했는데요. 갑자기 2번째, 3번째 섹션에서 뜬금없이 genetic variant association을 이야기합니다. 실지어 이 내용은 이미 다른 연구들에서 다 나온 이야기들이고요. 우리가 논문을 투고하면, 에디터가 2번째 혹은 3번째 타라까지 보고 '이 연구 이미 다 한거네. 왜 또 해?'라고 할거고, 바로 리젝될겁니다. 다른게 없어요. 저라면, 2,3,4번을 다 합치고 바로 'Genetic variants and Sex-bias'라는 주제로 두번째 섹션을 합니다. 그래야 1번째 융창하게 시작한 Sex bias가 이어지죠.."

**Kim et al., 2024 논문의 섹션 구조 분석:**

논문 제목: "Whole genome sequencing analysis identifies **sex differences** of familial pattern contributing to phenotypic diversity in autism"

Results 섹션 구성:
1. Overview of autism family data of East Asian and European ancestry
2. **Sex differences** of autism-associated genetic burden
3. Intellectual disability and total symptom severity affect **sex differences** in genetic burden
4. Intellectual disability and total symptom severity in male-to-female autism prevalence
5. Tolerance of polygenic burden for multiple autism traits in **females** within families

모든 섹션이 "sex differences"라는 중심 주제를 유지한다. 첫 섹션에서 데이터를 소개하고, 2-5번 섹션이 모두 성별 차이의 다양한 측면을 다룬다.

**섹션의 첫 문장이 중요하다**

각 섹션의 첫 문장은 해당 섹션의 방향을 제시한다.

내가 학생에게 남긴 코멘트:

> "각 섹션명을 적었는데, 이 섹션들을 이어서 읽으면 전혀 내용이 이어지지 않습니다. 첫번째 섹션은 'Sex difference in Korean ASD-WGS data'라고 했는데요 (사실 성별 차이가 데이터에 존재하는게 아니죠.. 환자겠죠?). 그러고 바로 뒷 섹션은 '자폐에는 여러 요인들이 있다'라고 되었어요. 자폐에 여러 요인이 있다는걸 모르는 사람이 있나요? 전혀 연결이 안되요.. 저만 이해를 못하는건지요?"

**Kim et al., 2024의 좋은 예시:**

섹션 2의 첫 문장:
```
We conducted a quality control assessment for the WGS datasets as per previous 
WGS studies and prioritized high-quality variants for de novo and common variant 
analyses (Fig. 2A).
```

섹션 3의 첫 문장:
```
While a higher burden of de novo PTVs in autistic females than autistic males 
were consistently observed in the Korean, SSC, and SPARK cohorts, the SPARK 
cases exhibited less pronounced female enrichment of de novo PTVs compared to 
the Korean and SSC cohorts.
```

두 번째 섹션이 첫 번째 섹션의 발견(성별에 따른 de novo PTV 차이)을 언급하며 자연스럽게 연결된다. "왜 SPARK는 다른가?"라는 새로운 질문을 제기하면서 다음 분석으로 이어진다.

각 섹션의 첫 문장에서 "왜 이 내용이 지금 필요한가"를 명확히 해야 한다.

**독자의 시선으로 읽기**

논문을 다 쓴 후, 각 섹션의 제목만 순서대로 읽어보자. 

잘못된 흐름:
```
1. Sex difference in Korean ASD-WGS data
2. Autism has multiple contributing factors
3. Genetic variant associations in autism
4. Sex-specific patterns
```

독자 반응: "2번이 왜 갑자기? 1번에서 성별 차이 이야기하다가 왜 갑자기 일반적인 자폐 이야기?"

좋은 흐름 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)):
```
1. Overview of autism family data
2. Sex differences of autism-associated genetic burden
3. ID and symptom severity affect sex differences in genetic burden
4. ID and symptom severity in male-to-female ratio
5. Tolerance of polygenic burden in females within families
```

독자 반응: "1번에서 데이터 소개, 2번에서 성별 차이 발견, 3번에서 무엇이 그 차이를 만드는지, 4번에서 그것이 성비에 미치는 영향, 5번에서 가족 내 검증. 논리적이네!"

## 문단 구성의 원칙

### 문단 한개는 하나의 완결된 아이디어

너무 짧은 문단은 대부분 앞뒤 문단과 합칠 수 있다.

> "한가지 궁금한게 (manuscript 전반적으로), 문단이 짧은데요. 여기도 문장 2개가 한 문단이라... 특별한 이유가 있을지?"

1-2문장으로 끝나는 문단은 피하자. 하나의 발견이나 개념을 설명하는 데 보통 3-5문장이 필요하다.

**Kim et al., 2024의 문단 구조 예시:**

```
[문단 1: de novo PTV의 성별 차이 - 5문장]
We conducted a quality control assessment for the WGS datasets... 
Our WGS analyses revealed a higher rate of de novo PTVs and MIS in children 
with autism compared to non-autistic siblings (Fig. 2B). Consistent with existing 
findings, de novo PTVs were found to be significantly enriched in children with 
autism in both Korean and replication cohorts (Fig. 2B). In children with autism, 
de novo PTVs were observed more frequently in females than males in Korean cohort 
(RR = 2.0; P = 0.11), SSC (RR = 1.8; P = 1.1 × 10−2), and SPARK (RR = 1.2; 
P = 0.32) (Fig. 2C). Although the difference was only significant in SSC, these 
results are consistent with a higher liability threshold in autistic females 
than males.

[문단 2: 성별 특이적 유전자 분석 - 4문장]
We further aimed to identify autism-associated genes in autistic females and 
males separately... We identified 98 autism-associated genes in females and 461 
genes in males, of which 58 genes overlapped. Identified genes were enriched for 
biological pathways... Female-specific genes were enriched for chromatin regulation 
and histone modification, whereas male-specific genes were highly observed in 
synaptic functions.
```

각 문단이 하나의 완결된 발견을 담고 있다.

### 각 문단의 첫 문장 = Topic Sentence

문단의 첫 문장(topic sentence)이 해당 문단의 핵심을 담아야 한다. 

독자는 각 문단의 첫 문장만 읽어도 대략적인 흐름을 파악할 수 있어야 한다.

Kim et al., 2024에서 각 문단의 첫 문장만 추출해보면:

```
Paragraph 1: We conducted a quality control assessment for the WGS datasets...
Paragraph 2: We further aimed to identify autism-associated genes in autistic females and males separately...
Paragraph 3: Next, we calculated the PS for autism using the recent GWAS data...
```

각 문단의 첫 문장만 읽어도 "QC → 성별 특이적 유전자 → Polygenic score" 순서로 분석이 진행되었음을 알 수 있다.

## 용어 사용의 정확성과 일관성

**개념을 명확히 구분한다**

비슷해 보이는 용어들도 과학적으로는 다른 의미를 가진다. 정확하게 구분해서 사용해야 한다.

내가 Kim et al., 2024 논문을 작성할 때 학생에게 남긴 코멘트다:

> "이건 불필요한 설명이에요. 단순하게 genetic variant burden을 보겠다는게 아니라 마치 autosomal의 burden을 보겠다는 의도 같구요. 그리면 이 색션의 첫 부분에는 sex-chromosome만 보는 비교가 나와야하는거죠."

> "그리고 나서 inherited risk를 보고, 마지막으로 polygenic risk를 보겠다고 하고, PRS를 들어가면 됩니다."

**Genetic variant burden vs Autosomal burden**
- Genetic variant burden: 모든 유전 변이의 부담
- Autosomal burden: 상염색체의 부담 (성염색체 제외)

섹션에서 autosomal burden을 보겠다고 하면, 그 전에 sex-chromosome 비교가 먼저 나와야 논리적이다.

**Inherited risk vs Polygenic risk**
- Inherited risk: 부모로부터 물려받은 위험도 (de novo 제외)
- Polygenic risk: 많은 유전자의 작은 효과가 합쳐진 위험도

이 두 개념을 순차적으로 다루어야 한다.

**De novo variants vs Rare variants**

차이를 명확히 하고 일관되게 사용해야 한다.

**Kim et al., 2024가 잘한 점:**

논문 전체에서 용어를 일관되게 사용한다:
- De novo variants (DNV)
- Polygenic score (PS)
- Protein-truncating variants (PTV)
- Missense variants (MIS)

한번 약어를 정의하면 논문 전체에서 동일하게 사용한다.

**용어를 통일한다**

한 논문 내에서 같은 개념을 다른 용어로 표현하면 독자가 혼란스러워한다.

**Fig vs Figure:**

> "Fig도 쓰는 것도 있고 Figure로 쓰는것도 있는데, 통일을 시켜주면 좋겠습니다."

**Cell subtype vs Molecular subtype vs Genomic subtype:**

> "바로 아래 문단에는 'molecular subtype'이라는 표현을 썼고, 여기는 그냥 'subtype'인데, 통일을 하면 좋겠습니다."

> "저는 molecular subtype은 아닌것 같아요. 왜냐면, RNA, protein expression을 측정한건 아니니까요. 그래서 genomic subtype이라는 표현을 쓰는게 좋을것 같아요."

논문 초반에 용어를 정의하고, 그 용어를 일관되게 사용해야 한다.

**한 문장에 너무 많은 내용 담지 않기**

복잡한 개념을 한 문장에 우겨넣으면 독자가 이해하기 어렵다.

내가 Kim et al., 2024 작성 시 학생에게 남긴 코멘트:

> "바로 직전 문장에서 attention issue와 genetic association 이야기를 하는데 왜 갑자기 여기서 ADHD-like phenotypes이 나오는거죠... 문장이 이해가 안됩니다.."

각 개념을 개별 문장으로 풀어서 설명하는 것이 좋다.

## 특수한 경우들: 연구 유형별 구조 설계

**Sex-bias 연구: 제목과 내용의 일관성**

논문 제목이 특정 주제(예: sex bias)를 다룬다면, Results도 그 흐름을 유지해야 한다.

내가 학생에게 남긴 코멘트 (위에서 인용한 것과 동일):

> "여기도 마찬가지인데, 논문의 제목도 'sex-bias'이고, 첫 섹션도 'sex bias in Korean ASD'로 시작했는데요. 갑자기 2번째, 3번째 섹션에서 뜬금없이 genetic variant association을 이야기합니다."

독자와 editor는 제목을 보고 특정 내용을 기대한다. Results가 그 기대에서 벗어나면 혼란스러워한다.

**Kim et al., 2024가 잘한 점:**

논문 제목에 "sex differences"가 있고, 5개 Results 섹션 중 4개가 직접적으로 sex differences를 다룬다. 첫 번째 섹션(Overview)조차도 male-to-female ratio를 명시적으로 보고한다.

**Subtype 분석: 정의를 먼저 명확히**

Subtype을 다룰 때는 용어 정의가 특히 중요하다.

내가 학생에게 남긴 코멘트들:

> "Clinical이 아니라 phenotype이 아닐지?"

> "바로 아래 문단에는 'molecular subtype'이라는 표현을 썼고, 여기는 그냥 'subtype'인데, 통일을 하면 좋겠습니다."

> "저는 molecular subtype은 아닌것 같아요. 왜냐면, RNA, protein expression을 측정한건 아니니까요. 그래서 genomic subtype이라는 표현을 쓰는게 좋을것 같아요."

**Subtype 종류:**
- **Genomic subtype**: 유전체 변이 기반
- **Molecular subtype**: 유전자/단백질 발현 기반  
- **Clinical/Phenotypic subtype**: 임상 증상 기반

어떤 기준으로 subtype을 나눴는지 명확히 정의하고, 일관되게 사용해야 한다.

**각 subtype의 특징을 구체적 수치와 함께**

Subtype을 제시했다면, 각각의 특징을 정량적으로 기술해야 한다.

좋은 예:
```
We identified four genomic subtypes. Cluster 1 was enriched for variants 
disrupting transcription factors such as FEZF2, ZBTB6, and ZNF454 (23 genes, 
adjusted p = 0.001), which are involved in early corticospinal neuron 
specification. Cluster 4 showed elevated burden of constrained noncoding 
variants (mean = 15.3) compared to other clusters (mean = 8.2, p < 0.001).
```

각 subtype이 무엇으로 구별되는지, 숫자로 명확히 보여주어야 한다.

**여러 cohort를 합쳤을 때**

여러 데이터셋을 통합한 경우, batch effect 처리와 품질 관리 결과를 간단히 언급하면 된다.

Kim et al., 2024의 예:
```
The Korean autism WGS data consists of 673 families of total 2,255 individuals, 
encompassing 21 multiplex families. The Korean autism cohort extensively collected 
deep phenotype data from these 673 families and an additional 826 families of 
1,475 individuals (total 1,499 families of 3,730 individuals).
```

자세한 방법은 Methods에, 결과만 Results에 간단히 제시한다.

## Figure와 Table의 효과적 배치

**본문에서 구체적으로 언급한다**

Figure나 Table을 언급할 때는 구체적인 정보와 함께 제시해야 한다.

잘못된 예:
```
Results are shown in Figure 2A.
```

올바른 예 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)):
```
In children with autism, de novo PTVs were observed more frequently in females 
than males in Korean cohort (RR = 2.0; 0.066 variants per female and 0.033 per 
male; P = 0.11), SSC (RR = 1.8; 0.104 per female case and 0.058 per male case; 
P = 1.1 × 10−2), and SPARK (RR = 1.2; 0.052 per female case and 0.045 per male 
case; P = 0.32) (Fig. 2C).
```

구체적인 숫자와 통계값을 본문에 제시하고, Figure는 시각적 확인을 위해 인용한다.

**순서대로 언급한다**

Figure와 Table은 본문에 등장하는 순서대로 번호를 매겨야 한다.

Figure 1A, 1B, 1C 순서로 언급하다가 갑자기 Figure 3을 언급하면 안 된다.

**Kim et al., 2024의 Figure 배치:**

```
Results 섹션 1: Fig. 1A, 1B, 1C (Overview)
Results 섹션 2: Fig. 2A, 2B, 2C, 2D, 2E, 2F (Genetic burden)
Results 섹션 3: Fig. 3A, 3B, 3C, 3D (ID and symptom severity)
Results 섹션 4: Fig. 4A, 4B (Male-to-female ratio)
Results 섹션 5: Fig. 5A, 5B, 5C, 5D, Fig. 6A, 6B, 6C (Family analysis)
```

논리적인 순서로 배치되어 있다.

**Figure 내용이 본문과 일치해야 한다**

내가 학생에게 남긴 코멘트:

> "히트맵하고 이 부분의 서술이 매칭이 안됩니다. 여기서는 GO 결과 같은게 들어간 것 같은데 (제가 이해한게 맞다면), 그런 부분이 히트맵에 표시가 되어야 할 것 같아요."

본문에서 설명한 내용이 Figure에서 시각적으로 확인 가능해야 한다.

**Supplementary vs Main Figure**

저널의 가이드라인을 확인해야 한다.

> "투고하려는 논문 사이트에서 author guideline 확인해주세요. Supplementary Figure 라고 쓰는지 Figure S 라고 쓰는지 확인을 해주세요."

일반적으로:
- **Main Figure**: 핵심 발견
- **Supplementary Figure**: 보조 데이터, 검증 실험, 추가 분석

Kim et al., 2024의 경우:
- Main Figures (1-6): 주요 발견들
- Supplementary Figures (S1-S8): Power calculation, 추가 분석, 검증 결과

## 인용(Citation)의 적절한 사용

**Previous studies 언급 시 반드시 인용**

다른 연구의 결과를 언급할 때는 항상 인용이 필요하다.

내가 자주 남기는 코멘트:

> "Previous studies 나 finding이 들어가면 citation이 있어야 해요."

> "Reference??"

잘못된 예:
```
As previously documented, DNV genes were associated with transcriptional 
regulation and synaptic transmission.
```

올바른 예 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)):
```
Consistent with existing findings [6, 7, 55, 56], de novo PTVs were found 
to be significantly enriched in children with autism in both Korean and 
replication cohorts (Fig. 2B).
```

**본인의 발견도 명확히 표시**

본인의 새로운 발견인지, 기존 연구의 재확인인지 명확히 해야 한다.

새로운 발견:
```
We identified three novel subtypes characterized by distinct noncoding 
regulatory profiles.
```

기존 연구의 확인 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)):
```
In line with previous findings [58], we observed an average twofold higher 
proportion of individuals with a de novo PTV among autism cases with ID 
compared to those without ID in both females and males (Fig. 3A).
```

## 저널별 요구사항 확인

**Author guideline 숙지**

투고 전에 반드시 저널의 가이드라인을 읽어야 한다.

내가 학생들에게 자주 하는 말:

> "투고하려는 논문 사이트에서 author guideline 확인해주세요."

확인할 사항:
- Results 섹션의 길이 제한
- Figure와 Table 개수 제한
- Supplementary Material 형식
- 인용 스타일
- 약어 사용 규칙

**워드 파일의 오류 수정**

제출 전에 기본적인 것들을 확인해야 한다.

> "워드에서 파란색으로 표시된 부분을 확인하고 수정이 필요하면 미리 해주세요. 마우스 오른쪽 버튼을 누르면 자동 고칠 제안을 해줍니다"

맞춤법, 문법 오류를 모두 수정하자.
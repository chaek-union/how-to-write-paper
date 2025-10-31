# 5장. Results 섹션을 작성하기

하나의 Result 섹션 안에서, 심지어 한 문장 안에서 어떻게 효과적으로 쓸 것인가에 대해 알아보자. 좋은 구조를 가진 Results도 문장이 명확하지 않으면 독자에게 전달되지 않는다. 이 장에서는 실제 우리 학생들이 작성한 논문에 남겼던 코멘트를 바탕으로, 문장 레벨의 작성 기술을 다룬다.

---

## Results 섹션의 문단 구조 — 유기적 연결

Results의 하나의 섹션을 작성할 때, 보통 3-4개의 문단을 적는다. 그 문단들은 서로 유기적으로 연결된다. 

우리가 작성한 뇌발달 싱글셀 논문 [Kim et al. 2024, Exp Mol Med](https://pmc.ncbi.nlm.nih.gov/articles/PMC11541755/)의 "Cellular landscape of neurodevelopmental disorder genes in early neuronal lineages" 섹션을 예로 살펴보자.

**문단 1: 세포 특이적 enrichment 패턴**
```
Over the past decade, large-scale genomic studies have identified risk genes 
associated with neurological disorders... We prioritized 14 sets of genes 
previously reported to be associated with neurological disorders... Consequently, 
distinct patterns of gene enrichment were detected in a cell type-specific manner.
```

이 문단은 큰 그림을 제시한다. 어떤 disorder risk genes이 어떤 cell type에서 enriched 되어 있는지 보여준다.

**문단 2: Neuronal lineage의 궤적 분석**
```
We further investigated the cellular lineages underlying the neuronal clusters 
and the lineage-specific patterns of neurodevelopmental disorder risk genes. 
The pseudotime trajectory built on cellular identity reflected the clustering 
patterns of cells differentiating from radial glia to neuroblasts, eventually 
committing to mature neurons...
```

문단 1에서 "cell type-specific"이라고 했으니, 이제 더 깊게 들어간다. 단순히 어떤 cell type이 아니라, cell이 분화하는 **궤적(trajectory)** 상에서 어떻게 발현되는지를 본다.

**문단 3-5: 각 Lineage의 상세 분석**

Lineage 1 (excitatory neurons):
```
Lineage 1 represents a differentiation trajectory from radial glia to excitatory 
neurons... Among the autism risk genes, those involved in transcriptional 
regulation, such as RNASE1 and TCF7L2, are predominantly expressed in the early 
stages of this lineage...
```

Lineages 2 & 3 (inhibitory neurons):
```
Lineages 2 and 3 represented the differentiation trajectory from radial glia 
to inhibitory neurons, diverging into MGE-derived (C20) and CGE-derived (C23) 
neurons...
```

각 lineage마다 어떤 risk genes이 어느 시점에 발현되는지, 어떤 biological pathway가 enriched 되는지를 구체적으로 서술한다.

**논리적 흐름:**
1. 큰 그림: 어떤 cell type에서 risk genes이 enriched 되는가?
2. 중간 그림: 이 cell type들이 어떻게 분화하는가? (lineage)
3. 세부 그림: 각 lineage에서 언제, 어떤 genes이, 어떤 pathway와 함께 발현되는가?

**각 문단의 첫 문장이 어떻게 연결되는지 주목하자:**
- 문단 1: "We prioritized 14 sets of genes..."
- 문단 2: "We **further** investigated the cellular lineages..."
- 문단 3: "Lineage 1 **represents**..."
- 문단 4: "**Like lineage 1**, lineages 2 and 3 presented..."

"Further", "Like" 같은 연결어가 없어도, 논리적 흐름이 자연스럽게 이어진다. 각 문단이 이전 문단에서 던진 질문에 답하거나, 더 깊은 분석을 제공하는 구조다.

---

## AI를 활용하여 Results 섹션 작성하기

불과 수년전만 하더라도, 논문을 쓴다는 것은 매우 어려운 일이었다. 영어로 글쓰기를 해야하기도 했고, 과학 글쓰기를 해야했으니까... 요즘은 챗지피티, 클로드와 같은 AI 툴이 나와서, 영작의 난이도를 많이 낮추었다. 그래서 처음 논문을 쓰는 학생들에게 AI 도구를 활용하는게 도움이 된다.

**단계별 작성 프로세스**

**1단계: 문단 구조 설계 (3-4개 문단)**

먼저 한 섹션 안에 몇 개의 문단을 쓸지 구상한다. 보통 3-4개가 적당하다 (이와 같은 구상은 처음부터 완벽할 필요가 없다).

예시:
- 문단 1: Risk genes의 cell type-specific enrichment
- 문단 2: Pseudotime trajectory 전체 패턴
- 문단 3: Lineage 1 상세 분석
- 문단 4: Lineages 2 & 3 비교 분석

**2단계: 각 문단의 핵심 결과 나열 (4-5개)**

각 문단에 들어갈 주요 결과들을 논리적으로 4-5개 적는다. 문장으로 여러분이 직접 써도 되지만, 꼭 완전한 문장일 필요는 없다. 또한 연결을 어떻게 해야할지 너무 고민할 필요가 없다. 처음 논문을 쓰는 학생들은 문장간의 연결에 과도하게 많은 시간을 보낸다. 문장간의 연결은 AI 툴이 해준다. 혹은 문장들을 던져주고 나서, "논리적으로 연결이 안되는게 있었어?"라고 AI에게 물어보면서, 점검해도 된다. 

예시 (문단 3):
```
- Lineage 1은 radial glia에서 excitatory neuron으로 분화
- NEUROD6이 neuroblast에서 일시적으로 발현
- Autism risk genes (RNASE1, TCF7L2) early stage에 발현
- Developmental delay genes는 다른 시점에 peak (RAB14, MYCN later, FOXP2 postnatal)
- Wnt signaling pathway enriched (FDR = 4.79 × 10−2)
```

이러면 대략 12개에서 20개의 핵심 포인트가 나온다.

**3단계: AI로 문장 생성 및 검토**

AI 툴에게 이 포인트들을 바탕으로 문단을 작성하도록 한다.

```
Prompt 예시:
"아래 결과들을 바탕으로 논문 Results 섹션의 한 문단을 작성해주세요:
- Lineage 1은 radial glia에서 excitatory neuron으로 분화
- NEUROD6이 neuroblast에서 일시적으로 발현
- Autism risk genes (RNASE1, TCF7L2) early stage에 발현
..."
```

논리적으로 맞는지, 그리고 의도한대로 결과가 제시되었는지 여러 번 읽어보고 수정한다. 이 과정에 사람(당신)이 개입해야 한다. 어쩌면 이 작업이 가장 많은 시간이 걸릴지도 모른다. 처음 논문을 쓰는 학생에게 이 부분이 어렵다. 어떻게 쓰여진 것이 좋은 글인가? 마치 학생은 처음 농작물을 얻어본 농부와 같다. 그래서 본인이 수확한 것이 좋은 작물인지 아닌지 판별하는 능력을 키워야 한다. 이것에는 왕도가 없다. 내가 스스로 경험하고, 혹은 학생들의 결과물을 통해 경험한 것들을 적어본다.

먼저, AI는 결과를 설명하면서 해석을 종종 넣는다. 아래와 같은 경우이다. 

**잘못된 예:**
```
FOXP2 was highly expressed at the end of the lineage, particularly in the 
postnatal stage, **suggesting its critical role in late neuronal maturation 
and potentially contributing to autism pathogenesis through disruption of 
synaptic function**.
```

**올바른 예:**
```
FOXP2 was highly expressed at the end of the lineage, particularly in the 
postnatal stage.
```

해석("suggesting its critical role...")은 Discussion에 넣어야 한다. Results에서는 관찰한 사실만 적는다. 물론 논문에서 문장 뒤에 ",suggesting 무엇" 이렇게 풀어서 설명하는 경우가 종종 있다. 그러나 AI 툴은 과도하게 이런 작업을 한다. 그러다보니 Results의 문단들이 속도감 있게 전개되지 않고, 부수적인 해석들로 가득찬다.


또 한가지 GPT의 패턴이 있다. Results를 작성할 때, 마지막에 요약 문단을 생성한다. GPT가 자주 생성하는 마지막 문단:

```
Collectively, these results demonstrate that essential biological processes 
are dynamically regulated throughout neurodevelopment, highlighting the 
temporal specificity of differentiation.
```

또는:
```
Collectively, these results demonstrate that a foundation model trained and 
fine-tuned using the atlas enables the prediction of meaningful biological 
representations of gene perturbations, positioning it as a powerful 
resource for dissecting the functional consequences of genetic perturbations 
associated with NDDs.
```

이런 종합적 해석은 Discussion에 속한다. Results는 마지막 결과를 제시하고 끝내면 된다. 이와 같은 문장 형태가 종종 논문에 쓰인다. 개인적인 라이팅 방식이긴 하지만, 해석과 총론은 Discussion에 넣는 것을 권유한다. Results에서는 데이터가 말하게 하고, 데이터로 의미를 전달하게 문장이 쓰여야 한다. 

또 한가지 주의 할 점은, AI의 라이팅은 자주 "과장"하거나 "모호"하게 문장을 작성한다. 그럴듯하게 보이는 작업물을 전달한다. 그래서 프롬프트를 입력할 때 가급적 정량적인 지표, 정확한 구성요소들을 넣어야 한다 (특히 Results 파트에서). 또한 나온 결과물을 읽어보고, 모호한 언어로 작성했는지를 점검해야 한다. 혹은 나온 결과물을 다른 AI에게 넣어서, "이거 쟤네가 한건데, 혹시 모호하게 쓰여진 문장이나, 그럴듯하게 보이는 문장이 있어? 구체적인 정보를 얻을수 있어? 혹시 그런 부분이 있으면 지적해봐" 라고 물어볼수도 있다. 

---

## 문장 작성할 때 우리가 자주하던 실수들

### 중요한 결과를 여러 문장에 분산시키지 말자

한 문장에서 명확하게 전달하는 것이 훨씬 효과적이다.

내가 Kim et al., 2024 논문 작성 시 학생에게 남긴 코멘트다 ([Kim et al. 2024, Genome Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC11429951/)):

> "여기도 매번 반복되는 습관인데, 중요한 결과를 너무 여러 문장에 나눠서 씁니다. 너무 헷갈려요..."

> "바로 직전 문장에서 attention issue와 genetic association 이야기를 하는데 왜 갑자기 여기서 ADHD-like phenotypes이 나오는거죠... 문장이 이해가 안됩니다.."

잘못된 예:
```
Previous studies showed attention deficits. Genetic associations were found. 
ADHD-like phenotypes were observed in siblings.
```

올바른 예:
```
Siblings of autistic individuals showed ADHD-like phenotypes, including 
attention deficits that were genetically associated with polygenic burden 
(β = 0.23, p = 0.003).
```

하나의 핵심 발견은 하나의 명확한 문장으로 표현하자. 단, 한 문장에 관련 없는 여러 내용을 우겨넣지는 말자.

### 과도하게 세세하게 적는 학생들 (MBTI가 S 혹은 ST 인 경우들..)

MBTI가 S인 학생들이 자주 하는 실수가 있다. 관찰한 모든 디테일을 다 적으려고 하는 것이다.

한 학생에게 남긴 코멘트다:

> "처음 논문을 쓰다보면, 학생처럼 MBTI가 S인 친구들이 자주 하는 실수가, 분석하며 관찰한 모든 것을 다 적는 것인데요. 범죄 스릴러 드라마라고 생각해볼게요. 여기선 범행 → 사건 수사 → 전투씬 → 사건 해결 만 있으면 되겠죠? 사건 수사하면서 방문한 음식점의 역사를 소개한다든지, 메뉴를 소개한다든지 하는 이야기는 안 해도 됩니다. 이건 맛집 탐방 유튜브가 아니니까요. 논문도 마찬가지에요. 이 섹션에서 전하고 싶은 1가지 메시지가 무엇인가요? 그것만 생각하며 쓰면 됩니다."

**각 섹션, 각 문단의 핵심 메시지 하나에 집중하자.** 그 메시지를 전달하는 데 필요한 최소한의 정보만 제공하면 된다.

Kim et al., 2024 (Exp Mol Med)의 집중된 서술:

"Cellular landscape of neurodevelopmental disorder genes in early neuronal lineages" 섹션:
- 문단 1: Risk genes는 특정 cell type에서 enriched 된다
- 문단 2: Neuronal lineages는 발달 단계에 따라 diverge 한다
- 문단 3: Lineage 1 (excitatory)의 특징과 temporal pattern
- 문단 4: Lineages 2 & 3 (inhibitory)의 특징과 비교

불필요한 관찰은 모두 생략했다.

### 문장을 작성하다가 안드로메다로 여행한 학생들 (MBTI가 NP인 경우들...)

일부 학생들은 문장을 작성하고 전개할 때, 우주 밖으로 나가버린다. 

A > B > C > D 순서로 전개를 해야하는데, A > B > B' > B'' > Z (응???) > 가 (응?? 응??)

이런 친구들은 호기심이 많고 생각이 많다. 그래서 사실을 순차적으로 전달해야 하는 Results의 글쓰기에서 새로운 활로를 열어버린다. Z까지 가고 나면, 친구들을 다시 잡아서 돌아오기가 어렵다. 혹시 이글을 읽는 본인이 이런 경우라면 해결책이 있다.

1. 논문을 작성할 때, 작성하고자 하는 아이템 (피겨, 테이블, 데이터)를 마련하자.
2. 인터넷을 끈다. 인터넷을 끈다. 인터넷을 끈다 -> 호기심에 의한 검색을 원천 차단한다.
3. 논문을 작성한다. 완벽하지 않고, 마음에 들지 않을 것이다. 그러나 과거의 여러분보다 훨씬 빠른 속도로 글을 쓸 것이다. 확신한다. 


### 문장의 길이: 너무 짧지도, 너무 길지도 않게

핵심은 **하나의 주요 결과는 하나의 명확한 문장으로** 표현하는 것이다.

```
In children with autism, de novo PTVs were observed more frequently in females 
than males in Korean cohort (RR = 2.0; P = 0.11), SSC (RR = 1.8; P = 1.1 × 10−2), 
and SPARK (RR = 1.2; P = 0.32) (Fig. 2C).
```

이 문장은:
- **하나의 핵심 발견**: 여성에서 de novo PTV가 더 많다
- **세 cohort의 증거**: 한 문장에 효율적으로 제시
- **정량적 데이터**: 모든 숫자 포함


### 분석명이나 도구명을 주어로 쓰지 말자

이것은 학생들이 자주 하는 실수다. 학부생들에게 글쓰기를 가르칠 때도 자주 보이는 실수이다. 

- "Heatmap analysis revealed..."
- "The volcano plot showed..." -> Figure legend에서는 이렇게 쓸수 있으나, Results에서 써야 할 문장은 아니다. 
- "GO analysis demonstrated..."
- "Our differential expression analysis found..."
- "The Seurat analysis showed..." (Seurat은 싱글셀 분석 툴)

대신 이렇게:
- "Gene expression differed significantly between..."
- "Among 500 genes tested, 45 showed..."
- "Enriched pathways included synaptic transmission and..."

Seurat, DESeq2, GSEA 같은 툴 이름은 Methods에 적으면 된다. 만약 여러분이 Seurat 툴의 개발자라면, 써도 된다. 근데 그런 게 아니니까... Results에서는 발견한 사실만 간결하게 전달하자.

### 처음 논문을 쓰는 학생들은 너무 자주 놀라고, 너무 자주 주목한다.... 

학생들의 논문을 보면 GPT가 생성한 듯한 표현들이 많다. 특히 "Altogether", "Together", "Notably", "Surprisingly" 같은 부사어를 과도하게 사용한다. 실제로 한 학생의 논문에서 내가 삭제 표시한 것들:

삭제한 표현들:
- "Altogether, the Core and Extended Atlas constitute..."
- "Together, these findings demonstrate..."
- "Notably, both OligoEUR and OligoEAS exhibited..."
- "Surprisingly, these models achieved..."
- "In particular, telencephalic neurons exhibited..."
- "Furthermore, the NOCAP contains..."

이런 표현들은 대부분 불필요하다. 없어도 문장의 의미는 그대로 전달된다.

**수정 전:**
```
Altogether, the Core and Extended Atlas constitute a comprehensive NOCAP 
annotated across hierarchical cell-type levels, designed to provide a robust 
and integrated atlas, providing the foundation for all subsequent analyses.
```

**수정 후:**
```
The Core and Extended Atlas constitute a comprehensive NOCAP annotated across 
hierarchical cell-type levels (Figure 1E).
```

훨씬 간결하고 명확하다. "Notably"나 "Surprisingly" 없이도 충분히 강력한 문장이다. 결과 자체가 "놀라움"을 전달한다. 한국 학생들은 부사를 많이 쓴다. 우리나라의 말투에도 그런 습관이 많다. 

한 학생 논문에 내가 남긴 코멘트:

> "[중요] 여기서부터 연결어와 부사, 불필요한 수사들을 삭제했습니다. 제가 삭제한 부분을 읽어보고, 의미가 제대로 전달되는지 확인해주세요. 왜 이 정도는 생략해도 되냐면, '결과(숫자)'를 보여주기 때문입니다. 만약 읽었을 때 속도감 있게 잘 읽혔는데, 뭔가 부족하다고 느껴지면, '결과(숫자)'를 더 보여주세요."

불필요한 수사를 제거하고 나면, 정작 **정량적 결과(숫자)**가 부족하다는 것을 깨닫게 된다. 그때 숫자를 채워 넣으면 된다.

### 과정 중심 동사 줄이기

"established", "optimized", "benchmarked" 같은 과정 중심 동사도 Results에서는 최소화하자.

한 학생 논문의 예:
```
To optimize the Core Atlas integration, we benchmarked batch correction methods 
using established evaluation metrics, effectively minimizing batch effects while 
preserving biological variation.
```

이것은 Method에 들어갈 내용이다. Results에서는:

```
The Core Atlas resulted in approximately 1.4 million high-quality cells 
(Figure S1B).
```

결과만 간단히 제시하면 된다.

### 순환 구조 문장 피하기 (feat. 펀쿨섹좌)

학생들이 문장을 적을 때 자주 하는 실수가 있다. 잘못된 예 (순환 구조):

```
To find differentially expressed genes, we performed differential expression 
analysis. As a result, we observed differentially expressed genes between 
groups.
```

이 문장의 문제점:
1. "To find A"라고 시작
2. "we performed B" (B는 A를 찾기 위한 분석)
3. "we observed A" (결국 A를 찾았다)

이건 내용이 없는 문장이다. 당연히 differential expression analysis를 하면 differentially expressed genes를 찾는 거다. "To find A, we did B. We found A" 구조는 피하자. 바로 "We found A"로 시작하거나, "A differed/showed/exhibited" 같은 직접적 표현을 쓰자.

### 줄임말에 대하여

Academic writing에서는 축약형(contractions)을 쓰지 않는다.

내가 학생에게 남긴 코멘트:

> "Academic writing에선 줄임말을 쓰지 않습니다..."

잘못된 예:
- can't → cannot
- don't → do not
- it's → it is
- isn't → is not
- doesn't → does not

단, 표준 약어(acronyms)는 사용 가능하다:
- DNA, RNA, PCA, GSEA, GO (이런 것들은 OK)

내가 말하는 "줄임말"은 isn't나 doesn't 같은 축약형(contractions)이다. 실제 전문 용어들은 당연히 줄여서 쓴다.

### 단어 선택의 정확성

Results와 Discussion에서 사용하는 동사가 다르다.

Results에 적합한 동사:
- showed, demonstrated, revealed
- indicated, suggested (약한 주장)
- differed, increased, decreased
- assessed, evaluated, examined, tested

Discussion에 적합한 동사:
- speculate, hypothesize (추측)
- implies, suggests (해석)
- may, might, could (가능성)

내가 학생에게 남긴 코멘트:

> "잘 쓰지 않는 말... 추측하는 것보다 assess, evaluate, investigate 등 이런 평가한 단어를 쓰는 게 좋습니다. 추측은 너무 강한 말이에요."

### 수동태 vs 능동태 

상황에 따라 적절히 선택해야 한다.

Results에서 능동태 (우리가 한 분석이나 찾은 것):
```
We examined 500 samples...
We performed differential expression analysis...
We identified three distinct lineages...
```

Results에서 수동태 (사전 연구에서 등장한 결과들):
```
Samples were clustered into three groups...
Genes were annotated using...
```

나는 Results에서 문장을 쓸 때, "We performed", "We found", "We observed"와 같은 능동태 문장을 쓴다. 꼭 수동태일 필요는 없다. 우리가 찾은 것, 우리가 실험한 것을 말하는 것이니까. 다만 다른 연구자들이 찾은 결과들을 언급할 때는 "Sanders et al. found" 이런 식의 능동태 문장은 쓰지 않는다. 다른 연구나 결과를 언급할 땐 수동태로 쓴다:

```
It was previously reported that... [1]
De novo variants have been shown to... [2,3]
```

이건 내가 주로 하는 라이팅 스타일이고, 이런 문장 방식은 사람마다 다를 수 있다.

능동태:
```
We conducted a quality control assessment for the WGS datasets...
We identified distinct neuronal lineages...
```

수동태:
```
Risk genes for neurodevelopmental disorders, including autism, developmental 
delay, and epilepsy, are predominantly expressed in neuronal cell types.
```

다른 연구 언급 (수동태):
```
De novo variants in autism have been shown to disrupt neuronal genes... [5]
```

### 인용(Citation)의 적절한 사용

**Previous studies 언급 시 반드시 인용**

다른 연구의 결과를 언급할 때는 항상 인용이 필요하다. 내가 Kim et al., 2024 작성 시 자주 남기는 코멘트다:

> "Previous studies 나 finding이 들어가면 citation이 있어야 해요."

> "Reference??"

잘못된 예:
```
As previously documented, DNV genes were associated with transcriptional 
regulation and synaptic transmission.
```

올바른 예:
```
As previously documented, DNV genes were associated with transcriptional 
regulation and synaptic transmission [2, 16, 21].
```

```
The autism and developmental delay risk genes were considerably enriched in 
both excitatory and inhibitory neuronal cell types, which is consistent with 
previous findings [24-26].
```

```
De novo variants in autism disrupt neuronal genes that are overexpressed in 
the prefrontal cortex during the mid-fetal period [5], indicating that risk 
perturbation at the molecular level precedes its clinical onset [6].
```

**본인의 발견도 명확히 표시**

본인의 새로운 발견인지, 기존 연구의 재확인인지 명확히 해야 한다.

**새로운 발견:**
```
We identified three distinct lineages diverged from radial glia and 
differentiated into excitatory and inhibitory neurons.
```

**기존 연구의 확인:**
```
Consistent with previous reports [23], we observed enrichment in synaptic genes.
```

**Citation 형식 통일**

저널마다 인용 스타일이 다르다. 한 논문 내에서는 일관되게 유지해야 한다. 내가 학생에게 남긴 코멘트:

> "투고하려는 논문 사이트에서 author guideline 확인해주세요. Supplementary Figure라고 쓰는지 Figure S라고 쓰는지 확인을 해주세요"

인용 스타일:
- **위첨자**: text²,³,⁴
- **괄호**: text [2, 3, 4]
- **Author-year**: text (Smith et al., 2020)

**Kim et al., 2024는 괄호 스타일 [숫자]를 일관되게 사용한다.**

---

## Results 문장을 작성할 때, 확인해야 하는 것

### 통계값은 필수

"significantly enriched"라고만 쓰지 말자. 항상 구체적인 수치를 제공해야 한다.

잘못된 예:
```
Gene expression was significantly higher in cases than controls.
```

올바른 예:
```
Gene expression was significantly higher in cases than controls (fold change = 2.3, 
p = 0.001, t-test, two-sided, n = 500).
```

Kim et al., 2024 (Genome Medicine)의 좋은 예:
```
In line with previous findings [58], we observed an average twofold higher 
proportion of individuals with a de novo PTV among autism cases with ID compared 
to those without ID in both females and males (Fig. 3A; Additional file 6: Table S5).
```

"twofold higher"라는 구체적 수치를 제시한다.

또 다른 예:
```
Male siblings had significantly higher scores for seven out of nine clinical 
phenotypes related to autism core symptoms (total symptom severity, social 
communication and restricted interest and repetitive behaviors) and significantly 
lower scores for five out of seven cognitive/adaptive behaviors than female 
siblings (Fig. 5C; Additional file 8: Table S7).
```

"seven out of nine", "five out of seven"로 정량화했다.

> "그리고 특정 pathway가 어느 시점에 x fold 만큼 올라갔고 내려갔는지 등등에 대한 정량적인 값이 있어야 할 것 같아요. 예를들어서, (Figure 1B). In particular, [pathway name] were significantly increased in [group] (XX fold, p=XXX, t-test, two-sided). 이런식으로 넣어야 합니다."

### 유효숫자 통일

저널마다 유효숫자 규정이 다르다. 한 논문 내에서는 일관되게 유지해야 한다.

일반적으로:
- p-value: 소숫점 2-3자리 (p = 0.001 또는 p = 1.1 × 10−2)
- effect size나 fold change: 소숫점 1-2자리 (RR = 2.0, fold change = 2.3)
- 백분율: 정수 또는 소숫점 1자리 (65%, 5.6%)

### 샘플 수 명시

통계 분석 결과를 제시할 때는 항상 샘플 수를 명시해야 한다.

```
We analyzed samples from the top 5 brain regions by sample size (cortex: n=342, 
hippocampus: n=198, cerebellum: n=156, striatum: n=89, midbrain: n=67).
```

내가 학생 논문에 남긴 코멘트:

> "샘플 수가 많은 순서대로 상위 5개 region과 샘플수 n=XX로 표시"

Kim et al., 2024 (Genome Medicine)의 예:
```
The Korean autism WGS data consists of 673 families of total 2,255 individuals, 
encompassing 21 multiplex families with more than two autistic children.
```

```
Of the 696 individuals with autism, 590 were males and 106 were females 
(5.6 male-to-female ratio). Siblings included 90 male and 123 female individuals 
(0.74 male-to-female ratio).
```

모든 그룹의 샘플 수가 명확하다.

### "higher", "lower", "enriched" - 정량적 근거 필요

비교 표현을 사용할 때는 반드시 정량적 근거를 제시해야 한다.

잘못된 예:
```
Oligogenic genes showed enrichment in synaptic transmission, comparable to 
DNV genes.
```

올바른 예:
```
Oligogenic genes showed enrichment in synaptic transmission (GO:0007268, 23 genes, 
adjusted p = 0.002), comparable to DNV genes (GO:0007268, 31 genes, 
adjusted p = 0.001).
```


### 사용한 통계 방법을 명시할 것

어떤 통계 검정을 사용했는지 항상 명시해야 한다. 저널마다 가이드라인이 있으니, 가이드라인을 확인하여 입력하길 바란다.

```
Groups differed significantly (p = 0.003, T-Test, Two-sided).
```

```
Proportions were compared using Fisher's exact test (p = 0.012).
```

```
We performed permutation testing (1,000 iterations) to assess significance.
```


### Non-significant 결과도 언급한다

통계적으로 유의하지 않은 결과도 값을 표기한다

```
Although we tested for differences in PRS between groups, no significant 
association was observed (p = 0.24, n = 500).
```

```
Sex ratios were similar across subtypes (p = 0.31, chi-square test).
```


### 비교 대상을 명확히

무엇과 무엇을 비교했는지 명확해야 한다.

애매한 표현:
```
De novo variants showed higher burden. (<- 무엇과 비교하여 higher?)
```

명확한 표현:
```
De novo variants showed higher burden in cases (mean = 2.3) compared to 
controls (mean = 0.8, p < 0.001, t-test).
```

```
In children with autism, de novo PTVs were observed more frequently in females 
than males in Korean cohort (RR = 2.0; 0.066 variants per female and 0.033 per 
male; P = 0.11).
```

누구와 누구를 비교했는지, 각각의 값이 무엇인지 모두 명확하다.


### "Significant"라는 용어를 사용할 때 - 통계적 의미

"Significant"는 과학 논문에서 특별한 의미를 가진다.

내가 Kim et al., 2024 작성 시 학생에게 남긴 코멘트다:

> "한 문장에 너무 많은 내용이 있지 않나요? 두 개는 다른 표현형이고, 각기 따로 설명을 할애할 수 있을 것 같아요."

> "그리고 'significant'를 말하면 통계값이 제시되어야 하는데요. 이런 것 포함. 투고하고자 하는 저널에 나온 다른 논문들 보고 포맷을 파악해보세요. 어떤 어떤 내용들이 들어가야 할지.."

통계적 유의성을 말할 때:
```
Expression was significantly higher in cases (p < 0.05, t-test).
```

일반적 중요성을 말할 때:
```
This finding is particularly important because...
```

또는:
```
This represents a notable difference from previous studies.
```

"Significant"를 통계적 의미로만 사용하고, 일반적 중요성은 "important", "notable", "substantial" 등으로 표현하자.


통계적으로 유의할 때:
```
Male siblings had significantly higher scores for seven out of nine clinical 
phenotypes related to autism core symptoms (p < 0.05).
```

일반적 중요성:
```
This finding is important for understanding sex-differential liability in autism.
```





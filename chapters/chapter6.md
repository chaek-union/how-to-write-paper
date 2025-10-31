# 6장. Methods — 첫 논문 글쓰기의 튜토리얼 단계

Methods 섹션은 논문에서 가장 '기계적'으로 쓸 수 있는 부분이다. Introduction이나 Discussion처럼 창의적인 서술이 필요한 것도 아니고, Results처럼 발견을 어떻게 표현할지 고민할 필요도 없다. 그저 **여러분이 무엇을 했는지를 정확하고 빠짐없이 기록**하면 된다.

그래서 나는 처음 논문을 쓰는 학생들에게 Methods부터 쓰라고 권한다. 다른 사람의 논문에서 비슷한 분석 방법을 찾아 문장 구조를 참고하고, 여러분의 연구에 맞게 숫자와 파라미터만 바꾸면 된다. 일종의 튜토리얼 단계라고 생각하면 된다.

하지만 '기계적'이라고 해서 아무렇게나 써도 되는 건 아니다. Methods가 부실하면 논문 전체의 신뢰도가 무너진다. 독자가 여러분의 결과를 재현할 수 없고, reviewer가 분석의 타당성을 검증할 수 없기 때문이다. 이 장에서는 Methods의 각 요소를 어떻게 구성하고 작성하는지 단계별로 정리한다.

---

## 연구 설계와 환자 모집

Methods의 첫 절은 보통 연구 설계와 대상자 모집으로 시작한다. 여기서 명확히 해야 할 것들이 있다.

**연구 목적, 코호트 구성, 윤리 승인**부터 적는다. IRB 승인 번호와 날짜, 동의서 취득 방식을 빠뜨리지 말자. 이건 단순한 형식이 아니라 연구의 윤리적 정당성을 보여주는 필수 요소다.

**포함·제외 기준**을 구체적으로 적어야 한다. "자폐 스펙트럼 장애 환자를 모집했다"고만 쓰면 안 된다. 어떤 진단 기준을 사용했는지, 연령 범위는 어떻게 되는지, 다른 공존 질환이 있는 경우는 포함했는지 제외했는지를 명시해야 한다.

**임상 변수 정의**도 중요하다. 분석에 직접 사용되는 변수(예: 나이, 성별, 진단, 병기, 인지 평가 점수)를 중심으로 정리한다. 이런 데이터는 임상팀으로부터 미리 표준화된 형태로 확보해두는 것이 좋다. 나중에 "이 환자 병기가 뭐였지?" 하고 찾아 헤매는 일이 없도록.

**예시 문장:**

```
This study included 512 individuals diagnosed with autism spectrum disorder and 
325 unaffected controls recruited under IRB approval (protocol #2020-0567). 
Written informed consent was obtained from all participants or legal guardians. 
Clinical characteristics such as age, sex, diagnostic category, and cognitive 
assessment scores were obtained from medical records (Table S1).
```

이 문장은:
- 샘플 수 (512 cases, 325 controls)
- IRB 번호 (#2020-0567)
- 동의서 취득 방식 (written informed consent)
- 수집한 임상 변수 (age, sex, diagnostic category, cognitive scores)
- 데이터 출처 (medical records)
- 상세 정보 위치 (Table S1)

모든 필수 정보를 담고 있다.

---

## 시료 수집 및 데이터 생산

대부분의 오믹스 연구에서는 혈액, 조직, 세포 등의 생물학적 시료로부터 DNA, RNA, 또는 단백질을 추출한다. 이 절에서는 실험 프로토콜의 모든 세부사항을 적을 필요는 없다. **데이터 종류, 생산 기관, 품질 지표**를 중심으로 간결하게 쓰면 된다.

**시료 채취 방법**을 간단히 적는다. 어떤 튜브에 담았는지(EDTA, heparin), 어떤 온도에서 보관했는지(-80°C, -20°C) 정도면 충분하다. 

**데이터 생산 절차**도 핵심만 적는다. 시퀀싱 플랫폼(Illumina NovaSeq, PacBio 등), read 길이(2×150 bp, 2×100 bp), 평균 커버리지(30×, 50×)를 명시한다. 사용한 키트가 있다면 회사명과 제품명도 적는다.

**품질 지표**는 반드시 포함한다. Q30(quality score 30 이상인 read의 비율), read depth, mapping rate 같은 기본 지표를 보고한다.

**예시 문장:**

```
Peripheral blood samples were collected in EDTA tubes and stored at −80°C. 
Genomic DNA was extracted using QIAamp DNA Mini Kit (QIAGEN) and sequenced on 
Illumina NovaSeq 6000 (2×150 bp). Mean coverage was 30× with Q30 ≥ 85%.
```

이렇게 몇 문장이면 충분하다. 실험 노트처럼 "DNA를 추출하고 농도를 측정하고 희석하고..."를 다 적을 필요는 없다.

---

## 데이터 품질관리(QC)

QC는 데이터 생성 직후 시행하는 가장 중요한 절차다. 오믹스 논문에서는 별도의 절로 다루는 것이 일반적이다. 왜냐하면 QC가 부실하면 그 뒤의 모든 분석이 무의미해지기 때문이다.

**주요 QC 항목을 데이터 종류별로 정리하면:**

**WGS/WES QC:**
- Contamination (FREEMIX 값)
- Call rate (성공적으로 genotype이 결정된 비율)
- Depth (평균 커버리지)
- Duplicates (중복 read 비율)
- Sex concordance (유전적 성별과 보고된 성별 일치 여부)

**RNA-seq QC:**
- RIN (RNA Integrity Number)
- Mapping rate (reference에 align된 read 비율)
- %rRNA (ribosomal RNA contamination)
- Gene detection 수 (발현이 검출된 유전자 수)

**샘플 수준 QC:**
- Ancestry (PCA로 확인한 유전적 ancestry)
- Kinship (가족 관계 확인, 예상치 못한 친척 관계 제거)
- Phenotype consistency (임상 데이터와 유전 데이터 일치 여부)

**QC 기준과 제외된 샘플 수를 구체적으로 기재**해야 한다. "품질이 낮은 샘플을 제거했다"고만 쓰면 안 된다. 어떤 기준으로, 몇 개를 제거했는지 명확히 해야 한다.

**예시 문장:**

```
Samples with mean coverage <20× or contamination (FREEMIX) >0.05 were excluded. 
RNA libraries with RIN <6.0 or mapping rate <80% were also removed. After QC, 
174 WGS and 169 RNA-seq samples remained for downstream analysis.
```

이 문장은:
- WGS QC 기준 (coverage <20×, FREEMIX >0.05)
- RNA-seq QC 기준 (RIN <6.0, mapping rate <80%)
- QC 후 남은 샘플 수 (174 WGS, 169 RNA-seq)

모든 결정이 투명하게 기록되어 있다.

---

## 데이터 처리 및 정렬

이 절은 정렬, 변이 호출, 정제의 전 과정을 기술하는 부분이다. 오믹스 분석을 하는 사람이라면 이미 익숙한 파이프라인일 것이다.

**Reference genome과 annotation 버전**을 반드시 명시한다. GRCh37인지 GRCh38인지, GENCODE v38인지 v105인지에 따라 결과가 달라질 수 있다.

**사용된 알고리즘 및 소프트웨어 버전**도 정확히 적는다. BWA-MEM v0.7.17, GATK v4.2.0처럼 버전까지 포함한다. 재현성을 위해 필수적이다.

**공통 문장은 표준 파이프라인을 참고**해도 좋다. GATK Best Practices나 nf-core 파이프라인 문서에서 Methods 문장을 가져와 여러분의 분석에 맞게 수정하면 된다. 이건 표절이 아니다. 표준 절차를 표준 방식으로 기술하는 것이다.

**변이·유전자 단위의 필터 기준**도 포함한다. MAF(minor allele frequency), call rate, Hardy-Weinberg equilibrium p-value 같은 기준을 명시한다.

**예시 문장:**

```
Reads were aligned to GRCh38 using BWA-MEM v0.7.17. Duplicates were marked and 
base quality was recalibrated using GATK v4.2.0. Joint genotyping was performed 
following GATK Best Practices. Variants with call rate <90%, MAF <0.01, or 
Hardy–Weinberg p < 1×10⁻⁶ were excluded. Variant annotation was conducted using 
Ensembl VEP v105 with GENCODE v38.
```

이런 문장은 다른 논문에서 비슷한 구조를 찾아 참고하면 쉽게 쓸 수 있다. 중요한 건 여러분의 파라미터를 정확히 기록하는 것이다.

---

## 통계 분석 및 모델링

통계 분석 절에서는 **분석 단위, 사용된 모델, 공변량**을 명확히 해야 한다.

**분석 단위**가 무엇인지 적는다. Variant-level인지, gene-level인지, sample-level인지에 따라 분석 방법이 완전히 다르다.

**사용된 모델**을 명시한다. 선형 회귀(linear regression), 로지스틱 회귀(logistic regression), 혼합 모델(mixed-effects model) 등 어떤 모델을 사용했는지 적는다.

**공변량(covariates)**을 빠짐없이 나열한다. 나이, 성별, ancestry principal components, batch effects 등 모델에 포함된 모든 변수를 적어야 한다. 이게 빠지면 분석의 타당성을 검증할 수 없다.

**다중비교 보정 방식**도 명시한다. FDR(False Discovery Rate), Bonferroni correction, permutation-based correction 중 무엇을 사용했는지, 임계값은 얼마로 설정했는지(FDR < 0.05, p < 2.5 × 10⁻⁶) 적는다.

**분석 소프트웨어와 버전**도 기재한다. R v4.3.0, PLINK v2.0, Python v3.9 등을 명시한다.

필요한 경우 **모델 검증 방법**도 적는다. Cross-validation, permutation testing, genomic control λ 같은 것들이다.

**예시 문장:**

```
Association tests were performed using a linear mixed model adjusting for sex, 
age, and the first five ancestry principal components. Multiple testing was 
controlled using the Benjamini–Hochberg procedure (FDR < 0.05). Statistical 
analyses were conducted in R v4.3.0 and PLINK v2.0.
```

이 문장은:
- 모델 종류 (linear mixed model)
- 공변량 (sex, age, 5 PCs)
- 다중비교 보정 (Benjamini-Hochberg, FDR < 0.05)
- 사용 소프트웨어 (R v4.3.0, PLINK v2.0)

필요한 정보를 모두 담고 있다.

---

## Gene Set Enrichment에 대한 작성 요령

유전자 목록을 만들고 functional enrichment를 수행했다면, 이 과정도 Methods에 상세히 기술해야 한다.

**Gene list 구축 기준**을 명확히 한다. 통계 임계값(FDR, log2 fold change 등)과 필터링 단계를 명시한다. "유의미한 유전자를 선택했다"고만 쓰면 안 된다. FDR ≤ 0.05인지, |log2FC| ≥ 1인지 구체적으로 적어야 한다.

**Gene ID 변환 규칙**도 적는다. Ensembl gene ID를 HGNC symbol로 어떻게 변환했는지, unmapped된 유전자는 몇 개인지, 어떤 버전의 annotation을 사용했는지 기재한다.

**Enrichment 분석의 세부사항**을 포함한다:
- 사용한 데이터베이스 (GO, KEGG, Reactome)
- 배경 유전자 집합 (전체 유전체? 발현된 유전자만?)
- Gene set 크기 제한 (10-2000 genes)
- 다중검정 보정 방식 (FDR, Bonferroni)
- 사용한 패키지와 버전 (gProfiler, enrichR, clusterProfiler)

**예시 문장:**

```
Differentially expressed genes (FDR ≤ 0.05, |log2FC| ≥ 1) were mapped to 
Ensembl release 105 using biomaRt. Functional enrichment was tested using 
gProfiler (GO Biological Process, 10–2000 genes) with 10,000 permutations 
and Benjamini–Hochberg FDR correction.
```

이 문장은:
- DEG 정의 (FDR ≤ 0.05, |log2FC| ≥ 1)
- ID 매핑 (Ensembl 105, biomaRt)
- Enrichment tool (gProfiler)
- DB 종류 (GO Biological Process)
- Gene set 크기 (10-2000)
- Permutation 횟수 (10,000)
- 보정 방식 (Benjamini-Hochberg FDR)

모든 파라미터가 재현 가능하도록 기록되어 있다.

---

## 재현성 및 데이터·코드 가용성

현대 과학 논문에서는 재현성이 무엇보다 중요하다. 저널에 따라서는 이 절이 필수인 경우도 많다.

**분석 환경**을 명시한다. Nextflow, Snakemake 같은 워크플로우 관리 도구를 사용했다면 버전을 적는다. 컨테이너 이미지(Docker, Singularity)나 conda 환경을 사용했다면 그것도 기록한다.

**원시 데이터 접근 경로**를 제공한다. 데이터를 공개 저장소(dbGaP, EGA, GEO 등)에 기탁했다면 accession number를 명시한다. 개인정보 보호 때문에 공개할 수 없다면 "available upon reasonable request"라고 적을 수도 있지만, 가능하면 공개하는 것이 좋다.

**분석 코드 저장소**도 링크한다. GitHub, Zenodo DOI, Figshare 등에 코드를 올려두고 URL이나 DOI를 제공한다.

**부록 자료(Supplementary Tables)**를 명확히 연결한다. Table S1에 샘플 메타정보와 QC 지표가 있고, Table S2에 유전자별 통계 결과가 있다면 본문에서 언급해야 한다.

**예시 문장:**

```
All analyses were executed using Nextflow v22.10 with Singularity container 
(sha256:…). Source code and configuration files are archived at Zenodo 
(DOI:10.5281/zenodo.xxxxx). Raw and processed data are available through 
dbGaP accession phs003245.v1.p1. Sample metadata and QC metrics are 
summarized in Table S1.
```

이런 문장은:
- 워크플로우 도구 (Nextflow v22.10)
- 컨테이너 (Singularity, sha256)
- 코드 저장소 (Zenodo DOI)
- 데이터 저장소 (dbGaP accession)
- 부록 위치 (Table S1)

투명성과 재현성을 모두 확보한다.

---

## Methods를 쓸 때의 마음가짐

처음 논문을 쓰는 학생들에게 하고 싶은 말이 있다. Methods는 여러분이 한 일을 정직하게 기록하는 공간이다. 결과를 예쁘게 포장할 필요도 없고, 거창하게 만들 필요도 없다. 그저 **다른 연구자가 똑같이 따라 할 수 있도록** 충분히 상세하게 쓰면 된다. 다른 논문의 Methods를 참고하는 것은 전혀 문제가 없다. 특히 표준 파이프라인(GATK Best Practices, DESeq2 workflow)을 사용했다면 해당 논문이나 공식 문서의 문장 구조를 가져와도 된다. 중요한 건 여러분의 파라미터와 버전 정보를 정확히 기록하는 것이다.

Methods를 쓰면서 "이 부분을 어떻게 했더라?"라는 생각이 든다면, 그건 실험 노트나 분석 로그를 다시 확인해야 한다는 신호다. 기억에 의존해서 쓰지 말고, 실제로 사용한 명령어, 파라미터, 버전을 확인하자. Methods가 탄탄하면 나머지 섹션을 쓰는 것도 훨씬 수월해진다. 여러분이 무엇을 했는지 명확히 정리되어 있으니, Results에서는 그 결과를 보고하면 되고, Discussion에서는 그 의미를 해석하면 된다. 첫 논문의 Methods를 잘 써두면, 다음 논문을 쓸 때도 그 템플릿을 활용할 수 있다. 같은 연구실에서 비슷한 분석을 하는 경우가 많으니, 한 번 제대로 만들어두면 계속 재사용할 수 있다.

자, 이제 여러분의 분석 과정을 정리해보자. 한 문장씩 차근차근 쓰다 보면 어느새 Methods 섹션이 완성되어 있을 것이다.
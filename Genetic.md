---
title: Genetic_1142

---

# Genetic
## chapter 1 and 2
### Genes, Genetics, Genomes, and Genomics
- gene = 遺傳基本單位
- genetics = 研究gene的學問
- genome = 一個生物的全部遺傳信息: 基因體
- genomic = 研究基因體的學問

#### 特點
- 基因的資訊被包含在其序列 (base sequence) 裡面 
- DNA的基因密碼: 三個bases代表一個amino acid
- 可以被複製跟傳遞 (一代傳一代)
#### codon 
- 一共有64個密碼子，其中三個維終止密碼子，其餘61個對應20種胺基酸
- 由於退化性，核甘酸的突變不一定會導致胺基酸序列改變 (silent mutation)

|特徵|解釋|
|---|---|
|degeneracy/redundancy<br>退化性|多個密碼子對應同一種胺基酸|
|unambiguous<br>不模糊性|特定一種密碼子只對應一種胺基酸|
|universal<br>廣泛性|所有生物共用同一套遺傳密碼，雖然偶有差異|

#### Codon Usage Bias
- 雖然有degeneracy，但是特定生物體中，某個codon比較被偏好
  - 不同的tRNA含量有差，使用對應的tRNA比較多的codon，轉譯比較快
  - 高表達量的基因比較偏好那些轉譯不容易錯誤的密碼子
  - 不同動物有不同的密碼子偏好
- 如果你想要大量製造某一個蛋白質，將密碼子修改成E.coli偏好的，就能夠提升表現

#### genotype and phenotype
- 基因型決定表現型
- 基因突變不容易發生，但是可以遺傳，導致基因多樣性

### properties of DNA
- 雙股螺旋，A配T，G配C，anti-parallel
- 正常的DNA (B form)，10對鹼基一圈，上一圈跟下一圈差36度
- 穩定DNA的力量有兩個，第一個是氫鍵 (AT、CG)，第二個是鹼基十個堆疊為一圈的凡德瓦力
- 分成不同種形式的DNA

|DNA型態|B-form|A-form|z-form|
|------|----|---|---|
|旋性|右手螺旋|右手螺旋|左手螺旋|
|一圈多少鹼基對|10.4 bp/turn|11 bp/turn|12 bp/turn|
|一圈有多高|3.4 nm/turn|<3.4 nm/form|4.5 nm/form|
|groove|明顯的 major and minor|有major and minor，但不明顯|只有一個groove|
|直徑|1.9 nm|2.3 nm (較寬)|1.8 nm (較扁)|
|屬於|標準型，predominant form|脫水型，鹼基相對於中心軸傾斜，結構較緊湊|形成zig-zag的型態，通常出現在GCGCGC等重複序列裡面|

- RNA聚合酶工作時，DNA往往會變得supercoil，這時DNA可能會變成Z-form
- Z-DNA常常在promoter出現，可以開啟或是關閉特定基因的轉錄活性
- Z-binding protein (ZBP)，例如ADAR1或是ZBP-1，可以專門辨識Z-form的DNA or RNA
  - 這包含一些抗病毒機制，如果ADAR1失調，可能會導致自體免疫疾病 (讓細胞誤以為病毒存在，例如Aidardi-Goutières Syndrome)
```mermaid
flowchart LR
C1{病毒入侵}
C1-->ZDNA(Z-DNA在細胞裡面成形)
ZDNA-->ZBP1(ZBP1辨識該DNA)
ZBP1-->pt[細胞焦亡:<br>一種高度發炎反應產生的<br>**溶解性細胞凋亡**]
pt-->R{病毒擴散<br>失敗}

style C1 fill: #c1ff72, stroke: #638f2c
style ZDNA fill: #eca2ff, stroke: #8e1dab
style ZBP1 fill: #ffa06a, stroke: #b14e16
style pt fill: #c4c4c4, stroke: #4f4f4f, stroke-dasharray: 3 3
style R fill: #ff5ecd, stroke: #8d0061, stroke-width: 2px
```

![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/DNA_form_0301.png)

- 共有四個Bases: **Adenine, Guanine, Thymine, Cytosine**
- 一個核甘酸包含含氮鹼基 (ATCG)，去氧核糖 (二號碳上面接的是H)，磷酸基
![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/nucleotide_structure_0301.png)

#### 遺傳物質的破壞

- **RNA對鹼性環境敏感**， $-OH$ group會攻擊ribose上的2'-OH，使其跟磷酸基產生連結，進而破壞磷酸基跟核糖之間的連接，導致RNA斷裂
![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/RNA_Hydrolysis.png)
- **DNA對酸性環境比較敏感**， $H^{+}$ 會攻擊purine的N，導致purine從DNA上面脫離，脫離後的空位在酸性環境下會促進磷酸二酯鍵的斷裂

![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/DNA_hydrolysis_0301.png)

#### 多核甘酸鏈
- polynucleotide有5'-phosphate跟3'-OH，AT之間兩個氫鍵，CG之間三個氫鍵，形成antiparallel，例如可以是如下:

$$
\begin{align}
5'-P & -TGCATG-OH-3'\\
3-'OH & -ACGTAC-P-5'
\end{align}
$$

### The central dogma
```mermaid
flowchart LR

DNA{DNA}

DNA-->Tc(transcription<br>轉錄)
Tc-->r((rRNA))
Tc-->m((mRNA))
Tc-->t((tRNA))

r-->R[交給核糖體]
m-->R
t-->R

R-->Tl(translation<br>轉錄)
Tl-->P{protein<br>合成}

 
style DNA fill: #c1ff72, stroke: #638f2c
style Tc fill: #ffa06a, stroke: #b14e16
style r fill: #57f0ff, stroke: #2c7e86, stroke-dasharray: 5 5
style m fill: #cdb2ff, stroke: #6543a6, stroke-dasharray: 5 5
style t fill: #b9c5ff, stroke: #646d96, stroke-dasharray: 5 5
style R fill: #8ef860, stroke: #378814
style Tl fill: #ff70b0, stroke: #920645
style P fill: #ff5ecd, stroke: #8d0061, stroke-width: 2px
```
- 例外包含:
  - 逆轉錄病毒 retrovorus
 
$$RNA\overset{\text{逆轉錄}}{\rightarrow}DNA\rightarrow RNA\rightarrow Protein$$

  - RNA複製病毒

$$RNA\overset{RdRp}{\rightarrow}RNA\rightarrow Protein$$

  - prion、RNA編輯等等

#### 搖擺假說
- 多數細胞並不是61種tRNA全部存在。事實上，他們大多數只有45種tRNA。一些tRNA可以辨識多個密碼子
- 實際上，mRNA的第三個鹼基通常不一定要A-U，G-C配對，而是可以跟其他的核甘酸配對，被稱為Wobble Effect
- 例如，我們以tRNA的第一個反密碼子鹼基，可以配對的mRNA的第一個密碼子鹼基來看看:

|tRNA的第一個反密碼子鹼基|配對的mRNA的第一個密碼子鹼基|
|--------------------|------------------------|
|G|C或是U|
|U|A或是G|
|I (次黃嘌呤, Inosine))|A、U 或是 C|


#### 補充: 序列介紹
- 可以分為三種: palindrome sequence、direct repeat sequence、invert repeat sequence

|序列|定義|特點|功能|
|---|---|---|---|
|Palindromic sequence<br>回文序列|在DNA或RNA中，回文序列指的是一段核苷酸序列，其正向與反向互補序列相同。如<br>5’-GAATTC-3’<br>3’-CTTAAG-5’|常見於限制酶的識別位點，如 EcoRI 就識別 GAATTC|回文結構容易形成二級結構 (如hairpin)，在基因調控與 DNA 修飾中扮演重要角色|
|Direct repeat sequence<br>直接重複序列|同一段序列在基因組中以相同方向重複出現。如<br>5’-ATCGATCG-ATCGATCG-3’|這種序列常見於轉座子、微衛星 DNA 或某些調控區域|可能影響基因表達、染色質結構，或在基因組演化中提供重組的基礎|
|Inverted repeat sequence<br>反轉重複序列|一段序列在基因組中以相反方向重複出現。如<br>5’-ATCG…CGAT-3’|容易形成二級結構，如hairpin或十字形結構|在基因調控、轉錄終止、以及某些病毒或質體的複製起點中扮演重要角色|

### 各種基因組計畫
- 長相差異非常巨大的個體，可能分子層級上基本差不多
- 各自的RNA和蛋白質合成也非常類似
#### 基本基因體組成
- Ploidy (套數): 雙套，diploid，來自父母
- Scale: 3 billion bp，兩萬個蛋白質編碼基因
- Exome: 全外顯子組，所有外顯子的組合，僅佔了genome的1.5%，佔了85%已知的致病突變

#### 人類基因組參考序列演進史

```mermaid
timeline

title Evolution of Reference Human Genome
   2001: Draft Sequences發表<br>，人類初步掌握遺傳藍圖
   2003: 人類基因組計畫，HGP，<br>提早達成
   2009: 基因組參考聯盟，GRC，<br>發布更精確的藍圖<br>GRCh37
   2009: UCSC也發布了類似<br>的藍圖，命名為hg19
   2013: GRC發布了<br>第38版藍圖 GRch38
   2013: UCSC同樣發布，版本號<br>跳過 20~37<br>，直接命名為 hg38
```
> [!Note]
> GRC命名染色體的格式為 1, 2, 3, X, Y
> UCSC命名染色體的格式為 chr1, chr2, chr3, chrX, chrY 🐱

#### T2T 聯盟計畫
- 前面幾個參考序列的定序法，往往會忽略一些重複序列區域，Sanger或是NGS都不一定能夠補全
- Telomere-to-telomere consortism 最新釋出的人類基因體序列 CHM13v1.1，彌補了GRCh38.p13所有的序列缺失，也校正了許多原本的組裝錯誤
- 完成史上第一個沒有任何gap、完整且連續的人類基因體序列
- 利用Hifi定序，有著提供長讀取數據的第三代定序優勢的同時，還兼具有比肩NGS的高精準度

#### why do we need the T2T-CHM13 Project? 
- 即使是 GRCh38，仍有約8%的區域是未知
- Sanger跟NGS屬於短序列定序，會把基因拆成小段，如果遇到高度重複的序列，就會算不出重復多少次
- 基因體裡有很多重複序列，就像那些純白色的拼圖片
  - ALU序列 (約300bp，在人類基因體裡重複了超過100萬次)
  - LINE序列 (約6000bp長) 
  - 還有微衛星DNA、端粒、著絲點
- 當你用Sanger/NGS這種短序列定序技術時：
   - 你拿到一段短序列 (比如150bp)
   - 這段序列剛好來自一個重複區域
   - 比對的時候，它會同時匹配到基因體的好幾個不同位置

> 結果就是: 
> 電腦不知道這段序列到底是從染色體1來的，還是從染色體X來的，還是從染色體7來的。🥲

- T2T-CHM13實現了 "從端粒到端粒" 的完整定序，大幅修正了過去參考基因組中的錯誤，提供了一個更連續、無斷點的模板

#### T2T的不足之處
- 來自於葡萄胎的同型合子基因組，46,XX (就是一個精子複製自己變成兩套 🙂)，而非一般正常胚胎，也無法定序Y染色體
- 研究後續轉向人類泛基因組 (pangenome)，並且嘗試補足Y染色體序列 (2013年已經完成)
- HPRC，又稱為國際人類泛基因組參考聯盟，已在2023年發表第一個草圖

> [詳細數據可以看看這裡唷 👀](https://www.blossombio.com/eNews/20210804/index.html)

#### The 1000 Genomes Project
- 千人基因組計畫著重於基因組變異的資料蒐集，包含:
  - SNPs (單核甘酸多態性)
  - Indels (小型的插入或是缺失)
  - Structural variation (大片段的消失、重復、倒位等等)
- 這些變異大多數屬於無害 (benign) 或是有益 (beneficial)，例如展現外貌變化，或是賦予抗寒的基因等等
- 有些屬於風險相關 (Risk associated) 變異，也就是讓你 "中獎機率可能比較高" 的變異 
- 有些屬於有害 (harmful) 或是致病變異 (pathogenic)，直接導致罕見遺傳疾病

### 進一步看看各個區域
#### 內含子跟非編碼區

|region|introns|non-coding regions, NCR|
|------|-------|-----------------------|
|位置|exons之間 (廢話)|位於轉錄單位兩端，或是在轉錄單位內部，或是本身也屬於轉錄單位|
|轉錄過程|被轉錄成hnRNA，然後被剪掉|可能會轉錄，也可能不會被轉錄|

- 反正就是: 
> [!Important]
> intron確實屬於NCR的一種，但NCR有一大堆，包含intron、promoter、enhancer、telomere、centromere、UTR (非轉譯區)、tRNA、rRNA、snRNA、miRNA、lncRNA等。但凡不是做蛋白質的區域，都是NCR !

- 如果外顯子組找不到突變，可以嘗試在調控區域或是intron找到答案

#### 變異類型跟規模
##### 小規模的序列變異
- 單核甘酸變異 (SNPs)，僅涉及單一鹼基替換
- 小規模插入跟缺失 (Indels)，大概50個鹼基對以下
- 小規模重復跟倒位

##### 重複序列變異
- microsatellites，也就是我們所知的STRs，一個重複單位通常2~10個鹼基對，做為親子鑑定常見
- trinucleotide repeats，三鹼基重複，會轉譯出重複的氨基酸鏈，發生過度擴張會導致神經退化性疾病，例如亨丁頓氏症的poly-Q

##### 大規模結構變異 (SV)
- 涉及長度大於50個鹼基對，或是數百萬個鹼基對的變異
- 例如複製數量變異 (SNV)，導致大片段的DNA增加或是減少，直接改變基因的數量
- 或著是重組，例如倒位、易位、插入等等

##### 染色體數異常
- 通常是非整倍體，例如唐氏症 (trisomy 21)，或著是透納症 (45, X)
- 如果是多倍體，通常會在發育時即出現問題，無法存活，例如Hydatidiform Mole (不完全的通常是三套染色體)

#### 深入介紹: SNP
- 人類基因組中大概有8470萬個SNP (根據千人基因組計畫)，例如:

$$
\begin{align}
& \text{sample A:}\\
& 5'\cdots AA\boxed{T}CGAATC\cdots 3'\\
& \text{sample B:}\\
& 5'\cdots AA\boxed{C}CGAATC\cdots 3'
\end{align}
$$

- SNP在非編碼區比較容易出現 (編碼區的SNP容易直接影響蛋白質功能，進而被淘汰)
- 門檻條件: 該變異在群體中的發生率高於1%
> [!Caution]
> - $\text{基因多型性}\ne\text{SNPs}\ne\text{基因突變}$ !!
> - 基因多型性通常是正常的遺傳多樣性，SNPs可能參與風險相關，基因突變屬於明確有害，直接導致疾病。
> - SNP不等於疾病，單一SNP可能無害，有些SNP可能跟疾病風險有相關性，但是多數只是讓你我 "與眾不同" 罷了 🙂

- SNP跟疾病的關聯性研究，很多都由GWAS (a genome-wide association study) 發現

#### Single nucleotide variations種類
- 靜默突變 (不影響轉譯):

$$GGG\rightarrow GG\boxed{T}\Rightarrow Gly$$

- 錯義突變 (導致轉譯胺基酸改變):

$$TGG\rightarrow TG\boxed{C}\Rightarrow Trp\rightarrow Cys$$

- 無義突變 (導致終止密碼子提前出現):

$$TGG\rightarrow TG\boxed{A}\Rightarrow Trp\rightarrow stop$$

- 框移突變 (插入跟缺失導致):

$$
\begin{align}
& GAGCC\boxed{T}GGTTGGAAG\cdots && \rightarrow Glu-Pro-Gly-Trp-Lys\cdots \\
\Rightarrow\quad & GAGCCGGTTGGAAG\cdots && \rightarrow Glu-Pro-Val-Gly\cdots
\end{align}
$$

- 如果是起始密碼子突變，那麼整個基因就無法轉錄跟轉譯:

$$
\begin{align}
& \boxed{T}ACAGGTGACGC\cdots \rightarrow CACAGGTGACGC\cdots\\
\Rightarrow\quad& \boxed{A}UGUCCACUGCG\cdots\rightarrow GUGUCCACUGCG\cdots\\
\Rightarrow\quad & Met-Ser-Thr-Ala\cdots\rightarrow \text{None}
\end{align}
$$

#### 舉例: 胺基酸轉換的代謝途徑
```mermaid
flowchart TB

classDef S fill: #a6a6a6, stroke: #5b5b5b, stroke_dasharray: 5 5
classDef P fill: #ffefad, stroke: #000
classDef E fill: #ffffff, stroke: #000

Phe[Phenylalanine]
Phe-->|透過|Ph(苯丙胺酸氫化酶)
Ph-->|形成|Tyr[Tyrosine]
Tyr-->|透過|Ta(酪氨酸氨基轉移酶)
Ta-->|形成|4hpa[4-hydroxyphenyl-pyruvic<br> acid]
4hpa-->|透過|4hpad(4-羥基苯基丙酮酸雙加氧酶)
4hpad-->|形成|Ha[Homogentisic acid]
Ha-->|透過|ha12d(黑尿酸1,2-雙加氧酶)
ha12d-->|形成|4m3a[4-maleyactoacetic acid]


  Ph-.->A(該酵素缺陷導致苯丙胺酸積累，造成**phenylketonuria**)
  Ta-.->B(該酵素缺陷導致酪氨酸積累，造成**type II <br>tyrosinemia**)
  4hpa-.->C(該酵素缺陷導致4-羥基苯基丙酮酸積累，造成**type III<br> tyrosinemia**)
  ha12d-.->D(該酵素缺陷導致黑尿酸積累，造成**alkaptonuria**)

class A,B,C,D S;
class Phe P
class Tyr P
class 4hpa P
class Ha P
class Ph E
class Ta E
class 4hpad E
class ha12d E
class 4m3a P

```

##### phenylketonuria, PKU
- 體染色體隱性遺傳
- PAH基因突變，Phe大量累積，對腦部跟中樞神經造成傷害 (智力發展遲緩)

##### alkaptonuria
- 體染色體隱性遺傳
- HGD基因突變，Tyr的副產物HGA累積，HGA沉積在結締組織裡面，導致褐黃症、骨關節炎

#### 深入介紹: SV跟辨認方法
- 可以從核型 (karyotype) 看出問題，使用Giemsa染劑對染色體進行染色，形成所謂的G-條帶 (AT多的地方是深色，CG多的地方是淺色)，觀察插入、重複、缺失的狀態
- 舉例，如下為一條染色體在插入、重複、缺失、倒位的情形:

$$
\begin{align}
\text{原本狀態}& \rightarrow AB-CDEF\\
\text{insersion}& \rightarrow AB-CDEFG\\
\text{duplication}& \rightarrow AB-CDDEF\\
\text{deletion}& \rightarrow AB-CEF\\
\text{inversion}& \rightarrow AB-DCEF\\
\end{align}
$$

- 最有名的就是trisomy 21 (Down syndrome)，當然還有trisomy 13、trisomy 18、47, XXY (Klinefelter syndrome)、45, X (Turner syndrome)

#### 深入介紹: 串聯重複序列 (Tandem Repeats)
- 這些重複序列直接相鄰串在一起
- 不同個體重複次數不同，又稱為VNTR
- 可以是tri-nucleotide、penta-nucleotide、hexa-nucleotide等等
- 這些重複序列在世世代代傳遞過程中，可能會重複序列增加，當增加到一定的數量時就會發病
- 通常這些併會影響到神經系統居多

##### poly-Q
- 外顯子區重複出現的CAG序列
- CAG編碼為麩醯胺酸，glutamine，也就是Q，因此又被稱為poly-Q
- 代表疾病就是Huntington's disease, HD，*HTT* 基因
- 咱們再舉幾個栗子 🌰

|類型|對應基因|通常的poly-Q數量|發病的poly-Q數量|
|----|-----|---------------|--------------|
|亨丁頓氏症 (HD)|HTT|6~35|36~120|
|脊髓延髓性肌肉萎縮症 (SBMA)，aka甘迺迪症|X染色體上的睪固酮受體|9~36|38~62|
|齒狀核紅核蒼白球路易氏體萎縮症 (DRPLA)|DRPLA或是ATN1|6~35|49~88|
|脊髓小腦萎縮症 (SCA) 家族|ATXN1、ATXN2、ATXN3、ATXN7、TBP等等|6~40個左右|50~120左右|

#### From Monogenic to Polygenic Traits
- 單基因性狀導致的疾病包含sickle cell disease (血紅蛋白基因突變)、phenyleketonuria (PAH基因突變)、HD (HTT基因突變)
- 多基因性狀導致的疾病包含一大堆複雜疾病，例如hypertension、type II diabete、cancer、dementia (晚發型)

##### 備註: Alzheimer's disease種類
- early-onset AD屬於單基因即可發病的失智症，家族遺傳傾向強烈。致病基因包含APP (類澱粉斑塊前驅物蛋白)、PSEN1、PSEN2 (presenilin，早老蛋白
- late-onset AD屬於多基因遺傳控制 (主要是風險基因影響，例如APOE基因)

##### 罕見突變的概念
- 會著重在次要等位基因頻率 (MAF)，也就是非主要等位基因的那一個，只要MAF的頻率低於1%，它就屬於罕見突變

### DNA的分離跟分析方法
#### PCR
- in vitro情況下大量擴增DNA的技術，由Kary Mullis (1983)發明，並因此獲得諾獎
- 核心步驟為: 變性 (DNA分開)、黏合 (primers結合)、延伸 (聚合酶額合成DNA)
- 試管內必須包含: 模板股、primers、*Taq* polymerase、dNTPs、buffer and ions (ex: $Mg^+$ )

```mermaid
flowchart LR

DNA(DNA)
DNA-->|denaturation|A(分離成單股)
A-->|annealing|B(primers接上)
B-->C(replication)
C-->D[形成新的DNA]
D-.->|重複循環|DNA
```
- 產生大量DNA後拿去跑凝膠電泳，可以從條帶的數量去分析，例如，如果兩個個體一個是homozygous，一個是heterozygous，前者電泳跑出一個條帶，後者出現兩個條帶

#### restriction enzyme
- 通常辨識palindromic sequences
- 命名規則是根據其分離來源的生物體命名的，例如EcoRI代表的就是:
  - **E**: genus，也就是Escherichia
  - **co**: species，也就是coli
  - **R**: strain，來自RY13菌株
  - **I**: 代表發現順序，在該菌株裡面發現的第一個限制酶
- 切割的末端可以是sticky end或是blunt end
  - sticky ends可分為5' overhangs跟 3'overhangs，容易進行配對，方便DNA重組
  - blunt ends無突出單股，連接效率較低，但不具序列專一性

|類型|定義|特徵|舉例|
|---|---|---|---|
|5′ overhang|在 DNA 的 5′ 端留下單股突出序列|突出端帶有磷酸基，容易與互補序列配對|EcoRI等限制酶切割|	
|3′ overhang|在 DNA 的 3′ 端留下單股突出序列|突出端帶有羥基 (-OH)|KpnI等限制酶切割|

##### restriction modification system, R-M system
- 細菌的先天免疫系統，區分自我跟外來DNA
- 細菌的限制酶發現外來的病毒DNA，就會把其切斷。然而，為了避免自己的基因被切掉，細菌會把自己的DNA甲基化 (methylation，利用methyltransferase)
- 有些病毒因此有些進化出了甲基化的機制，躲避限制酶攻擊

#### Electrophoresis
- DNA帶負電，我們會把DNA樣本置入瓊脂 (agarose) 板上的槽 (slot) 裡面，並且將其泡入buffer (記得slots的位置要接進負極)
- 通電後DNA就會開始往正極泳動，短鏈DNA跑得快，長鏈DNA跑得慢

#### restriction fracment length polymorphism, RFLP
- 如果你的SNPs使原本限制酶的切位點增加、消失或是位置改變，例如:

$$
5'-GAATTC-3'\quad\Rightarrow\quad 5'-GAA\boxed{C}TC-3'
$$

- 這個時候切出來的DNA長度就會有所變化，條帶分布就會有個體間的差異，因此呈現了**多態性 (polymorphism)**
- 例如sickle cell disease中，GAG變成GTG，突變剛好破壞了一個限制酶，導致原本的DNA無法被切成兩段
- 因此，如果在負極處多了一條槓，形成三條槓，那就是異型合子 ( $\beta^A/\beta^S$ )，如果只有兩條槓，就是正常同型合子 ( $\beta^A/\beta^A$ )，如果只有一條槓，那就是病理同型合子 ( $\beta^S/\beta^S$ )

![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/RFLP_SCD_0306.png)

#### nucleic acid hybridization
- DNA變性後可以再結合，因此可以利用probe和其進行互補。例子包含Southern blotting或是fluorescence in sidu hybridization (FISH)

##### Southern blotting
```mermaid
timeline
   title southern blotting workflow
   
   DNA消化: 用限制酶切割基因<br>組DNA，產生不同大小<br>的片段
   電泳分離: 將片段放入agarose<br> gel，利用電場<br>依大小分離
   變性: 將雙股DNA轉為<br>單股，以利探針結合
   轉移/Blotting: 利用毛細作用或電泳<br>，將DNA片段轉移到<br>硝酸纖維素或尼龍膜。
   固定: 通常透過烘烤或<br>紫外線交聯，使DNA<br>穩定附著在膜上。
   雜交/Hybridization: 加入帶有放射性、<br>螢光或化學標記的DNA<br>探針，與目標序列<br>互補配對。
   檢測: 透過放射自顯影或<br>螢光顯影觀察訊號，<br>顯示目標DNA的<br>位置與大小。
```
- 如果我有一個probe可以跟tandem repeat的核心序列結合，並且我用限制酶切下含有tandem repeat的片段，如果條帶位置越接進負極，重複的序列越多，越可能發病

![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/southern_blotting_tandem_repeat_0306.png)

##### FISH
- in situ (原位) = 直接在樣本上進行檢測
- 把有螢光的probe直接跟樣本的遺傳物質做鹼基配對
- 可以用來觀察細胞分裂的不同時期的細胞染色體樣態，或是用視覺化的方式確定基因在染色體的位置
- 也可以用來觀測基因組的結構變異 (缺失、重複、插入、倒位、易位等等)

> [!Note] 舉個栗子 🌰
> - 我可以把一個基因的probe放到已經複製凝聚的染色體上面。要是一對色體 發出螢光的位置不同，那就是發生了translocation
> - 要是一個染色體只出現一個螢光點 (按理來說複製了就該有兩個螢光點)，就說明發生了deletion

![image alt](https://www.genome.gov/sites/default/files/inline-images/FISH_Fact-sheet2020.jpg)

#### SNP chips and hybridization
- 假如說我有一個SNP，它有AT跟CG兩種形式，這個時候，我的SNP組合，由於染色體是雙套，就會是: $g^{AT}g^{AT}$ 、 $g^{AT}g^{CG}$ 、 $g^{CG}g^{CG}$
- 然後我針對DNA變性後的每一個單股片段都接上螢光標記
- 假如說我有不同的SNP probe，這些probe附著到beads (微珠) 上，當我的螢光DNA樣本倒入，跟這些beads上的probes雜交，我就會得到下列結果:

|基因型|對應A的探針|對應T的探針|對應C的探針|對應G的探針|
|-----|---------|---------|----------|---------|
| $g^{AT}g^{AT}$ |🟡|🟡|⚪|⚪|
| $g^{AT}g^{CG}$ |🟡|🟡|🟡|🟡|
| $g^{CG}g^{CG}$ |⚪|⚪|🟡|🟡|

#### 毛細管電泳偵測
毛細管電泳偵測
- 讓PCR產物帶有螢光標記，放進細長的毛細管中，利用電場讓DNA片段依大小移動。跟凝膠電泳一樣，小片段跑得快，大片段跑得慢
- 儀器用雷射激發螢光，偵測片段通過的時間
- 結果呈現：電腦會畫出峰圖 (electropherogram)，每個峰代表一個片段的大小。具體來說，就是一個橫軸為片段大小，縱軸為螢光強度的圖
- 假如說，某STR位點出現兩個峰，表示此人有兩個不同長度的等位基因 (heterozygous)。如果只有一個波峰，那就是 homozygous

---

## chapter 3
### classical genetics
- 古典遺傳學OG孟德爾開創
- 發明hereditary factors (遺傳因子) 這詞，就是現在知道的gene
- OG酷愛豌豆的原因:
  - 性狀明顯看得出來
  - 好栽培，三個月就收成 (我的意思是生長週期短好做實驗)
  - 自花授粉植物，品系穩定
  - 遺傳控制可以用異花人工授粉達成

##### 速帶過國中課本
- 在dominant跟recessive的同型合子 ( $WW\times ww$ ，此處代表圓形種子vs皺縮種子) 下，F1代指看出dominant表徵，F2中recessive表徵再次出現，比例大概是3:1
- 在異型合子裡面，只有dominant的遺傳因子顯現 → **顯隱律**
- test cross: 我不知道其中一個個體的基因型，所以我讓它跟另一個隱性的同型合子做雜交，如果後代沒有隱性，原個體基因型為 $WW$ ，如果顯性隱性都有，那原個體基因型為 $Ww$

> 好，進入正題，各位重新變成大學生 🙂

#### 種子到底為什麼皺縮
- 種子的形狀由SBEI (澱粉分支酶) 基因控制，該基因用來合成澱粉
- SBEI的基因突變 (轉作子插入基因導致功能下降)，導致澱粉合成異常
- 正常種子能把糖轉成澱粉，保持飽滿圓滑。突變型因為SBEI功能缺失，澱粉量減少、糖分累積，乾燥時水分流失不均，種子皺縮。

> [!Note]
> 在幫豌豆做PCR跑電泳時，可以看出 $WW$ 的基因，因為沒有insertion，形成一條跑得比較遠的條帶。 $Ww$ 形成一遠一近的條帶。 $ww$ 形成一條近的條帶

#### 單基因遺傳主要特徵
- 基因成對出現 (兩個alleles)，可以兩兩相同 (homozygous)，或是兩兩不同 (heterozygous)
- 一個配子形成時通常只攜帶一個allele，授精隨機發生，不同親代的allele重新配對
- 這叫做**the principle of segregation**

#### dihybrid expetiment
- 可以用Punnett square (棋盤法) 來判斷基因型跟預測表現型，如果是dihybrid cross (兩性狀雜交，例如 $WW\ GG\times ww\ gg$ )，表現型在F2的比例將會是 **9:3:3:1**
- 也就是說，在兩個性狀的遺傳因子下，會形成4種基因型配子 ( $WG,\ Wg,\ wG,\ wg$ )
- 一個trait不會影響到另一個trait，這叫做**the principle of independent assortment**

#### 家族譜系 
- 可以用Pedigree diagram來分析，通常圖中會用不同的符號代表不同狀況 (一次讓你終生難忘 🙂)

![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/pedigree_diagram_symbols_0307.png)

##### autosomal dominant inheritance
- 例如Huntington's disease
- 體染色體顯性基因遺傳，男性跟女性受到的影響相同，由於是顯性，受影響個體在每一代都會有出現的可能
- 受影響的個體通常有一位受影響的父母
- 在圖上面基本上不會出現半滿的圖形 (因為發病基因並非隱性)，而且每一世代基本上都會有人中標

##### autosomal recessive inheritance
- 例如albinism (白化症)
- 異型合子個體 (半滿圖形) 不會發病 (被稱為carriers)，如果有發病的個體，其父母至少兩個皆為異型合子，或是其中一個是發病者，另一個是異型合子
- 體染色體隱性基因遺傳，男性跟女性受到的影響相同
- inbreeding (近親交配) 會大幅提升遺傳的可能性

### 遺傳定律的延伸跟拓展
#### codominance
- alleles所產生的性狀會同時且獨立的表現出來，而不是一個被遮蓋或是產生中間型態
- 可以從表現型上明確分析出到底是homozygous還是heterozygous

##### 舉例
- SSRs/STRs/microsatellite的短串聯重複序列 (異型合子的基因電泳檢測結果就是兩條size的STRs條帶，來自父親跟母親)
- ABO血型系統 (A型抗原或是B型抗原)
- sickle cell disease的紅血球特徵 (異型合子可以同時產生 $Hb^A$ 跟 $Hb^S$ )
- Roan color: 紅色的毛牛跟白色的毛牛會產生花斑毛牛 (Roan)

![image alt](https://raw.githubusercontent.com/Jacklyn301/image_bank/main/SSRP_codominance_0307.png)

#### incomplete dominance
- 子代性狀表現的是中間型態，又稱為中間型遺傳，在表現型裡面，F2這一代就會形成1:2:1的比例
- 例如金魚草的顏色，紅花 ( $RR$ )跟白花 ( $Rr$ )的子代為粉紅花 ( $Rr$ )

#### multiple alleles
- 單一性狀有三個以上alleles，但是基因型只由其中兩種alleles決定
- 最熟悉的例子就是剛才共顯性提到的ABO血型系統 (基因分為 $I^A\ ,I^B\ ,i$ )
- 複習一下血型跟抗體抗原的關係

|blood types|A|B|AB|O|
|-----------|-|-|--|-|
|血漿中存在的相對應抗體|B antibody|A antibody|(none)|A and B antibodies|
|紅血球表面存在的抗原|A antigen|B antigen|A and B antigens|(none)|
|基因型|$I^A I^A$ or $I^A i$|$I^B I^B$ or $I^B i$|$I^A I^B$|$ii$|

#### epitasis 
- 有好幾個非等位基因 (loci不一樣) 同時控制一個性狀時，其中一對基因的表現會掩蓋或是改變另一對基因的表現
  - epitatic: 掩蓋別的基因的那對基因
  - hypotatic: 被掩蓋的那對基因

##### epitasis vs dominance

|特徵|dominance|epitasis|
|---|---------|--------|
|loci|發生在同一個基因座上的alleles之間，例如 $A$ 跟 $a$|發生在不同基因座上的非等位基因之間，例如 $A/a$ 跟 $B/b$|
|影響|顯性掩蓋隱性|一個基因的表現決定另一個基因是否有出場的機會|

##### 舉例
- "髮色" 的基因 (例如長金髮或是棕髮)，當遇上了 "是否禿頭" 的基因，禿頭的基因會掩蓋掉髮色的基因
- 拉不拉多有三種毛色: 黑色、棕色、黃色，是由一對控制色素產生的基因 ( $B/b$ ) ，跟一對控制色素是否沉著於毛髮的基因 ( $E/e$ ) 共同決定。如果後者的基因型為 $ee$ ，無論前者基因為何，都會呈現黃色的毛髮

|gamate|$BE$|$bE$|$Be$|$be$|
|------|----|----|----|----|
|$BE$|$BB\ EE$ ⚫|$Bb\ EE$ ⚫|$BB\ Ee$ ⚫|$Bb\ Ee$ ⚫|
|$bE$|$Bb\ EE$ ⚫|$bb\ EE$ 🟤|$Bb\ Ee$ ⚫|$bb\ Ee$ 🟤|
|$Be$|$BB\ Ee$ ⚫|$Bb\ Ee$ ⚫|$BB\ ee$ 🟡|$Bb\ ee$ 🟡|
|$be$|$Bb\ Ee$ ⚫|$bb\ Ee$ 🟤|$Bb\ ee$ 🟡|$bb\ ee$ 🟡|
### 當環境遇上基因
#### the penetrance
- 並不是說你有這個基因就一定會發病，有時你有該致病基因，不一定會表現出性狀。這個現象可以用**穿透率**來解釋
- 定義: 在攜帶特定致病基因的群體中實際表現出該疾病性狀的人數比例

$$\frac{\text{表現出性狀的人數}}{\text{攜帶致病基因的人數}}\times 100%\text{%}$$

- 如果是complete penetrance，那有突變基因就一定會發病 (存在一對一絕對關係)
- 如果是incomplete penetrance，那麼攜帶基因不一定會發病
- 例如某些遺傳性癌症 (如*BRCA1*基因突變) 雖然屬於顯性突變，但是個體可能也不會發病 
> [!Warning]
> 並不是所有的顯性疾病都能夠完全穿透 !! 

##### 影響穿透率的因素
> 為什麼有些人會生病，有些人不會?

- 環境因素: 不同的飲食或是生活習慣，或著是接觸的化學物質會影響
- epistasis: 其他基因可能掩蓋主校基因的作用
- epigenetics: DNA可能被甲基化
- age-dependency: 有些疾病需要年齡增長才會表現，又稱為延遲穿透

#### the expreesivity
- 即使發病了，每個人的表現形嚴重程度也有所不同
- 即使在同一個家族，攜帶同一個突變位點的成員之間，病情的輕重程度也有所不同。這叫做表現度的多樣性 (variable expressivity)
- 例如Marfan syndrome (chr15的 *FBN1* 基因突變)，有些人可能只是表現出瘦長的身材，有些人會有嚴重的心血管併發症或是眼部問題

|概念|penetrance|expressivity|
|---|----------|------------|
|關鍵問題|是否發病|病得多嚴重|
|本質|all-or-none (要麼發病，要麼不發病)|spectrum (嚴重程度呈現連續分布)|
|definition|攜帶者中表現出症狀的比例|患者間臨床表現的一致性|

- 如同穿透率，表現度也受到其他修飾基因、環境、表觀遺傳的影響

#### 表現型、基因型跟環境
- 就算基因型相同，不同環境條件下也可能會有不同表現型:

$$phenotype=genotype + environmental factors$$

- 例如物種*Ranunculus aquatilis*，即使是同一株植物，水面下葉片 (絲狀) 跟水面上葉片 (掌狀) 就不一樣
- 喜瑪拉雅兔在體溫低的肢端長出黑毛，在體溫高的身體核心區域長出白毛 (因為調控黑色素的酵素tyrosinase只會在低溫下正常運作)

#### phenocopy
- 表現型模擬指的是**非基因突變造成的表型**，但其外觀或症狀卻與某個遺傳性疾病非常相似
- that is，環境因素或其他非遺傳原因 "模仿" 了某個基因突變的表現，因此不會傳給下一代 (non-hereditary)
>[!Tip] 
>舉最簡單的例子: 你吃太多phenylalanine也會中毒，看起來就跟患上PKU的人一樣 🙂

#### mtDNA transmission
- 粒線體主要存在於卵子的細胞質中，即使發生了paternal leakage (精子的粒線體不小心跑進卵子)，也往往會被細胞標記 (機制通常包含ubiquitination) 跟降解
- 由於粒線體基因僅來自母親，不涉及減數分裂中的染色體分配，因此不遵守孟德爾遺傳法則
> [!Note]
> 其實粒線體也可能會移傳自父親! 一個[發表在PNAS期刊上的研究](https://www.pnas.org/doi/full/10.1073/pnas.1810946115)發現一些患有粒線體疾病的病人 (症狀包含疲勞、肌張力低下、肌肉疼痛及眼瞼下垂等等)，它們有來自雙親的粒線體 😮

#### mosaicism
- 一個個體出現多個基因型: 同一個個體中，存在兩種或兩
種以上具有不同基因型的細胞群
- 通常是因為胚胎發育過程中，單一細胞發生突變，且僅將該突變傳給自己的子細胞導致的現象
- 通常mosacism分成兩種: germline跟somatic類型

##### germline/gonadal mosaicism
- 突變只有在產生配子的細胞中出現，其他的體細胞完全沒問題。通常就是在發育的時候，生殖幹細胞的突變導致
- 父母沒事，孩子發病
- 如果一對健康的父母生下的孩子都有相同的顯性遺傳疾病，就可能是germline mosacism導致

##### somatic mosaicism
- 個體的體細胞具有超過一種基因型。通常就是胚胎發育時在有絲分裂中出現錯誤或是突變
- 不會傳給下一代，個體表現可能例如局部的皮膚顏色出現差異，或是局部神經系統異常

##### challenges
- 傳統抽血檢測 (檢驗白血球DNA) 可能測不出來
- NGS可能也測不出來 (偵測到的比例可能低於5%)

#### chimerism
- 一個單一生物體由兩個或是多個zygotes的細胞形成
- 非常非常非常罕見，遺傳表現可能包含:
  - 44, XX 加上 44, XY → 個體同時有兩套性器官
  - 組織異源性 (不同器官的DNA可能完全不一樣)
  - 當作親子鑑定發現DNA不符合時，可能孩子的父母為chimerism
- 當然，也有可能是後天性的 (acquired chimerism)，也就是透過器官移植得來的
  - 例如，做了骨髓移殖之後，受贈者的血型改變

|類型|mosacism|chimerism|
|---|--------|---------|
|來源|單一zygote|多個zygotes|
|發生時間|受精卵發育期間|受精卵早期榮的時候，或是後天移殖導致|
|example|somatic mosaicism、gonadal mosaicism|先天性 (融合胎兒) 或是後天性 (器官移植)|

![image alt](https://www.waivingentropy.com/wp-content/uploads/2013/09/Mosaicism-and-chimerism.jpg)

---

## chapter 4
### relationship between genes and chromosomes
#### 再review一次
- 成雙成對
- segragation (分離率)
- independent assortment (獨立分配率，僅限於非連鎖的基因)

#### karyotype
- 每個物種都有一整套屬於其自己的染色體 (chromosome completment)
- 用視覺化的方式讓你看出某個體的一整套染色體，被稱為karyotype
![image alt](https://as1.ftcdn.net/v2/jpg/01/09/51/64/1000_F_109516465_sa6HJgV0yfbYyW5Nu8YzwOwebAkPAxwt.jpg)

#### assignment of chromosome numbers
- 通常會根據該染色體的物理特徵，給它一個特定的數字
- 通常是根據染色體大小，從大到小分成1~22，因此，尺寸最大的染色體就是chr1

### review: the cell cycle
```mermaid
timeline
title the cell cycle
  section interphase (20 hours)
    G1 phase: cell growth & protein synthesis & pre-DNA synthesis : G1/S checkpoint
    S phase: DNA synthesis
    G2 phase : cell keep growing & post-DNA synthesis
  
  section mitotic phase or M phase (1 hours)
    prophase : chromatin condenses
    prometaphase: nuclear membrane breakdown
    metaphase: form metaphase plate
    anaphase: chromosome break at centromeres
    telophase: nuclear membrane reforms\
    
  section cytolinesis
    myosin II & actin filament ring contract: cleave cell in two

  section interphase
     the cycle restart : may enter Phase G0 : cell leaves cycle
```
- 主要分為兩期: 間期 (interphase) 跟細胞分裂期 (mitotic, or M phase)

#### interphase
- 大概佔了9成的時間，分為G1 phase、S phase、G2 phase
  - G1: 著重在細胞生長跟胞器的複製
  - S: DNA的複製，確保每個染色體都複製成兩個姊妹染色分體 (sister chromatids)
  - G2: 合成未來細胞分裂所需的蛋白質 (例如tubulin或是紡錘體)
- G0 phase: 屬於非增殖狀態，細胞分裂停止
- 這些細胞進入G0期之後，可能等待時機再次進入細胞週期
- 或是開始分化，形成有功能的細胞 (例如神經元)，不再進行分裂。這就是為何神經元或是心肌細胞受損很難再生的原因之一\

#### mitotic phase
- 分成兩個重點: 細胞核分裂 (mitosis/karyokineses) 跟細胞質分裂 (cytokinesis)

##### stages of mitosis 

|phase|description|
|-----|-----------|
|prophase 前期|染色質凝聚成染色體|
|prometaphase 前中期|核膜開始消失，紡錘絲開始連結到著絲點上面|
|metaphase 中期|姊妹染色分體被牽引，排列到赤道板 (或是被稱為metaphase plate) 上面，這個時候最好觀察karyotype|
|anaphase 後期|姊妹染色分體分開，紡錘絲縮短|
|telophase 末期|染色體到達兩極，重新變成絲狀的染色質，核膜重新生成|

##### cytokinesis
- 由myosin跟微絲形成的環組成。微絲會慢慢收縮，在原先赤道板的區域形成分裂溝，形成兩個細胞

![image alt](https://images.squarespace-cdn.com/content/v1/5c5aed8434c4e20e953d6011/f85097f5-45ef-426e-8b79-ed0993fbb3c8/Stages%2Bof%2Bmitosis.jpeg)

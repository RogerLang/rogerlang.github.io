---
layout: post
title: You're up and running!
---

# Unanticipated broad phylogeny of BEN DNA-binding domains revealed by structural homology searches  

## 前言
研究蛋白质功能的重要一步是把氨基酸序列划分在不同的domain family。传统的做法是使用多序列比对的方法进行划分。但是蛋白质的三维结构更保守（不理解）相比一级序列，具有有限序列相似的蛋白质仍然可以包含类似的功能域。
还有大量孤儿DNA模体缺少同源结合蛋白，但是识别新的DNA结合域做的人变得越来越少。之前发现的BEN结合域是一个新的序列特异性的DNA结合模块。作用于*cis*元件。这个结构域在多种果蝇和哺乳动物的发育过程中起重要作用。
>他们组和别人都发现了  
BEN domain 在多种多细胞物种和一些特定物种中都发现了。
BEN domain最初被定义为在螺旋-环边界处有4个α螺旋，以及几个保守氨基酸。但是这个结构域并不保守，不同物种之间差异很大，果蝇中有4个α螺旋，但是在哺乳动物中有6个α螺旋。
用了Alphafold的数据库，和RoseTTAFold。比较这2个AI预测的结构和实际结构的差别。最终为了说明BEN domain比之前预测分布的广泛。还说明了可以通过结构的同源性对蛋白的结构域进行分类。

## 结果
### BNE domain在多细胞物种间分布不均匀
BEN domain包含5或者6个α螺旋，以及一个13-28个氨基酸loop区。 helix-loop boundaries有脂肪性氨基酸的倾向性，在稳定蛋白结构中起重要作用。
> helix-loop boundaries指的应该是螺旋和loop的交界处？
线虫中都缺乏BEN Domian。

### 用AF系统性预测BEN domain
一级序列匹配率低，并且从36个BEN包含的蛋白中获取了36个BEN结构域。使用一级序列的方法是不可行的。
因此使用结构比较的方法。使用实验获得的BEN结构与AF2数据库中的蛋白质结构进行比较。使用的工具是DALI。

> **Proteome-wide homologous structure searching and structural analysis**
> **结构预测部分结果的方法补充**
 TheDALIserver(http://ekhidna2.biocenter.helsinki.fi/dali/)21 was used to compare the PDB experimentally solved protein structures with AlphaFold2 models. We defined the ‘‘top hits’’ as the top 10% of the hits with a Z-scoreR3. The annotated domains were retrieved from the InterPro database.
 To determine potential novel BEN domains, we manually inspected the candidate structures obtained from the DALI screening
 using PyMOL. Specifically, we checked whether each candidate structure possessed the characteristic features of a BEN domain,
 including five core a helices and a middle loop spanning at least 13 residues. 

 用结果证明使用结构比对的方法比序列比对查找同源物的方法更powerful。这部分证明了这个方法是可靠的。

### 线虫有大量未注释的BEN Domain因子
研究了那些缺乏BEN Domain，但是可能存在BEN Domain的物种。
首先在线虫中，用Insv-BEN structure（也就是Ⅰ型BEN）进行结构比较。得到161个相似的结构，评分都≥3。用的DALI算法，主要通过匹配等位残基的结构相似性进行的。这个方法不能说明找到的结构就一定有BEN Domain。只能手动确定。最后确定了13个BEN Domain蛋白。
通过3D结构的不同，这13个BEN样蛋白可以根据结构分成3类。Ⅰ类与DNA结合的结构主要是α_5螺旋和loop区，而类因为多了第6个螺旋，因此，主要是α_5和α_6与DNA发生作用。

BEN Domain折叠产生了沿着DNA螺旋沟的正电表面，是BEN-DNA相互作用的基础。并且这些BNE样模块和BEN蛋白一样，在helix-loop区有疏水残基保守序列。
> 找到新的蛋白质家族，至少应该比较一级序列，四级结构，还有静电荷。

### 线虫中新的BEN domain蛋白识别特定的DNA序列
LIN-14 and SEL-7，前者靶向miRNA *lin-4*，对线虫的发育很重要。后者是Notch信号通路的调节者。
通过CHIP-seq分析，找到31个显著的DNAmotif

### 比较果蝇和斑马鱼中的BEN Domain
在果蝇中又发现了2种新的BEN Domain蛋白。在斑马鱼中也还发现了8个人类的DEN Domian，几乎所有的这些模块都能与Insv-BEN完全重合。

### DUF4806基序包含之前没有识别的BEN domain亚型
10个预测的BEN Domain与DUF4806基序部分重叠。DUF4806基序并没有被实验验证，并且与BEN重叠的部分只到α_4。
后面关于结构描述的部分看不懂。

### 多序列比对揭示BEN域的保守性
将人，果蝇，和线虫中的BEN结构域的序列进行多序列比对，helix2-4相对其它部分是保守的。loop区有不同的长度，这个loop区的第5个氨基酸是高度保守的，并且倾向于甘氨酸。
Ⅱ型和Ⅰ型相比，除了多了第6个helix以外，helix2变长了。

### 结构比较揭示了BEN结构域及其同源域的相似性
在结构筛选的过程中，发现了HTH基序，（helix-turn-helix）。其中包括了同源结构域homeodomains：一种高度保守的DNA结合序列。BEN的2，4，5α螺旋和同源基序的α1-3是很相似的。
值得注意的是，BNE与TALE组或非TALE同源结构域是相似的。TALE是一个古老的同源结构域。BEN在早期可能起源于同源基序，因为都有着同样的DNA序列识别策略。

### 识别植物中的BEN样结构
多细胞生物中找到了BEN，可是没有在原核生物中找到。植物中却有一群BEN样蛋白。

### BEN Domain，同源基序和植物BEN样结构域的关系
想建立BEN样蛋白之间的关系。同源基序中α1和3中的保守疏水序列有助于维持疏水核心。这个特点同样存在于BEN domain和植物的BEN样区域，氨基酸替换都是具有相同的性质。
植物的BEN样区域与同源基序更相似，比如，都有3个helix，BEN domain有5或者6个helix。这意味着植物类BEN模型独立来源于当前单子叶植物和真双子叶植物祖先中的同源结构域或另一种含HTH的蛋白。（这句话没看懂，以及这一段论证起源关系的都没看懂）

### 新的含ben蛋白的上下文分析表明它们与转录/染色质调节模块共出现
之前报道了BEN domain，但是功能未知，但是有时和其它基序一起出现在基因调控中。重新评估了扩大的BEN超家族。新的BEN模块与染色质和转录调控domain，以及大量的锌指结构domain有关，与已知的BEN Domain一致。但是BEN domain在核算处理和基因转位的功能并不清楚。

### 3D比较发现新的包含DUF3504的蛋白


## 讨论
### 多细胞生物中广泛存在的包含BEN结构域的因子
对结构域的注释对理解蛋白质功能很重要。使用结构比对的方法，在多种蛋白中发现了新的BEN结构域和BEN样DNA结合结构。**在线虫中发现了以前认为不存在的大量BEN因子。发现了DUF4806是一个新的BEN domain类型。发现了包含BEN结构的因子可能是转录调控因子。**




## 生词本
Unanticipated adj.没想到的；未预料到的
phylogeny n.【生】系统发育(学)
orphan n. 孤儿；（印刷）孤行 v. 使成为孤儿 adj. 孤儿的，无双亲的
metazoan n. 后生动物；多细胞动物 adj. 后生动物的；多细胞动物的
sporadically adv. 零星地；偶发地

## 知识补充
### orphan DNA motifs
orphan DNA motifs是一种没有在其他物种或谱系中检测到同源性的DNA序列。

### Motif和domain的区别
结构域的概念由Wetlaufer于1973年首次提出，他定义结构域为**可以自动折叠的稳定的蛋白质结构单位**。过去，结构域被描述为，折叠单位，致密结构单位，功能和进化单位。每个定义都是有效的并且经常重叠。紧密结构单位结构域在很多不同的蛋白质中被发现，它在结构环境内容易独立折叠。自然界经常把几个domains结合在一起形成多结构域和多功能蛋白质。在一个多结构域蛋白质中，每一个结构域可以独立行使它自己的功能，或者和它的临近蛋白协调一致的方式行驶。Domains既可以作为模块构建大的复合体像病毒颗粒或肌纤维，也可以提供特定的催化或结合位点，这些都在酶或调节蛋白中被发现。

Motif：在生物学中是一个基于数据的数学统计模型，典型的是一段sequence也可以是一个结构，是特定的group的序列预测，例如一个DNA sequence可以定义为转录因子结合位点，也就是序列倾向于被这种factor结合。对蛋白质来说，sequence motifs可以被定义为蛋白质（蛋白质序列）属于一个给定的蛋白质家族。一个简单的motif可以是，例如，一个模式pattern，而这个模式被这个group中的所有成员共享。例如WTRXEKXXY（这里，X代表任何氨基酸）。当然也有更复杂的motif模型。Motif有时和特定的功能联系一起。



### 染色质/转录调控模块














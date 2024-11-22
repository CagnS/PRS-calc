# PRS-calc

Final project for bme 160 class

Calculating Polygenic Risk Scores for Insulin Sensitivity
Polygenic risk scores (PRS) are increasingly utilized in genetic research and clinical practice to
predict the likelihood of individuals developing complex diseases based on their genetic
makeup. The increasing prevalence of insulin resistance and its associated complications
means it is important for people to know their own risk level. We present a python program that
calculates a PRS for modified Stumvoll insulin sensitivity. Our program takes two inputs: an
individual’s genotype data in Reference SNP (rs) format and genome-wide association study
(GWAS) datasets. The GWAS data is obtained from the GWAS catalog online
(https://www.ebi.ac.uk/gwas/) and provides associations between specific SNPs and modified
Stumvoll insulin sensitivity. Our program takes both the individual’s genotype data and the
GWAS dataset and combines data from both to find the effect of each SNP on an individual's
risk score. It then aggregates the effects of these genetic variants across the genome since
each contributes a small effect to the overall risk of disease, and the result is a PRS score which
is outputted and printed. While this program is designed for assessing the risk of insulin
sensitivity (as this is the GWAS data pre-loaded in), one could in theory use it for any disease as
long as there is available data on the GWAS catalog.
Introduction of The Problem
An individual’s knowledge of their risk level for conditions such as insulin resistance is incredibly
important. With knowledge of one’s risk level, an individual is empowered with knowledge that
could affect their decision making at every level. These individuals could prevent a life-altering
diagnosis and in some cases even save or extend their own lives. Our tool allows an individual
to calculate one’s PRS score based on GWAS data they choose.
Description of the Solution
Our program first loads in the data inputs.Then, to actually calculate the PRS our program uses
a for loop to cycle through each SNP in the genotype data. Each SNP count in the genotype
data is multiplied by the effect size from the GWAS dataset, and the products are all summed to
produce the final PRS.
Discussion/Evaluation
We had some difficulties finding solid, usable data. The GWAS data was not hard to find but
there were issues loading it. We eventually figured it out, and calculating the PRS score was a
matter of following the equation in a way that ran through each row of the data.
Besides offering individuals a free and easy way to assess their risk for a disease, our
program’s significance is also in the fact that it allows users to input both their own genotype
data and their GWAS data of choice. This means that if an individual wants to use data collected
from a population of their own ethnicity for increased accuracy, they can do so.
Conclusion
In conclusion, our Python-based PRS calculation tool is a valuable resource for those who
desire personalized risk assessment for a given disease/condition. This tool allows an individual
to assess their risk for insulin sensitivity and other conditions if they desire. It also allows an
individual to get a more accurate score by using data more accurate to them.(like that collected
from a population of their own ethnicity). Future improvements to this program could be an input
field where you directly input the GWAS link and your genotype data.
References
1. https://www.illumina.com/areas-of-interest/complex-disease-genomics/polygenic-risk-sco
res.html#:~:text=Polygenic%20risk%20scores%20(also%20known,of%20developing%20
a%20particular%20disease.
2. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8894758/#:~:text=The%20basic%20equa
tion%20for%20the,Term
3. https://www.ebi.ac.uk/gwas/

Join $\bowtie$
Join: a binary operator.
* A : $(X_1,\cdots,X_m, Y_1,\cdots,Y_n)$
* B : $(Y_1,\cdots,Y_n, Z_1,\cdots,Z_p)$
語法： $A \bowtie_{<合併條件>} B$
目的：兩關聯表格各取一條件欄位，以此特定條件欄位之運算合併兩關聯表格
* A JOIN B (or A B): **common attributes appear only once**. e.g. CITY
* $(X_1,\cdots,X_m, Y_1,\cdots,Y_n, Z_1,\cdots,Z_n)$
結合律 Association:
$$(A\bowtie B )\bowtie C = A\bowtie ( B\bowtie C )$$
交換律 Commutative:
$$A\bowtie B = B\bowtie A$$
* if A and B have ==no attribute in common==, then
$$A\bowtie B = A \times B$$


非基本運算子
$$R1 \bowtie_{<合併條件>} R2 ＝ σ_{<合併條件>} （R1 \times R2）$$
![[Pasted image 20230321042017.png]]
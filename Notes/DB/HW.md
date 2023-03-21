1.      (15%) 有一個與租船有關的資料庫：三個資料表Sailors, Boat, Reserves
![[Pasted image 20230321062347.png]]
寫出其**關聯代數運算式**與**表格答案**。
  1. 查詢”Wawrinka”所租過船的船名、顏色
  $$\Pi_\text{color, bname}
  \left(\sigma_{sname = 'Wawrinka'}((\text{Sailors $\bowtie_{sid}$ Reserves})\bowtie_{bid}Boats) 
  \right) $$
![[Pasted image 20230321113320.png]]

  2. 查詢rating大於或等於9的船員人數
  $$\Pi\text{Count}(*)(\sigma_{rating\geq 9}(Sailors)) $$
   6
   ![[Pasted image 20230321113335.png]]
  1. 查詢曾經租過編號為103船的船員名字、年齡與姓名
  $$\Pi_{sname,age}(\sigma_{bid='103'}(Sailors\bowtie_{sid}Reserves))$$
![[Pasted image 20230321113314.png]]
  1. 查詢租過船名為”Blast”船的船員姓名與租用日期
  $$\Pi_{sname,day}(\sigma_{bname='blast'}((Boats\bowtie_{bid}Reserves)\bowtie_{sid}Sailors))$$
![[Pasted image 20230321113308.png]]
  1. 查詢從6/1/2015~6/5/2015被借出的船隻名、船隻顏色、船員姓名與其年齡
$$\Pi_{bname,color,sname,age}(\sigma_{day\geq2015-06-01\bigcap day\leq2015-06-05}(Sailors\bowtie_{sid}Reserves)\bowtie_{bid}Boats) $$
![[Pasted image 20230321113300.png]]

2.  參考第2題的資料表，繪製表格回答以下關聯式代數(Relational Algebra) 之計算結果


   1. $\Pi_{sid,sname,rating,age,day}(Sailors\bowtie_{sid}Reserves)$
  
| sid | sname     | rating | age | day        |
|-----|-----------|--------|-----|------------|
| 22  | Wawrinka  | 10     | 30  | 6/7/2015   |
| 22  | Wawrinka  | 10     | 30  | 6/5/2015   |
| 22  | Wawrinka  | 10     | 30  | 6/3/2015   |
| 22  | Wawrinka  | 10     | 30  | 6/1/2015   |
| 32  | Lu        | 9      | 32  | 5/28/2015  |
| 32  | Lu        | 9      | 32  | 6/1/2015   |
| 64  | Nishikori | 10     | 26  | 6/3/2015   |
| 85  | Nadal     | 10     | 29  | 5/30/2015  |
| 85  | Nadal     | 10     | 29  | 6/3/2015   |
| 85  | Nadal     | 10     | 29  | 6/3/2015   |
  2. $\Pi_{Boats.bid,bname,color,sid}(\sigma_{color='green'}(Boats\times Reserves))$
  
| bid | bname  | color | sid  |
|-----|--------|-------|------|
| 103 | Marine | green | 22   |
| 103 | Marine | green | 22   |
| 103 | Marine | green | 22   |
| 103 | Marine | green | 22   |
| 103 | Marine | green | 32   |
| 103 | Marine | green | 32   |
| 103 | Marine | green | 64   |
| 103 | Marine | green | 85   |
| 103 | Marine | green | 85   |
| 103 | Marine | green | 85   |
  3. $\Pi_{sname,age,bname,color,day}((Sailors\bowtie_{sid}Reserves)\bowtie_{bid}Boats)$
  
  | sname     | age | bname    | color | Day        |
|-----------|-----|----------|-------|------------|
| Wawrinka  | 30  | Intelake | blue  | 6/7/2015   |
| Nadal     | 29  | Intelake | blue  | 5/30/2015  |
| Wawrinka  | 30  | Clipper  | red   | 6/5/2015   |
| Lu        | 32  | Clipper  | red   | 5/28/2015  |
| Nadal     | 29  | Clipper  | red   | 6/3/2015   |
| Wawrinka  | 30  | Marine   | green | 6/3/2015   |
| Lu        | 32  | Marine   | green | 6/1/2015   |
| Nadal     | 29  | Marine   | green | 6/3/2015   |
| Wawrinka  | 30  | Blast    | red   | 6/1/2015   |
| Nishikori | 26  | Blast    | red   | 6/3/2015   |
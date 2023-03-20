# Types
Traditional Set Operations 基本運算子
* [[Union]] (聯集) $\bigcup$
* [[Difference]] (差集) $-$
* [[Cartesian Product]]/Times (卡氏積) $\times$
* [[Select]]/Restrict (選擇(限制)) $\sigma$
* [[Projection]] (投影) $\Pi$
Special Relational Operations 非基本運算子(可由基本組合而成)
* [[Intersection]] (交集) $\bigcap$
* Join/[[Natural Join]] (合併) $\bowtie$
* [[Divide]] (合併) $\div$ 
# Constriants
### Union Compatibility
two relations are union compatible iff they have identical headings
* they have same set of **attribute name**.
* corresponding attributes are defined on the **same domain**.
Union ($\bigcup$), Intersection ($\bigcap$) and Difference ($-$) require Union Compatibility, while Cartesian Product ($\times$) don't
* Still need Integrity Rule: Duplicate PK $\rightarrow$ 拒絕或留一

## SQL vs Relational Operators
A SQL `SELECT` contains several relational operators.
SQL: 
```SQL
SELECT S#, SNAME
FROM S, SP
	WHERE S.S# = SP.S#
	AND CITY = 'London'
	AND QTY > 200
```
1. Join : $S\bowtie_{S\#} SP$
2. Select : $\sigma_{CITY ='London', QTY>200}$
3. Project :  $\Pi_{S\#,SNAME}$
BNF:
$$ \Pi_{S\#,SNAME}(\sigma_{CITY ='London', QTY>200}(S\bowtie_{S\#} SP)) $$
除法 $\div$
A, B: two relations.
* A : $(X_1,\cdots,X_m,Y_1,\cdots,Y_n)$
* B : $(Y_1,\cdots,Y_n)$
語法： $A\div B$
目的：第一個關聯表格當做是被除表，第二個關聯表格當做是除表。此運算是在關聯表格A中找出包含關聯表格B中屬性值的值組
* Heading: $(X_1,\cdots,X_m)$
* Body: all $(X:x)$ satistify $(X:x,Y:y)$ in A for all $(Y:y)$ in B
非基本運算子
$$A\div B = \Pi_x(A) - \Pi_x(\Pi_x(A) \times B-A) $$
![[Pasted image 20230321043511.png]]


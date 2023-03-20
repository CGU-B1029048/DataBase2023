卡氏積 times ×
語法 $A \times B$
* A, B: two relations.
  * A : (X<sub>1</sub>,...,X<sub>m</sub>)), A = { a | a = (a<sub>1</sub>,...,a<sub>m</sub>)}
  * B : (Y<sub>1</sub>,...,Y<sub>n</sub>), B = { b | b = (b<sub>1</sub>,...,b<sub>n</sub>)}
目的：
* 合併時無條件限制，以所有可能的配對方式，將R1與R2兩個關聯間的所有值組加以合併
* 若R1有m筆記錄，R2有n筆記錄，卡式積之後則有$m\times n$筆記錄的關聯表格
* 若R1有a個屬性（欄位），R2有b個屬性(欄位)，卡式積之後則有$a+b$個屬性的關聯表格
結果: 
* Heading: (X<sub>1</sub>,...,X<sub>n</sub>,Y<sub>1</sub>,...,Y<sub>n</sub>)
* Body: { c | c = (a<sub>1</sub>,...,a<sub>m</sub>,b<sub>1</sub>,...,b<sub>n</sub>)}
Association:
$$(A \times B) \times C = A \times (B \times C)$$
● Commutative:
$$A \times B = B \times A$$
![[Pasted image 20230321034358.png]]
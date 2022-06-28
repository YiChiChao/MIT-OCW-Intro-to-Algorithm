# MIT Intro of Algorithm

## Intro
To solve computation problems and communicate with others that your solutions are **correct** and **efficient**.
### 定義
* Problem：
    * 給定一群input，要去找到對應的正確output
    * 正確的output條件一般不會是對一個一個input去給，而是正確output要滿足一些驗證條件
    * 一般而言，input會是隨機的巨大數據
* Algorithm：
    * $f: I \rightarrow O$
    * 一個訂定的流程讓所有input最終都能產生正確的output
* Correctness：
    * 透過數學歸納法來證明演算法的正確性
        * Hypothesis
        * Base Case
        * Induction
* Efficiency
    * 為了不被電腦影響測試結果，efficiency是去計算某個演算法需要花多少固定時間的operation數目。
    * 對於這堂課而言，polynomial time($O(n^{c})$)就可以視為efficient
### 舉例
* Problem：Given any set of n students, is there a pair of students with same birthday?(Assume resolution of possible birthdays exceeds n (include year, time, etc.) )
* Algorithm：
    * 建立一個表去記錄所有人的生日和時間
    * 開始問所有在教室當中的同學，
        * 如果問的對象的生日已經存在於表中，return 有解
        * 否則將其名字和生日紀錄在表中並繼續
    * 當問完所有人後就return無解 
* Correctness：證明上述演算法的正確性
    * **Hypothesis**：如果前k個人中有至少兩個人生日相同，則演算法會在訪問第k+1個人前回傳正解
    * **Base Case**：k = 0, 前k個人沒有解
    * 假設$k = k \prime$
        * 如果前k個人中有至少兩個人生日相同，則會回傳
        * 如果前k個人中沒有人生日重複，透過其演算法，會去檢驗第k+1個人的生日是否和前k個人相同，如果有，則會回傳。
### Model of Computation
![](https://i.imgur.com/6iaQ0yp.png)


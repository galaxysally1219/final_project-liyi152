# final_project-liyi152
final_project-liyi152 created by GitHub Classroom
project:任意給定平面上三點, 判斷原點是否在這三點所圍成的三角形內.

作法:
input: X(輸入的三點所呈矩陣)
output: 原點的位置

計算面積的方法:
step 1: 計算三角形ABC(A,B,C為輸入的三點)面積
step 2: 計算三角形ABO,ACO,BCO(O為原點)面積
step 3: 判斷三點是否可呈三角形
平面上三點的關係:
1.共點
2.共線
3.呈三角形
step 4: 利用面積關係求出原點位置
面積關係的情況:
1.原點在內部: abo+aco+bco=abc
2.原點在外部: ab0+aco+bco>abc
3.原點在邊界上: abo,aco, or bco 其中一個面積為0

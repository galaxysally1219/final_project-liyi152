# final_project-liyi152
final_project-liyi152 created by GitHub Classroom
Project 5: 任意給定平面上三點, 判斷原點是否在這三點所圍成的三角形內.
作法:
input: X(輸入的三點所呈矩陣)
output: 原點的位置
step 1: 計算三角形ABC(A,B,C為輸入的三點)面積
step 2: 計算三角形ABO,ACO,BCO(O為原點)面積
step 3: 判斷三點是否可呈三角形
step 4: 利用面積關係求出原點位置
面積關係的情況有三種:
原點在內部: abo+aco+bco=abc
原點在外部: ab0+aco+bco>abc
原點在邊界上: abo,aco, or bco 其中一個面積為0

pseudo code:
ab=B-A;
ac=C-A;

abc=1/2*abs(ab(1)*ac(2)-ab(2)*ac(1)); 
abo=1/2*abs(A(1)*B(2)-A(2)*B(1)); 
aco=1/2*abs(A(1)*C(2)-A(2)*C(1)); 
bco=1/2*abs(B(1)*C(2)-B(2)*C(1)); 

check=0; 
if(A==B|A==C|B==C)
    disp('共點');
    check=1;
end
if(abs(ab/norm(ab))==abs(ac/norm(ac)))
    disp('共線');
    check=1;
end
if(check==0)
    if(abo+aco+bco>abc)
        disp('在外部');
    else
        if(abo>0&&aco>0&&bco>0)
            disp('在內部');
        else
            disp('在邊界上');
        end
    end
end
end

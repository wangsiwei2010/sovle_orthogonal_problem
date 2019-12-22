# sovle_orthogonal_problem
wen2013 feasible method for optimization with orthogonality constraints. 

需自己定义优化函数
例如：

function [F,G]=fun1(P,alpha,Y,Q,L)
    G=2*L*P-2*alpha*Y*Q';
    F=trace(P'*L*P)+alpha*(norm(Y-P*Q,'fro'))^2;
end

其中G为F关于待优化变量的导数
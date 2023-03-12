# Data-sturcture.-nth-Ugly-No-More-efficient-code-



def n_th_ugly(n):
    dpugly = [0] * n 
    dpugly[0] = 1 
    u2 = u3 = u5 = 0 
    multip_2 = 2
    multip_3 = 3 
    multip_5 = 5 
    for i in range(1,n):
        dpugly[i] = min(multip_2, multip_3, multip_5)
        if dpugly[i] == multip_2:
            u2 += 1 
            multip_2 = dpugly[u2] * 2 
        if dpugly[i] == multip_3:
            u3 +=  1 
            multip_3 = dpugly[u3] * 3 
        if dpugly[i] == multip_5:
            u5 += 1 
            multip_5 = dpugly[u5] * 5
            
    return dpugly[n - 1]
    

n= 15        
print(n_th_ugly(n))
    

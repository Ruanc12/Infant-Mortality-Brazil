#### Os Municípios serão filtrados de acordo com o Coeficiente Geral de Mortalidade Padronizado por Idade (CGMP) por mil habitantes, no qual é calculado segundo a seguinte relação: 

$$
CGMP = \frac{\sum_i \left(\frac{O_i}{N_i}\times P_i\right)}{\sum_i P_i} \times 1000
$$

##### Onde:  
- $O_i$: número de óbitos no grupo etário $i$  
- $N_i$: população do grupo etário $i$  
- $P_i$: população padrão do grupo etário $i$  

#### O filtro utilizado será CGMP > 5 no primeiro triênio.

#### O Municípios também serão filtrados de acordo com o Desvio Médio Relativo do Número de Óbitos (DMRO), no qual é calculado segundo a seguinte relação: 

O **Desvio da Média de Óbitos (DMRO)** é definido como:  

$$
DMRO = \frac{DMO}{M} \times 100\%
$$  

onde:  

$$
DMO = \frac{|O_{t-1} - M| + |O_{t} - M| + |O_{t+1} - M|}{3}
$$  

$$
M = \frac{O_{t-1} + O_{t} + O_{t+1}}{3}
$$  

- $O_t$: número de óbitos no ano $t$.
- $M$: média do número de óbitos do triênio.

#### O filtro utilizado será DMRO < 20% e percentual de óbitos no primeiro triênio.

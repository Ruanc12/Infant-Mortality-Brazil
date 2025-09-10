#### Esse projeto tem como objetivo aplicar diferentes metodologias de modelagem para dados longituinais. Tradicionalmente, as análises com esses tipos de dados são realizadas utilizando Modelos de Efeitos Mistos, no entanto, essa abordagem pressupõe que os dados são provenientes de uma população homogênea, pois o modelo ajusta uma trajetória única para todos os indivíduos. Levando isso em conta, a modelagem de trajetórias por grupos latentes torna-se uma ferramente útil, pois torna possível a modelagem de padrões de trajetórias em populações heterogêneas. As principais abordagens utilizadas são os Modelos de Mistura de Crescimento (GMM=Growth Mixture Models) e Análise de Crescimento com Classes Latentes (LCGA=Latent Class Growth Analysis), que podem ser utilizadas em desfechos contínuos ou discretos. A principal diferença entre as metodologias é a ausência de efeitos aleatórios no LCGA. Para aplicação desses métodos, são considerados dados de mortalidade infantil de cidades brasileiras entre os anos de 2005 e 2012 disponibilizados por Russo (2019). Disponível em: [openICPSR](https://www.openicpsr.org/openicpsr/project/108527/version/V1/view;jsessionid=81B73ADAB523CB4E00C486CA530208E6?path=/openicpsr/108527/fcr:versions/V1/Data_Final.dta&type=file).




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

#### O filtro utilizado será DMRO < 20% no primeiro triênio.
### Referências
Russo, Letícia Xander. Data_IM_Brazil_Final: Data_Final.dta. Ann Arbor, MI: Inter-university Consortium for Political and Social Research [distributor], 2019-02-18. https://doi.org/10.3886/E108527V1-11941

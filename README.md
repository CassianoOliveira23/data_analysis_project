<h1 align="center">Análise de Dados</h1>

![analiseimagem](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/9b0fc301-509f-4766-8617-003f05568385)

<h3>Case: Cancelamento de Clientes</h3>

<p>Uma empresa de grande porte recentemente percebeu que da sua base total de clientes, a maioria são clientes inativos, ou seja, que já cancelaram o serviço.</p>
<p>Precisando melhorar seus resultados a empresa quer compreender os motivos que levaram ao cancelamento, e quais as ações mais eficientes para reduzir este número</p>

---

Ferramentas Utilizadas:
- Python <img align="center" height="20" width="30" alt="js-icon"  src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
- Biblioteca Pandas
- Jupyter Anaconda

---

<h1>Importando a Base de Dados</h1>

<p>Importei a biblioteca
pandas, após importar a biblioteca nós vamos
utilizar o pd.read_csv para ler o nosso arquivo
que está no formato csv. E atribundo a tabela a uma variável</p>

![1](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/a8c2c763-72ad-43ed-ba20-dd5f46944a80)

<h3>Utilizei o comando display para visualizar a nossa base de dados.</h3>

![2](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/279c513a-e4a4-4139-a249-edf006794e53)


---


<h1>Removendo Informações Vazias</h1>

<p>Antes de começar com as análise é essencial
fazer o tratamento de dados, assim
evita trazer erro por conta de dados
desnecessários ou até inexistentes.</p>
<p> Utilizei o comando
tabela.dropna para remover as informações
vazias da nossa tabela.</p>

![3](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/037ec4b6-409c-4382-b3fe-2e8817fd2eb9)


---


<h1>Análise de Dados</h1>

<h3>Verificando a Taxa de Cancelamento</h3>

<p>Vamos começar analisando a taxa de cancelamento da empresa,
pois o objetivo é diminuí-la. Então vamos ter que verificar
qual é essa taxa e descobrir de onde ela vem.</p>

<p> Utilizei o tabela[“cancelou”].value_counts
para verificar a quantidade de informações que temos
na coluna “cancelou” da tabela.
</p>

<p>Dessa forma vamos poder visualizar com o display qual
é a proporção de clientes que cancelaram e que
continuam com a assinatura.</p>

![5](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/32c4ac22-efa8-4a9c-8a8e-6f4701ca625f)

<p>A primeira visualização vai mostrar a contagem dos dados, quem
cancelou (1) e quem não cancelou (0). Já a segunda visualização vamos normalizar e formatar
em percentual, assim fica mais fácil para analisar qual a
proporção de clientes que estão cancelando o serviço.
</p>

<p>Perceba que temos um total de 56,7% de cancelamento das
assinaturas, então mais da metade dos clientes estão
cancelando o serviço.</p>

<p>Então vamos descobrir de onde vem esse
número.
</p>


---


<h1>Verificando o Cancelamento por Contrato</h1>

<p>Já vimos como está a relação do cancelamento dos clientes, agora
podemos dar uma olhada como está a duração do contrato desses
clientes.
</p>
<p>Lembrando que temos 3 tipos de contrato: mensal, trimestral e
anual. Então é interessante ver como está essa proporção para
verificar se isso pode ser um fator que afeta diretamente o
cancelamento do serviço</p>

![6](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/f62a3cca-01ce-4a35-a429-f2c148ddd9f2)

Com essa simples análise você já nota que temos a seguinte
proporção na duração dos contratos:
- Anual 40,19%
- Trimestral 40,00%
-  Mensal 19,75%

<p>Veja que temos uma divisão quase igual entre os planos anual e
trimestral, mas o plano mensal já fica atrás com quase 20%.</p>

<p>O que podemos fazer é analisar as informações dos contratos para
verificar como estão distribuídas e verificar se algum deles tem um
percentual maior de cancelamento.</p>


---

<h1>Analisando as Informações dos Contratos</h1>

<p>Utilizei o groupby para agrupar as
informações da coluna duração_contrato e depois
fazer a média das informações que temos na tabela.</p>

<p>Isso vai nos dar uma informação mais geral de cada
um desses planos, e podemos verificar se tem alguma
informação importante.</p>

![7](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/4fd859c8-9322-4dab-8f4d-00da39b20b13)

<p>Com as informações agrupadas, é possível notar que os clientes do
plano Mensal, possuem uma média de cancelamento igual a 1,
ou seja, praticamente todos os clientes que utilizam esse plano
fizeram o cancelamento do serviço.</p>

<p>Esse já é um ponto importante dentro da nossa análise, pois existe
um plano dessa empresa, onde praticamente todos os clientes
fazem o cancelamento do serviço.</p>


---

<h1>Removendo o Contrato Mensal</h1>

<p>Sabendo que o contrato mensal não é uma boa opção para a empresa, nós podemos remover as
informações desse contrato específico e continuar analisando.</p>

![8](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/465918a7-d2dd-47c8-a0f2-34abe87b8bba)

<p>Veja que a proporção de
cancelamentos já caiu para 46,1%
nessa análise, mas esse número
ainda é muito alto.</p>

<p>Então vamos continuar analisando
para chegar em um valor aceitável
de cancelamentos que não esteja
perto dos 50%.</p>


---

<h1>Análise de Assinaturas</h1>

<p>Como ainda temos um número bem alto de cancelamentos vamos agora fazer uma
análise nas assinaturas para verificar se podemos tirar alguma conclusão para melhorar
esse índice de cancelamentos.</p>

<p>Primeiro vamos fazer a contagem dos valores na coluna de assinaturas para saber
quantas assinaturas temos em cada um dos planos.</p>

<p>Em seguida vamos agrupar as informações por assinatura e obter a média das linhas
para cada uma das colunas.</p>

![9](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/73493d6e-d2ce-4018-b408-d0107d99d993)

<p>Na primeira análise podemos
verificar que temos praticamente
a mesma quantidade em cada
uma das assinaturas, ou seja,
temos praticamente 1/3 em cada
assinatura.</p>

<p>E na segunda análise temos que
os valores de cancelamento
também são muito parecidos.</p>

<p>Não podemos excluir nenhuma
informação, pois os dados são
praticamente iguais. Isso quer
dizer que vamos ter que ir mais
fundo na nossa análise de dados.</p>

---

<h1>Análises Gráficas</h1>

<p>Para criação dos gráficos nós vamos utilizar a biblioteca plotly.express</p>

![10 - criango graficos](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/1e373590-e48b-4e27-9d24-3ade114ac634)

<p>Agora utilizei a estrutura de repetição For para percorrer cada uma das colunas da nossa tabela. Com isso vamos
criar um gráfico de Histograma com cada uma das colunas, assim podemos analisar cada uma das informações e verificar como
elas se comportam em relação aos cancelamentos da empresa</p>


<p>Nesse gráfico é possível notar que
clientes com mais de 20 dias de atraso
cancelam suas assinaturas.</p>

![dias_atraso](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/c448c461-48c1-4ae0-874a-5d17c900a8f6)
#

<p>Já nesse outro gráfico é possível notar
que clientes com mais de 5 ligações ao
call center cancelam suas assinaturas.</p>

![call_center](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/c1c97f02-3874-4e75-8e16-3f2762f42dd9)
#

<p>Analisando apenas os dois gráficos
indicados, nós podemos manter na tabela
as ligações ao call center que são menores
do que 5.</p>

<p>E podemos manter também as
informações onde os dias de atraso são
menores do que 0.</p>

<p>Com isso podemos visualizar a base de
dados e fazer o cálculo novamente para
verificar o percentual de cancelamento.
Veja que só removendo as informações
dessas duas colunas passamos de um
percentual de quase 50% de cancelamento
para 18,4%. Tivemos que fazer
várias etapas até chegar em um valor
“aceitável”</p>

![11](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/e4be7695-f419-4522-b70b-bffef907ed59)


![12](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/5eb87bad-2029-454b-8fbe-62a5a53ff528)

---

<h1>Conclusão</h1>

<p>Nós começamos a análise com um taxa de
cancelamento de 56,7%. Após o primeiro tratamento
conseguimos diminuir um pouco e atingimos 46,1%.</p>

<p>No final com ajuda dos gráficos conseguimos ajustar
nossa base de dados e chegamos ao percentual de
18,4% em cancelamentos.<p>

<p>E fazendo todas essas análises e tratamentos nós
temos como mostrar para empresa onde estão os
problemas e o que pode ser feito para minimizar os
cancelamentos</p>

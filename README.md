<h1 align="center">Projeto de Análise de Dados</h1>

![analiseimagem](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/9b0fc301-509f-4766-8617-003f05568385)

<h3>Case: Cancelamento de Clientes</h3>

<p>Uma empresa de grande porte recentemente percebeu que da sua base total de clientes, a maioria são clientes inativos, ou seja, que ja cancelaram o serviço.</p>
<p>Precisando melhorar seus resultados a empresa quer compreender os motivos que levaram ao cancelamento, e quais as ações mais eficientes para reduzir este número</p>

---

Ferramentas Utilizadas:
- Python <img align="center" height="20" width="30" alt="js-icon"  src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
- Biblioteca Pandas
- Jupyter Anaconda

---

<h1>Importando a Base de Dados</h1>

<p>Vamos importar da biblioteca
pandas, muito utilizada para análise de dados.
Após importar a biblioteca pandas nós vamos
utilizar o pd.read_csv para ler o nosso arquivo
que está no formato csv. E atribundo a tabela a uma variável</p>

![1](https://github.com/CassianoOliveira23/data_analysis_project/assets/130614345/a8c2c763-72ad-43ed-ba20-dd5f46944a80)

<h3>vamos utilizar o comando display para visualizar a nossa base de dados.</h3>

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
número tão alto!
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

Veja que a temos uma divisão quase igual entre os planos anual e
trimestral, mas o plano mensal já fica atrás com quase 20%.

O que podemos fazer é analisar as informações dos contratos para
verificar como estão distribuídas e verificar se algum deles tem um
percentual maior de cancelamento.


---

<h1>Analisando as Informações dos Conratos</h1>


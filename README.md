<h1>Análise de dados com Python usando a ferramenta Anaconda Jupyter</h1>
  <h3>script desenvolvido durante evento Intensivão Python ministrado pela Hashtag Programação</h3>
  <br /> <br />
  
  ```python
#Passo 1: importar a base de dados
import pandas as pd

tabela = pd.read_csv("telecom_users.csv")

#Passo 2: visualizar a base de dados
tabela = tabela.drop("Unnamed: 0", axis=1)
display(tabela)

# - entender quais informações estão disponíveis
# - descobrir os erros da base de dados
```


<div>
<style>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>IDCliente</th>
      <th>Genero</th>
      <th>Aposentado</th>
      <th>Casado</th>
      <th>Dependentes</th>
      <th>MesesComoCliente</th>
      <th>ServicoTelefone</th>
      <th>MultiplasLinhas</th>
      <th>ServicoInternet</th>
      <th>ServicoSegurancaOnline</th>
      <th>...</th>
      <th>ServicoSuporteTecnico</th>
      <th>ServicoStreamingTV</th>
      <th>ServicoFilmes</th>
      <th>TipoContrato</th>
      <th>FaturaDigital</th>
      <th>FormaPagamento</th>
      <th>ValorMensal</th>
      <th>TotalGasto</th>
      <th>Churn</th>
      <th>Codigo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7010-BRBUU</td>
      <td>Masculino</td>
      <td>0</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>72</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>SemInternet</td>
      <td>...</td>
      <td>SemInternet</td>
      <td>SemInternet</td>
      <td>SemInternet</td>
      <td>2 anos</td>
      <td>Nao</td>
      <td>CartaoCredito</td>
      <td>24.10</td>
      <td>1734.65</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>9688-YGXVR</td>
      <td>Feminino</td>
      <td>0</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>44</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>Fibra</td>
      <td>Nao</td>
      <td>...</td>
      <td>Nao</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>Mensal</td>
      <td>Sim</td>
      <td>CartaoCredito</td>
      <td>88.15</td>
      <td>3973.2</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>9286-DOJGF</td>
      <td>Feminino</td>
      <td>1</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>38</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>Fibra</td>
      <td>Nao</td>
      <td>...</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>Mensal</td>
      <td>Sim</td>
      <td>DebitoAutomatico</td>
      <td>74.95</td>
      <td>2869.85</td>
      <td>Sim</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>6994-KERXL</td>
      <td>Masculino</td>
      <td>0</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>4</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>DSL</td>
      <td>Nao</td>
      <td>...</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>Sim</td>
      <td>Mensal</td>
      <td>Sim</td>
      <td>BoletoEletronico</td>
      <td>55.90</td>
      <td>238.5</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2181-UAESM</td>
      <td>Masculino</td>
      <td>0</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>2</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>DSL</td>
      <td>Sim</td>
      <td>...</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>Mensal</td>
      <td>Nao</td>
      <td>BoletoEletronico</td>
      <td>53.45</td>
      <td>119.5</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>5981</th>
      <td>0684-AOSIH</td>
      <td>Masculino</td>
      <td>0</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>1</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>Fibra</td>
      <td>Sim</td>
      <td>...</td>
      <td>Nao</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>Mensal</td>
      <td>Sim</td>
      <td>BoletoEletronico</td>
      <td>95.00</td>
      <td>95</td>
      <td>Sim</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5982</th>
      <td>5982-PSMKW</td>
      <td>Feminino</td>
      <td>0</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>23</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>DSL</td>
      <td>Sim</td>
      <td>...</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>2 anos</td>
      <td>Sim</td>
      <td>CartaoCredito</td>
      <td>91.10</td>
      <td>2198.3</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5983</th>
      <td>8044-BGWPI</td>
      <td>Masculino</td>
      <td>0</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>12</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>SemInternet</td>
      <td>...</td>
      <td>SemInternet</td>
      <td>SemInternet</td>
      <td>SemInternet</td>
      <td>Mensal</td>
      <td>Sim</td>
      <td>BoletoEletronico</td>
      <td>21.15</td>
      <td>306.05</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5984</th>
      <td>7450-NWRTR</td>
      <td>Masculino</td>
      <td>1</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>12</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>Fibra</td>
      <td>Nao</td>
      <td>...</td>
      <td>Nao</td>
      <td>Sim</td>
      <td>Sim</td>
      <td>Mensal</td>
      <td>Sim</td>
      <td>BoletoEletronico</td>
      <td>99.45</td>
      <td>1200.15</td>
      <td>Sim</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5985</th>
      <td>4795-UXVCJ</td>
      <td>Masculino</td>
      <td>0</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>26</td>
      <td>Sim</td>
      <td>Nao</td>
      <td>Nao</td>
      <td>SemInternet</td>
      <td>...</td>
      <td>SemInternet</td>
      <td>SemInternet</td>
      <td>SemInternet</td>
      <td>Anual</td>
      <td>Nao</td>
      <td>CartaoCredito</td>
      <td>19.80</td>
      <td>457.3</td>
      <td>Nao</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>5986 rows × 22 columns</p>
</div>



```python
#Passo 3: Tratamento de dados
# - tratar os valores que estão reconhecidos de forma errada
tabela["TotalGasto"] = pd.to_numeric(tabela["TotalGasto"], errors="coerce")

# - tratar registros com muitos valores vazios
# - deletando colunas vazias
# obs.: axis = 0  x -> linha   ou   axis = 1 x -> linha
tabela = tabela.dropna(how="all", axis=1)
# - deletando linhas vazias
tabela = tabela.dropna(how="any", axis=0)

print(tabela.info())

```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 5974 entries, 0 to 5985
    Data columns (total 21 columns):
     #   Column                  Non-Null Count  Dtype  
    ---  ------                  --------------  -----  
     0   IDCliente               5974 non-null   object 
     1   Genero                  5974 non-null   object 
     2   Aposentado              5974 non-null   int64  
     3   Casado                  5974 non-null   object 
     4   Dependentes             5974 non-null   object 
     5   MesesComoCliente        5974 non-null   int64  
     6   ServicoTelefone         5974 non-null   object 
     7   MultiplasLinhas         5974 non-null   object 
     8   ServicoInternet         5974 non-null   object 
     9   ServicoSegurancaOnline  5974 non-null   object 
     10  ServicoBackupOnline     5974 non-null   object 
     11  ProtecaoEquipamento     5974 non-null   object 
     12  ServicoSuporteTecnico   5974 non-null   object 
     13  ServicoStreamingTV      5974 non-null   object 
     14  ServicoFilmes           5974 non-null   object 
     15  TipoContrato            5974 non-null   object 
     16  FaturaDigital           5974 non-null   object 
     17  FormaPagamento          5974 non-null   object 
     18  ValorMensal             5974 non-null   float64
     19  TotalGasto              5974 non-null   float64
     20  Churn                   5974 non-null   object 
    dtypes: float64(2), int64(2), object(17)
    memory usage: 1.0+ MB
    None
    


```python
#Passo 4: Análise Inicial
# como estão os nossos cancelamentos (churn) ?
display(tabela["Churn"].value_counts())
display(tabela["Churn"].value_counts(normalize = True).map("{:.1%}".format))
```


    Nao    4387
    Sim    1587
    Name: Churn, dtype: int64



    Nao    73.4%
    Sim    26.6%
    Name: Churn, dtype: object



```python
#Passo 5: Análise Mais Completa
# - comparar cada coluna da tabela com a coluna de cancelamento
import plotly.express as px

# ao trabalhar com gráficos existem 2 etapas:
# etapa 1- criar os gráficos
for coluna in tabela.columns:
    # para edições nos gráficos: https://plotly.com/python/histograms/
    # para mudar a cor do gráfico , color_discrete_sequence=["blue", "green"]
    grafico = px.histogram(tabela, x=coluna, color="Churn")
    # etapa 2- exibir os gráficos
    grafico.show()
```
<h3>Gráficos gerados pelo comando grafico.show():</h3>



<h1>Conclusões</h1>

Clientes com contrato mensal tem MUITO mais chance de cancelar:
    Podemos fazer promoções para o cliente ir para o contrato anual
    
Familias maiores tendem a cancelar menos do que famílias menores
    Podemos fazer promoções pra pessoa pegar uma linha adicional de telefone para um parente, ou dependente
    
MesesComoCliente baixos tem MUITO cancelamento. Clientes com pouco tempo como cliente tendem a cancelar muito
    A primeira experiência do cliente na operadora pode ser ruim
    Talvez a captação de clientes esteja sendo feita de maneira errada trazendo clientes desqualificados
    Ideia: a gente pode criar incentivo para os clientes ficarem mais tempo como cliente
    
Quanto mais serviços o cliente tem, menos chance dele cancelar
    Podemos fazer promoções com mais serviços pro cliente
    
Pode estar ocorrendo algum problema no nosso serviço de Fibra que tá fazendo os clientes cancelarem
    Investigar serviço de fornecimento de produtos com fibra ótica
    
Clientes no boleto tem MUITO mais chance de cancelar
    Podemos fazer alguma ação para eles migrarem para as outras formas de pagamento


```python

```

# Relatório Operacional de Pré-Decolagem - FIAP
Esse projeto apresenta um sistema operacional de pré-decolagem para uma missão espacial fictícia. O objetivo é construir um algoritmo capaz de avaliar as condições de segurança da missão e determinar se está pronto para decolagem. A atividade faz parte do curso de **Ciência da Computação** da instituição **FIAP**.

---

## Instruções de execução do código
As instruções a seguir visam orientar a execução do projeto no ambiente do **Google Colab**:
1. Baixe o arquivo notebook (`.ipynb`);
2. Baixe os arquivos de dados (`.csv`) correspondentes à telemetria;
3. Acesse o [Google Colab](https://colab.research.google.com/);
4. Faça o upload do arquivo `.ipynb`;
5. Carregue os arquivos `.csv` para o ambiente de execução;
6. Execute as células sequencialmente para reproduzir a simulação e as validações.

---

## Organização e Dados da Telemetria
O algoritmo de verificação analisa diversas categorias de parâmetros críticos da espaçonave. A partir de faixas de segurança predefinidas, o sistema toma a decisão operacional:

* **Temperatura Interna (°C):** 18 a 32  
* **Temperatura Externa (°C):** -8 a 30  
* **Níveis de Energia (%):** $\ge 80$  
* **Tensão da Bateria (V):** 26 a 30  
* **Corrente da Bateria (A):** 10 a 25  
* **Potência Instantânea (kW):** 0,30 a 0,80  
* **Pressão dos Tanques (bar):** 90 a 140  
* **Integridade Estrutural:** Igual a 1 (OK)  
* **Módulos Críticos:** Todos em "OK"

  ---

## Análise Energética

Cálculos responsáveis por definir a autonomia e a viabilidade energética da missão antes do empuxo de subida:

* **Capacidade Total:** 120 kWh  
* **Carga Atual:** 80% a 100%  
* **Consumo Estimado na Decolagem:** 30 a 40 kWh  
* **Perdas Energéticas:** 5% a 8%

---

## Prints da execução 
### 1. Execução da Telemetria (Sem Anomalias)
> Visualização dos registros em conformidade com as faixas de segurança operacionais.
<img width="3965" height="1117" alt="Tabela_Telemetria_Aurora_Sem_Anomalias" src="https://github.com/user-attachments/assets/bf76249a-149c-4cdd-ac43-40e4876894fb" />


### 2. Execução da Telemetria (Com Anomalias)
> Demonstração da injeção estocástica de falhas (ex: pressão excessiva nos tanques) resultando no aborto automático do lançamento.
<img width="3965" height="1117" alt="Tabela_Telemetria_Aurora_Anomalias" src="https://github.com/user-attachments/assets/ff1de7f9-9de5-4668-b0a8-db0072700379" />


### 3. Log de Execução do Script em Python
> Saída detalhada do terminal simulando a auditoria linha por linha da telemetria da Missão Aurora.
<img width="2007" height="1589" alt="script_python_execucao" src="https://github.com/user-attachments/assets/edf533ce-f145-4125-9143-261aa03b1c7b" />

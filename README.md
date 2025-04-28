# 🚛 Sistema de Auditoria de Apontamentos de Frota

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-blue?logo=pandas)
![OpenPyXL](https://img.shields.io/badge/OpenPyXL-Excel_Processing-green?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

Solução profissional para auditoria de apontamentos de frota com abastecimentos, horímetros e quilometragens.

## 📋 Estrutura do Arquivo de Entrada

| Coluna          | Tipo      | Descrição                              | Exemplo                   |
|-----------------|-----------|----------------------------------------|---------------------------|
| ORIGEM          | string    | Fonte do dado                          | "OFICIAL"                 |
| INSTANCIA       | int       | Unidade operacional                    | 91                        |
| BOLETIM         | int       | Número do documento                    | 1939                      |
| FROTA           | int       | Número da frota                        | 65229                     |
| MARCA           | string    | Fabricante do veículo                  | "VOLVO"                   |
| MODELO          | string    | Modelo do equipamento                  | "FH 520 6X4T"             |
| CATEGORIA       | string    | Classificação do veículo               | "CAMINHÃO TRANSP. DIVERSOS"|
| HR_OPERACAO     | datetime  | Data e hora da operação                | "01/03/2023 00:00:20"     |
| CD_MATERIAL     | int       | Código do material                     | 251081                    |
| COMBUSTIVEL     | string    | Tipo de combustível                    | "ÓLEO DIESEL"             |
| TIPO_RODADO     | string    | Tipo de medição (HR/KM)                | "KM"                      |
| QTD             | float     | Quantidade abastecida                  | 215.11                    |
| NO_HOR_ODOM     | float     | Horímetro ou odômetro                  | 513723                    |
| KM              | float     | Quilometragem percorrida               | 430.2                     |

## 🛠️ Funcionalidades

### 🔍 Análise de Consistência
- Verificação de sequência de horímetros
- Detecção de registros fora de ordem cronológica
- Identificação de saltos inconsistentes

### ⚡ Processamento de Dados
- Conversão automática de tipos
- Tratamento de valores decimais
- Padronização de datas

### 📊 Saídas Geradas
- `Correção_de_horímetros.xlsx`
- `Instancias_divergentes.xlsx` 
- `Apontamentos_duplicados.xlsx`

## 🚀 Como Usar

1. Prepare seu arquivo no formato especificado
2. Execute o Jupyter Notebook
3. Os relatórios serão gerados automaticamente

```python
# Exemplo de carga de dados
import pandas as pd
dados = pd.read_excel('APONTAMENTOS.xlsx')
```

## 📄 Licença
MIT License - Copyright (c) 2023 Luiz Felipe Souza
[<img src="https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin" alt="LinkedIn">](https://www.linkedin.com/in/luizfelipesouzaeag/)

# MLP para Predição de Evasão Escolar — UFRB

Rede Neural Multicamadas (MLP) para prever a evasão de alunos de graduação da Universidade Federal do Recôncavo da Bahia (UFRB), a partir de dados socioeconômicos e acadêmicos.

**Resultado principal:** AUC-ROC de 0,943 no conjunto de teste, superando os baselines reportados na literatura para o mesmo tipo de problema.

## Sobre o problema

Evasão escolar é o abandono do curso antes da conclusão. Identificar com antecedência quais alunos têm maior probabilidade de evadir permite que a instituição direcione ações de apoio (bolsas, acompanhamento pedagógico, suporte psicológico) para quem mais precisa, antes que o abandono aconteça.

Este projeto treina um classificador binário (evade / não evade) usando um Multilayer Perceptron (MLP), com dados históricos de alunos da UFRB.

## Resultados

| Métrica | Valor |
|---|---|
| AUC-ROC | 0,943 |
| Acurácia | 87% |
| Recall (evasão) | 86,3% |
| Especificidade | 88% |
| Precisão (evasão) | 90,4% |

### Comparação com a literatura

| Estudo | Modelo | Métrica |
|---|---|---|
| Teodoro, 2020 | Random Forest | AUC-ROC 0,88 |
| Sulak, 2024 | ANN | Acurácia 77,3% |
| **Este projeto** | **MLP** | **AUC-ROC 0,943 / Acurácia 87%** |

## Dataset

- **Instituição:** UFRB
- **Período:** 2017 a 2022
- **Alunos:** 9.165
- **Features:** 28 (variáveis socioeconômicas e acadêmicas)
- **Split:** 80% treino / 20% teste

> Os dados utilizados são registros acadêmicos internos da UFRB e não estão incluídos neste repositório por questões de privacidade. O notebook assume que os dados já estão disponíveis em formato tabular compatível — veja a seção [Como executar](#como-executar) para detalhes de formato esperado.

## Arquitetura e hiperparâmetros

- **Otimizador:** Adam (learning rate = 0,001)
- **Regularização:** L2 (0,003)
- **Early stopping:** patience = 25
- **Batch size:** 64

## Estrutura do repositório

```
mlp-evasao-ufrb/
├── MLP_Evasao_Escolar_ModeloFinal.ipynb   # Notebook com pré-processamento, treino e avaliação
├── requirements.txt                        # Dependências do projeto
└── README.md
```

## Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/LincolnShow12/mlp-evasao-ufrb.git
   cd mlp-evasao-ufrb
   ```

2. Crie um ambiente virtual e instale as dependências:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Abra o notebook:
   ```bash
   jupyter notebook MLP_Evasao_Escolar_ModeloFinal.ipynb
   ```

4. Execute as células em ordem. O notebook cobre: carregamento e limpeza dos dados, pré-processamento das 28 features, treino do MLP e avaliação com as métricas descritas acima.

## Autores

- Alex
- Antonio Francisco
- Lincoln Meira de Santana

**Orientador:** Dr. Tiago Palma Pagano

Projeto desenvolvido no curso de Engenharia de Computação — UFRB.

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Se este trabalho foi útil para você, considere deixar uma ⭐.
---

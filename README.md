# 🧠 MLP para Predição de Evasão Escolar - UFRB

## 📌 Sobre o Projeto
Rede Neural Multicamadas (MLP) para prever evasão de alunos da UFRB.
🎯 **AUC-ROC de 94,3%** no conjunto de teste.

## 📊 Resultados Principais
- 🎯 AUC-ROC: **0,943 (94,3%)**
- 📈 Acurácia: **87%**
- 🔍 Recall (evasão): **86,3%**
- ✅ Especificidade: **88%**
- 🎯 Precisão (evasão): **90,4%**

## 🏗️ Arquitetura do Modelo

**Parâmetros:**
- ⚙️ Otimizador: Adam (lr=0,001)
- 📉 L2 regularization: 0,003
- 🛑 Early stopping: patience=25
- 📦 Batch size: 64

## 🗃️ Dataset
- 🏫 Instituição: **UFRB**
- 📅 Período: **2017 a 2022**
- 👨‍🎓 Alunos: **9.165**
- 🔧 Features: **28** (socioeconômicas + acadêmicas)
- 
## 📚 Comparação com Literatura
- 🌲 Random Forest (Teodoro, 2020): AUC-ROC 0,88 → **nosso modelo: 0,943** ✅
- 🧠 ANN (Sulak, 2024): Acurácia 77,3% → **nosso modelo: 87%** ✅

## 👥 Autores
- 👤 Alex
- 👤 Antonio Francisco
- 👤 Lincoln

**Orientador:** Dr. Tiago Palma Pagano

📚 **Engenharia de Computação - UFRB**

## 🔗 Repositório
https://github.com/LincolnShow12/mlp-evasao-ufrb

---

⭐ Se este trabalho foi útil, deixe uma estrela!
- ✂️ Split: 80% treino / 20% teste

## 📋 Matriz de Confusão (Teste)

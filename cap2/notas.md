# Métodos Preditivos vs Inferenciais — Anotações (ISLP)

A diferença entre um **foco preditivo** e um **foco inferencial** está principalmente na **construção do modelo** e na **interpretabilidade**.

Em **métodos preditivos**, não nos importamos com a forma da função de estimação, desde que ela produza estimativas suficientemente boas.

Existe **erro redutível** e **erro irredutível**.  
A diferença entre eles consiste em quanto da variável resposta pode ser explicado pelas preditoras. A ideia é que, ao melhorarmos o modelo, reduzimos o erro, mas existe um limite para essa redução. Mesmo com o melhor modelo possível, ainda haverá o erro irredutível associado — seja por limitações na seleção de features ou por outros fatores não observáveis.

- **Métodos preditivos** → foco total em predição: classificação correta ou regressão suficientemente próxima  
- **Métodos inferenciais** → foco nas relações entre preditoras e resposta: qual feature é mais importante e como essa relação ocorre  

---

## Métodos Paramétricos e Não Paramétricos

- **Métodos paramétricos** assumem um formato funcional para reduzir o problema de estimação  
- **Métodos não paramétricos** não impõem uma forma funcional fixa, oferecendo maior flexibilidade ao custo de maior complexidade  

---

## Trade-off: Interpretabilidade vs Flexibilidade

Existe um trade-off entre **interpretabilidade** e **flexibilidade do modelo**.

Modelos mais restritivos tendem a ser mais fáceis de interpretar e, consequentemente, mais adequados para métodos inferenciais.

Modelos não paramétricos, não lineares e mais complexos — como splines, deep learning, entre outros — possuem alta flexibilidade, mas tornam o processo de interpretabilidade extremamente complexo.

---

## Métodos Supervisionados e Não Supervisionados

- **Métodos supervisionados** estão associados a uma variável resposta.  
  Existe uma função a ser estimada, seja para:
  - predizer valores da variável resposta (abordagem preditiva)  
  - entender as relações entre a resposta e suas preditoras (abordagem inferencial)  

  Problemas desse tipo incluem **regressão** e **classificação**.

- **Métodos não supervisionados** subvertem essa lógica.  
  Não há variável resposta, apenas um conjunto de variáveis \( X_i \).  
  O objetivo é entender melhor as relações existentes entre essas variáveis.

  Problemas desse tipo incluem **redução de dimensionalidade** e **clustering**.

---

## Overfitting, Treino e Teste

O tema do **overfitting** é abordado de forma tangencial, explicando por que avaliar modelos apenas pelo MSE de treino pode ser problemático.  
Modelos que se ajustam muito bem aos padrões da base de treino podem falhar em generalizar para a base de teste.

---

## Graus de Liberdade e Flexibilidade

> *"The degrees of freedom is a quantity that summarizes the flexibility of a curve."*

Essa é uma abordagem alternativa para entender graus de liberdade, associando-os diretamente à flexibilidade do modelo.

---

## KNN e Viés-Variância

Aumentar o número \( K \) no **KNN** torna o modelo menos flexível:

- \( K = 1 \) → **alta variância**, **baixo viés**  
- \( K = 100 \) → **alto viés**, **baixa variância**  

Isso faz sentido, pois ao aumentar a quantidade de vizinhos utilizados para definir a predição, cada ponto individual passa a ter menor influência direta no modelo.

---

## Tópicos Abordados

1. Métodos preditivos e inferenciais  
2. Métodos paramétricos e não paramétricos  
3. Trade-off entre interpretabilidade e flexibilidade  
4. Métodos supervisionados e não supervisionados  
5. Regressão vs classificação  
6. Diferença entre base de treino e base de teste  
7. Método KNN  

---

> **Nota:** *Pesquisar citação* — “There is no free lunch in statistics”.

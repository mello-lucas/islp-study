# Notas cap3 - Regressão Linear

OLS é não enviesado, ou seja, se estimarmos os paramêtros de uma população com várias amostras dessa população, na média iremos nosso estimador irá se aproximar da valor real da população.

**Diferença entre erro padrão e desvio padrão**: 

Desvio padrão mede a dispersão dos dados individuais em torno da média da população ou da amostra.

Erro padrão mede a variabilidade amostral de um estimador, isto é, o quanto o estimador varia em torno do verdadeiro parâmetro populacional quando repetimos o processo de amostragem.

**Definição correta de intervalo de confiança:**

Um ponto de confunsão frequente é a interpretação de um intervalo de confiança. Um IC(95%) não possui 95% de probabilidade de conter o verdadeiro valor do parâmetro, a probabilidade está associada ao procedimento de construção do intevalo, e não a um intervalo específico após os dados serem observados. 

Um intervalo de confiança de 95% é construído por um procedimento que, se repetido infinitas vezes sob as mesmas condições, gera intervalos que contêm o verdadeiro parâmetro populacional em 95% das amostras.

**R2:**

O coeficiente de determinação, denotado por \(R^2\), é amplamente utilizado na avaliação de modelos de regressão linear. Ele mede a **proporção da variabilidade da variável resposta** que é explicada pelo modelo, em comparação com um modelo nulo que utiliza apenas a média da variável resposta.

Valores de \(R^2\) próximos de 1 indicam que o modelo explica grande parte da variabilidade observada em \(y\), enquanto valores próximos de 0 indicam que o modelo possui poder explicativo semelhante ao de um modelo sem regressores.

O coeficiente de determinação para um fit com múltiplas váriaveis sempre irá aumentar conforme novas variáveis forem adicionadas, devido a isso é sempre recomendado avaliar o R2 ajustado.

**Suposições regressão linear:**

aditiva -> A associação entre a preditora Xj e a target Y não depende de outras preditoras. | Pode ser relaxada com termos de interação.

linear -> Um aumento de uma unidade em Xj sempre representa o mesmo aumento em Y, independente do valor de Xj. | Pode ser relaxada com transformações, termos polinomiais, splines ou GAMs.

**Diferença entre intervalo de confiança e de predição:**

O intervalo de confiança mede a incerteza da média estimada do processo, enquanto o intervalo de predição mede a incerteza de um datapoint específico.
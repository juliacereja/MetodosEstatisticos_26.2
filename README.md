# 📊 Resumo de Estatística — Revisão para Prova

---

## 1. Classificação de Variáveis

Perguntas para checar uma variável:

- **Válida?** → mede realmente o que diz medir
- **Confiável?** → dá resultado consistente
- **Qualitativa?** → **nominal** (sem ordem) ou **ordinal** (com ordem)
- **Quantitativa?** → **discreta** (contável) ou **contínua** (mensurável)

**Distribuição de variável categórica:** quais categorias existem e quantas (ou que %) das observações caem em cada uma.

---

## 2. 🚨 Gráficos Enganosos

| Armadilha | Por que engana |
|---|---|
| Pizza em 3D | Efeito de perspectiva falho — distorce o tamanho aparente das fatias |
| Eixo de barras que não começa em 0 | Diferenças pequenas parecem enormes |
| Pizza para mostrar mudança no tempo | Os números não são partes de um mesmo todo |
| Imagens distorcidas representando um valor | Enganam sobre o tamanho real da diferença |

> ⚠️ **Framing:** a escolha de qual dado enfatizar nunca é neutra, mesmo representando os mesmos dados.

---

## 3. Histograma

Resume a distribuição de uma variável **quantitativa** com infinitos valores possíveis, agrupando valores próximos em **faixas (classes)** e contando quantas observações caem em cada uma.

**Regras de construção:**
- Classes com **largura igual**
- Barras **coladas**, sem espaço entre elas
- Eixo X é uma **escala numérica contínua** dividida em faixas *(diferente do gráfico de barras, onde o eixo X são categorias separadas)*

**O que descrever:**
- **Centro** — onde os dados se concentram
- **Variabilidade** — o quão espalhados estão os valores
- **Forma:**
  - Simétrica
  - Assimétrica à **direita** → maioria dos valores baixos, outliers altos (média maior que a mediana)
  - Assimétrica à **esquerda** → maioria dos valores altos, outliers baixos
- **Desvio** — existe um outlier?

---

## 4. Série Temporal

Mostra como uma variável muda ao longo do tempo.

- **Tendência** — movimento geral de subida/descida, ignorando os picos
- **Ciclo** — ondulações para cima e para baixo (picos)
- **Padrão geral** = tendência + ciclos
- **Desvio** — pico ou vale muito fora do esperado, que merece explicação

**Comparando grupos:**
- **Sobreposição** — duas ou mais séries no mesmo gráfico, com cores diferentes
- **Facetamento** — um mini gráfico separado por grupo, lado a lado (evita poluir um gráfico só)

---

## 5. Medidas de Tendência Central

| Medida | Resistente a outliers? | Observação |
|---|---|---|
| **Média** | ❌ Não | Um único valor fora do padrão distorce ela |
| **Mediana** | ✅ Sim | Depende só da posição, não do tamanho do dado |
| **Moda** | — | Funciona para qualquer tipo de dado; pode ser unimodal, bimodal, amodal ou plurimodal |

> ⚠️ Em distribuição **assimétrica**, a **mediana** é a medida mais confiável pra descrever o típico.
> Nenhuma das três (média, mediana, moda) evidencia o quão espalhados os dados estão.

---

## 6. Quartis

Dividem os dados **ordenados** em 4 partes iguais:

- **Q1** — valor abaixo do qual estão 25% dos dados (mediana da metade de baixo)
- **Q3** — valor abaixo do qual estão 75% dos dados (mediana da metade de cima)

**Amplitude interquartil (IQR) = Q3 − Q1**
- Mede o quão espalhados estão os **50% centrais** dos dados
- É **resistente** (ignora as pontas/extremos)
- Mostra o quão concentradas as observações estão em torno da mediana

---

## 7. Medidas de Dispersão

- **Desvio médio** — distância média de cada ponto até o centro (em módulo)
- **Variância** — usa **n − 1**, valores sempre ao quadrado
- **Desvio padrão** — quanto **maior**, mais espalhados (heterogêneos) os dados estão em torno da média; quanto **menor**, mais parecidos entre si

**Qual resumo usar:**
- Dados **simétricos e sem outliers** → média + desvio padrão
- Dados **assimétricos ou com outliers** → resumo dos 5 números (mínimo, Q1, mediana, Q3, máximo)

---

## 8. Da Ideia ao Número: Conceito → Índice

\`\`\`
Conceito (abstrato)
   ↓
Variável (mensurável)
   ↓
Indicador (uma ou mais variáveis)
   ↓
Índice (vários indicadores combinados)
   ↓
volta a representar o conceito/fenômeno mais amplo
\`\`\`

**Propriedades de um bom indicador/índice:**
- **Validade** — mede o conceito certo
- **Confiabilidade** — dá resultado consistente
- **Cobertura** — representa bem toda a população de interesse
- **Transparência** — a forma de calcular é aberta, dá pra conferir
- **Comunicabilidade** — fácil de entender pelo público
- **Comparabilidade** ao longo do tempo — permite ver evolução ano a ano

---

## 9. Análise Bivariada

- **Variável explicativa (independente)** — a que pode influenciar
- **Variável resposta (dependente)** — o resultado que você quer entender
  - Ex.: nº de latas de cerveja (explicativa) → nível de álcool no sangue (resposta)

> ⚠️ **Correlação não implica causalidade** — duas variáveis podem andar juntas sem uma causar a outra (pode existir um terceiro fator por trás, tipo riqueza do país causando TV por pessoa **e** expectativa de vida ao mesmo tempo).

### Tabela de contingência
Usada quando as **duas variáveis são categóricas** — cruza as categorias de uma com as da outra.

**Regra do %:** fixa a explicativa e calcula o % da resposta dentro de cada categoria dela.

### Diagrama de dispersão
Usado quando as **duas variáveis são quantitativas** — explicativa no eixo X, resposta no eixo Y.

Descrito por:
- **Direção** — positiva (sobem juntas), negativa (uma sobe, outra desce), ou sem correlação
- **Forma** — reta, curva, etc.
- **Intensidade** — pontos colados numa reta = forte; espalhados = fraco

> ⚠️ **Cuidado:** a relação pode ser fortíssima mas **não-linear** (forma de "U", por exemplo) — aí um coeficiente de correlação linear engana, dando "fraco/zero" mesmo com um padrão bem claro. Por isso: **sempre olhe o gráfico.**

---

## 10. Coeficiente de Pearson (r)

- Mede a **direção** e a **intensidade** de uma relação **linear** entre duas variáveis quantitativas
- Padroniza os dados para entender o quanto os valores se afastam da média, positiva ou negativamente
- Produto positivo → relação positiva (as duas sobem juntas)
- Produto negativo → relação negativa (uma sobe, outra desce)
- **Intervalo:** r sempre fica entre **-1 e +1**

> ⚠️ **Pegadinhas do Pearson:**
> - r perto de 0 **não significa** "sem relação nenhuma" — só significa sem relação **linear**. Pode haver uma relação forte, só que curva (não-linear), e ainda assim dar r perto de zero.
> - **Não é resistente a outliers** — um valor bem fora do padrão pode distorcer o r sozinho.
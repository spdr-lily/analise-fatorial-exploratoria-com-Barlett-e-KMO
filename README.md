# analise-fatorial-exploratoria-com-Barlett-e-KMO
## 1. Objetivo

O objetivo deste projeto é realizar uma Análise Fatorial Exploratória (AFE) aplicada a um conjunto de dados simulados, com o propósito de identificar estruturas latentes associadas a traços de personalidade. A análise inclui testes de adequação, extração de fatores, avaliação de cargas fatoriais e interpretação dos resultados.

## 2. Metodologia
### 2.1 Importação de Bibliotecas

Foram utilizadas bibliotecas amplamente aceitas em pesquisa estatística e psicometria:
pandas — manipulação de dados
numpy — operações matemáticas
matplotlib / seaborn — visualização
scipy.stats — testes estatísticos
factor_analyzer — análise fatorial
sklearn.preprocessing — padronização

## 3. Preparação dos Dados
### 3.1 Geração dos Dados

O conjunto de dados foi simulado para representar 3 fatores latentes de personalidade, cada um associado a um subconjunto de itens (perguntas tipo Likert 1–5).
Foram gerados:

14 itens distribuídos entre 3 fatores

300 respondentes

Estrutura com correlações internas, simulando consistência psicométrica

Após geração das variáveis latentes, os resultados foram convertidos para a escala Likert para posterior análise.

## 4. Testes de Adequação da AFE
### 4.1 Teste de Bartlett

O Teste de Esfericidade de Bartlett foi aplicado para verificar se a matriz de correlação é adequada para redução de dimensionalidade.

Critério:

p < 0.05 indica que a AFE é apropriada.

4.2 Medida KMO (Kaiser-Meyer-Olkin)

Avalia o grau de correlação parcial entre as variáveis.

Critérios:

0.80 excelente

0.70 bom

0.60 aceitável

< 0.50 inadequado

O resultado global KMO calculado foi:

KMO Global: [valor calculado no notebook]

## 5. Determinação do Número de Fatores

Foi utilizado o Scree Plot, baseado na análise dos autovalores (eigenvalues).
Critérios aplicados:

Regra de Kaiser (fatores com eigenvalue > 1)

Inspeção visual do ponto de inflexão (“cotovelo”)

A evidência gráfica sugeriu 3 fatores, compatível com a estrutura latente previamente simulada.

## 6. Extração e Rotação dos Fatores
Método de Extração

Principal Axis Factoring (PAF) — apropriado para dados psicométricos não normalizados.

Método de Rotação

Varimax (ortogonal)

Facilita interpretabilidade, maximizando cargas em um único fator

## 7. Cargas Fatoriais

As cargas fatoriais obtidas permitiram:

Identificar itens que carregam fortemente em cada fator

Confirmar a coerência entre a estrutura simulada e a estrutura extraída

Critérios utilizados:

Cargas > 0.40 foram consideradas significativas

Itens com cargas cruzadas foram revisados para avaliar ambiguidade semântica

## 8. Interpretação dos Fatores

Os três fatores foram interpretados como:

Fator 1 — Traço Psicológico A
(ex.: Extroversão, se os itens assim o indicassem)

Fator 2 — Traço Psicológico B

Fator 3 — Traço Psicológico C

A interpretação depende do conteúdo semântico dos itens simulados.

## 9. Conclusões

A AFE demonstrou boa adequação estatística (Bartlett e KMO aceitáveis).

O Scree Plot confirmou a existência de 3 fatores principais, compatíveis com a estrutura simulada.

As cargas fatoriais apresentaram padrões claros, permitindo boa separação entre os fatores.

O conjunto de dados simulado apresentou propriedades psicométricas realistas, adequadas à aplicação de técnicas fatoriais.

## 10. Reprodutibilidade

Para reproduzir o experimento, é necessário:

Executar todas as células do notebook

Instalar o pacote factor_analyzer

Garantir versão recente do Python (>= 3.9)

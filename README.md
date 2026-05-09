[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/zHqjFsRx)
# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto:não lembro
- cadeia:não lembro
- linguagem:não lembro
- gramática:não lembro
- autômato finito:não lembro
- linguagem regular:não lembro
- linguagem livre de contexto:não lembro
- linguagem sensível ao contexto:não lembro
- linguagem irrestrita:não lembro
- hierarquia de Chomsky:não lembro
- computabilidade:não lembro
- máquina de Turing:lembro parcialmente

2. Definições com exemplo
1. O que é um alfabeto?

Um alfabeto é um conjunto de símbolos usados para formar palavras ou cadeias.

Exemplo usando:

Σ = {a, b}

Nesse caso, só podemos usar as letras a e b.

2. O que é uma cadeia?

Uma cadeia é uma sequência de símbolos do alfabeto.

Exemplos:

a
ab
bba
aaab

Todas essas cadeias utilizam apenas símbolos do alfabeto {a,b}.

3. O que é uma linguagem?

Uma linguagem é um conjunto de cadeias que seguem uma regra.

Exemplo:

L = { cadeias que terminam com b }

Cadeias que pertencem:

b
ab
aab
bb

Cadeias que não pertencem:

a
aba
4. O que é uma gramática?

Uma gramática é um conjunto de regras usado para gerar cadeias de uma linguagem.

Exemplo:

S -> aS
S -> b

Essa gramática gera:

b
ab
aab
aaab

Ela produz várias letras a seguidas de um b.

3. Linguagens
Linguagem L1
L1 = { w em {0,1}* | w termina com 01 }
1. Escreva três palavras que pertencem à linguagem
01
101
1101
2. Escreva duas palavras que não pertencem
10
111
3. Diga, se souber, em qual classe ela provavelmente se encaixa

Provavelmente é uma linguagem regular.

4. Explique o motivo em linguagem simples

Porque basta verificar os dois últimos símbolos da cadeia. Um autômato finito consegue fazer isso facilmente.

Linguagem L2
L2 = { a^n b^n | n >= 0 }
1. Escreva três palavras que pertencem à linguagem
ab
aabb
aaabbb

Também existe:

ε

(cadeia vazia, quando n = 0)

2. Escreva duas palavras que não pertencem
aab
abb
3. Diga, se souber, em qual classe ela provavelmente se encaixa

Provavelmente é livre de contexto.

4. Explique o motivo em linguagem simples

Porque a quantidade de letras a precisa ser igual à quantidade de letras b. Um autômato finito não consegue contar indefinidamente, mas uma pilha consegue.

Linguagem L3
L3 = { a^n b^n c^n | n >= 0 }
1. Escreva três palavras que pertencem à linguagem
abc
aabbcc
aaabbbccc
2. Escreva duas palavras que não pertencem
aabcc
aaabbcc
3. Diga, se souber, em qual classe ela provavelmente se encaixa

Provavelmente é sensível ao contexto.

4. Explique o motivo em linguagem simples

Porque é necessário garantir ao mesmo tempo a mesma quantidade de a, b e c, o que é mais complexo do que linguagens livres de contexto.

4. Autômato finito

Considere o autômato:

Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
1. Qual linguagem esse autômato parece reconhecer?

Ele parece reconhecer cadeias que terminam com:

01

Porque o estado final q2 é alcançado quando aparece um 1 depois de um 0.

2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita
Cadeia 01
q0 --0--> q1
q1 --1--> q2

Resultado: aceita.

Cadeia 101
q0 --1--> q0
q0 --0--> q1
q1 --1--> q2

Resultado: aceita.

Cadeia 100
q0 --1--> q0
q0 --0--> q1
q1 --0--> q1

Resultado: rejeita.

Cadeia 1101
q0 --1--> q0
q0 --1--> q0
q0 --0--> q1
q1 --1--> q2

Resultado: aceita.

Cadeia 111
q0 --1--> q0
q0 --1--> q0
q0 --1--> q0

Resultado: rejeita.

3. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias
Cadeia 101
Símbolo	Estado
início	q0
1	q0
0	q1
1	q2

Resultado: aceita.

Cadeia 100
Símbolo	Estado
início	q0
1	q0
0	q1
0	q1

Resultado: rejeita.

5. Gramática

Considere a gramática:

S -> aS
S -> b
1. Gere cinco cadeias produzidas por essa gramática
b
ab
aab
aaab
aaaab
2. Descreva a linguagem em palavras

A linguagem possui várias letras a seguidas de um único b no final.

3. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples

Ela parece ser uma gramática regular.

Justificativa:

As regras seguem um padrão simples e não precisam de memória complexa para funcionar.

Ela representa algo como:

a* b
6. Ponto de dificuldade
1. O que você entende dele

Entendo que linguagens formais possuem regras e que autômatos servem para reconhecer cadeias válidas.

2. Onde você se confunde

Tenho dificuldade em diferenciar quando uma linguagem é regular, livre de contexto ou sensível ao contexto.

3. Que tipo de explicação ajudaria

Exercícios guiados e exemplos passo a passo comparando as classes de linguagens.

## 7. Uso de IA, se houver

Pergunta feita:
"Explique linguagens formais, autômatos e gramáticas com exemplos simples."

Resumo da resposta:
A IA explicou os conceitos básicos de alfabetos, cadeias, linguagens, gramáticas e classes de linguagens.

Como eu verifiquei:
Comparei com anotações da aula e exemplos vistos pelo professor.

O que eu alterei na minha resposta:
Reescrevi as explicações com palavras mais simples e adicionei exemplos próprios.

O que ainda não entendi:
Ainda tenho dúvidas sobre a diferença entre linguagens livres de contexto e sensíveis ao contexto.
## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório: diagn-stico-de-retomada-teoria-da-computa-o-KaineLirines

Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```

# Sistema de Notas – Prova Prática Paradigmas de Programação
**Discente:** Tereza Clarice da Silva Rocha 
**Linguagem:** Python 3 

## O que o programa faz:

Lê os dados de notas de alunos de uma escola (nome, duas notas e faltas), calcula a média de cada um e mostra quem foi aprovado/reprovado.

**Regra:** é aprovado quem tem média **6.0 ou mais** e **no máximo 8 faltas**.

## Como rodar

```bash
python3 Sistema_Notas.py
```

Exemplo Saída:

```
=== RELATÓRIO DA TURMA ===
Ana    média 8.8  ->  APROVADO
Bruno  média 5.8  ->  REPROVADO
Carla  média 5.5  ->  REPROVADO
Diego  média 9.8  ->  APROVADO
Gabriel média 8.8  ->  APROVADO
------------------------------
Aprovados: 3 | Reprovados: 2
Média da turma: 7.7 | Melhor média: 9.8
```

## Divisão entre os paradigmas utilizados:

| Etapa | Função | Paradigma | O que faz |
|---|---|---|---|
| 1 | `carregar_alunos` | Imperativo | Transforma o texto em dados, usando laço e lista |
| 2 | `analisar_turma` | Funcional | Calcula médias e aprovados sem alterar nada |
| 3 | `exibir_relatorio` | Imperativo | Mostra o resultado e conta aprovados/reprovados |
| – | `main` | Imperativo | Chama as etapas 1, 2 e 3 na ordem |

## Pilares usados

### Imperativo
- **Estado mutável:** variáveis que mudam de valor (a lista `alunos` e os contadores).
- **Sequência de comandos:** as instruções rodam na ordem em que foram escritas.
- **Estruturas de controle:** `for` e `if`/`else` controlam o fluxo.
- **Efeitos colaterais:** o `print` mostra algo na tela.

### Funcional
- **Funções puras:** `calcular_media`, `esta_aprovado` e `arredondar` só dependem do que recebem e não mudam nada fora delas.
- **Imutabilidade:** o resultado é guardado em tuplas e em um dicionário novo.
- **Funções de ordem superior:** `map`, `filter`, `reduce` e `compor` recebem ou devolvem funções.
- **Recursão:** `maior_valor` chama a si mesma em vez de usar laço.
- **Composição:** `compor` junta `arredondar` e `str` em uma função só.

## Requisitos 

| Pedido | Como foi atendido |
|---|---|
| Paradigmas imperativo e funcional | Os dois no mesmo programa |
| Indicar os pilares nos trechos | Mostrado em Pilares Utilizados |
| Em C ou Python | Python |
| Mínimo de 3 funções | 9 funções |
| Mínimo de 3 tipos de dados | 7 tipos (tabela abaixo) |

### Tipos de dados

| Tipo | Onde aparece |
|---|---|
| `str` | nomes dos alunos |
| `int` | faltas e `MAX_FALTAS` |
| `float` | notas, médias e `MEDIA_MINIMA` |
| `bool` | resultado de `esta_aprovado` |
| `list` | `DADOS_BRUTOS` e `alunos` |
| `tuple` | cada aluno e as médias |
| `dict` | `contagem` e o resultado de `analisar_turma` |

## Conclusão

O programa mostra como que os paradigmas imperativo e funcional podem ser usados
juntos na mesma aplicação. O imperativo cuidou do fluxo, do estado e da saída
na tela (`for`, `if`, contadores e `print`). O funcional cuidou dos cálculos,
com funções puras, `map`, `filter`, `reduce` e recursão, sem alterar os dados.

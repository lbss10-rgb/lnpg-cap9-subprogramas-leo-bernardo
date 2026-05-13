# lnpg-cap9-subprogramas-leo-bernardo
# Atividade Prática — Capítulo 9: Subprogramas

**Disciplina:** Linguagens de Programação  
**Nome:** [Léo Bernardo da Silva Santos]  

## Descrição das Tarefas

### Tarefa 1 — Modularização em Java
Implementação de um sistema de controle acadêmico que cadastra 5 alunos, calcula médias e determina a situação (Aprovado, Recuperação ou Reprovado).  
**Versões desenvolvidas:** Monolítica e Modularizada.

### Tarefa 2 — Modularização em Python
Sistema de vendas que calcula subtotal, aplica desconto progressivo e imprime cupom fiscal.  
**Versões desenvolvidas:** Monolítica e Modularizada com funções.

### Tarefa 3 — Passagem de Parâmetros por Valor em Java
Demonstração do comportamento de passagem por valor com tipos primitivos (`int`).

### Tarefa 4 — Passagem de Referência de Objetos em Java
Demonstração do comportamento de objetos em Java (passagem da referência por valor).

### Tarefa 5 — Projeto Livre com Subprogramas
Sistema Bancário Simples totalmente modularizado.

---

## Instruções de Execução

### Java
```bash
# Compilar e executar (exemplos)
javac ControleAcademico.java && java ControleAcademico
javac PassagemPorValor.java && java PassagemPorValor
javac PassagemReferenciaObjeto.java && java PassagemReferenciaObjeto
javac SistemaBancario.java && java SistemaBancario

```
### Python
```bash
python sistema_vendas.py
```



Legibilidade: O código modularizado fica muito mais fácil de ler e entender, pois cada método tem um nome claro que revela sua intenção.
Reutilização: Funções como calcularMedia(), calcularDesconto() e imprimirRelatorio() podem ser facilmente reutilizadas em outros sistemas.
Facilidade de Manutenção: Alterar a lógica de aprovação ou a regra de desconto exige mudança em apenas um lugar.
Clareza do Fluxo: O main() fica curto e atua como orquestrador das chamadas.
Coesão: Cada subprograma possui alta coesão, realizando apenas uma tarefa bem definida.

Observações sobre a Modularização

Legibilidade: O código modularizado fica muito mais fácil de ler e entender, pois cada método tem um nome claro que revela sua intenção.
Reutilização: Funções como calcularMedia(), calcularDesconto() e imprimirRelatorio() podem ser facilmente reutilizadas em outros sistemas.
Facilidade de Manutenção: Alterar a lógica de aprovação ou a regra de desconto exige mudança em apenas um lugar.
Clareza do Fluxo: O main() fica curto e atua como orquestrador das chamadas.
Coesão: Cada subprograma possui alta coesão, realizando apenas uma tarefa bem definida.

Principais Conceitos Aplicados

.Modularização e Separação de Responsabilidades
.Passagem de Parâmetros (por valor e por referência de objeto)

.Retorno de valores

.Reutilização de código

.Boas práticas de coesão e legibilidade

Dificuldades Encontradas

.Gerenciar o buffer do Scanner ao alternar entre nextDouble() e nextLine().
.Entender que Java passa sempre por valor, mas no caso de objetos é copiado o valor da referência.
.Identificar quais partes do código eram boas candidatas a virarem subprogramas.

Vantagens Percebidias

A modularização trouxe maior organização, facilitou a depuração, melhorou significativamente a legibilidade e tornou o código mais profissional e próximo das boas práticas de programação.

Diagramas de Chamadas
Tarefa 1 — Controle Acadêmico (Java)

flowchart TD
    A[main] --> B[lerNome]
    A --> C[lerNotas]
    A --> D[calcularMedia]
    A --> E[determinarSituacao]
    A --> F[imprimirRelatorio]

    subgraph "Para cada aluno"
    B & C --> D --> E
    end
    E --> F

Tarefa 2 — Sistema de Vendas (Python)

flowchart TD
    A[Programa Principal] --> B[ler_produto]
    A --> C[calcular_subtotal]
    A --> D[calcular_desconto]
    A --> E[calcular_total]
    A --> F[imprimir_cupom]

    B --> C --> D --> E --> F

Tarefa 5 — Sistema Bancário Simples

flowchart TD
    A[main] --> B[exibirMenu]
    A --> C[depositar]
    A --> D[sacar]
    A --> E[consultarSaldo]

    B --> F{opção?}
    F -->|1| C
    F -->|2| D
    F -->|3| E
    F -->|4| G[Sair]

    C --> A
    D --> A
    E --> A

Observações sobre a Modularização

Legibilidade: Métodos curtos com nomes claros revelam a intenção do código.
Reutilização: Funções como calcularMedia(), calcularDesconto() e imprimirRelatorio() podem ser reutilizadas facilmente.
Manutenção: Alterações são feitas em um único local.
Clareza do Fluxo: O main() atua apenas como orquestrador.
Coesão: Cada subprograma possui uma única responsabilidade bem definida.

Dificuldades Encontradas

.Controle do buffer do Scanner no Java

.Compreensão profunda de que Java sempre usa passagem por valor (mesmo com objetos)

.Decidir o melhor nível de granularidade dos métodos

Vantagens Percebias da Modularização

.Código mais organizado e profissional

.Fácil depuração e teste individual de métodos

.Maior legibilidade e facilidade de manutenção

.Preparação para projetos maiores.



# Exercício: Tela de compra de tickets

Arquivo: `Tela de compra de tickets.html`

## Contexto

Um parque de diversões vai vender ingressos pela internet. Cada ingresso é comprado por um **responsável** para uma **criança**, e o parque exige os dados dos dois antes de liberar a entrada. O pagamento é feito com **cartão de crédito**.

Sua tarefa é montar a tela de compra em HTML: um formulário que coleta os dados do responsável, da criança e do cartão e mostra o valor total do ingresso.

## Objetivos

- Usar o tipo de `input` adequado para cada informação (`text`, `tel`, `email`, `date`, `number`).
- Aplicar validações nativas do HTML: `required`, `minlength`/`maxlength`, `min`/`max` e `pattern`.
- Organizar o formulário em grupos com `fieldset` e `legend`, e ligar cada campo ao seu texto com `label`.

> **Dica:** o CPF tem exatamente 14 caracteres porque está no formato `000.000.000-00`. Um `pattern` possível é `\d{3}\.\d{3}\.\d{3}-\d{2}`.

## Documentos

### Responsável

| Campo              | Tipo    | Validações                                        |
| ------------------ | ------- | ------------------------------------------------- |
| Nome               | `text`  | `required`, mínimo 5, máximo 50 caracteres        |
| CPF                | `text`  | `required`, mínimo 14, máximo 14, com `pattern`   |
| Telefone           | `tel`   | `required`                                        |
| E-mail             | `email` | `required`                                        |
| Data de nascimento | `date`  | `required`                                        |

### Criança

| Campo              | Tipo   | Validações                                      |
| ------------------ | ------ | ----------------------------------------------- |
| Nome               | `text` | `required`, mínimo 5, máximo 50 caracteres      |
| CPF                | `text` | `required`, mínimo 14, máximo 14, com `pattern` |
| Data de nascimento | `date` | `required`                                      |

## Forma de pagamento

### Cartão de crédito

| Campo            | Tipo     | Validações                                  |
| ---------------- | -------- | ------------------------------------------- |
| Número do cartão | `text`   | com `pattern`                               |
| Validade (mês)   | `number` | mínimo 1, máximo 12                         |
| Validade (ano)   | `number` | mínimo 2026, máximo 2036 (ano atual + 10)   |
| CVC              | `number` | mínimo 1, máximo 999                        |
| Nome no cartão   | `text`   | `required`, mínimo 5, máximo 50 caracteres  |

## Valor

Apresentar o valor total de **R$ 103,97**.

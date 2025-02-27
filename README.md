# Documentação do Sistema Bancário Simples

## Descrição
Este programa implementa um sistema bancário simples em Python, permitindo que o usuário realize operações de **depósito**, **saque** e **consulta de extrato**. O programa executa em um loop interativo até que o usuário opte por sair.

## Funcionalidades
- **Depósito**: O usuário pode depositar um valor positivo, que será somado ao saldo.
- **Saque**: O usuário pode sacar um valor, respeitando:
  - O saldo disponível na conta.
  - O limite de saque por transação (R$ 500,00).
  - O limite de 3 saques diários.
- **Extrato**: Exibe o histórico de transações e o saldo atual.
- **Sair**: Encerra o programa.

## Variáveis Globais
- `saldo` (*float*): Armazena o saldo disponível na conta.
- `limite` (*float*): Define o limite máximo para cada saque (R$ 500,00).
- `extrato` (*str*): Acumula o histórico de transações realizadas.
- `numero_saques` (*int*): Conta o número de saques realizados.
- `limite_saques` (*int*): Define o limite de saques diários (3 saques).

## Fluxo do Programa
1. O programa exibe um menu com as opções disponíveis.
2. O usuário escolhe uma opção digitando um caractere correspondente.
3. Dependendo da escolha:
   - Se `d`, solicita um valor de depósito e atualiza o saldo e o extrato.
   - Se `s`, solicita um valor de saque e verifica as condições antes de autorizar a transação.
   - Se `e`, exibe o extrato e o saldo.
   - Se `q`, encerra o programa.
   - Se inválido, exibe uma mensagem de erro.

## Validação de Erros
- O programa verifica se:
  - O valor de depósito é positivo.
  - O valor do saque é positivo e dentro do saldo e do limite.
  - O usuário excedeu o número de saques diários.
  - A opção digitada é válida.

## Exemplo de Uso
```bash
    [d] Depositar
    [s] Sacar
    [e] Extrato
    [q] Sair

    => d
Informe o valor do depósito: 200

    [d] Depositar
    [s] Sacar
    [e] Extrato
    [q] Sair

    => e

================ EXTRATO ================
Depósito: R$ 200.00

Saldo: R$ 200.00
=========================================

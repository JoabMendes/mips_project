# Processador MIPS

## Características

- 4 bits de Dados (0-15)
- Capaz de receber um conjunto de instruções (256Bits)
- ULA com 8 Operações:

  - AND
  - OR
  - NAND
  - XOR
  - ADD
  - SUB
  - ATT (Atribuição)
  - SLT

- Apenas Inteiros
- Clear e Clock integrados
- Componentes: ULA + UNIDADE DE CONTROLE + REGISTRADORES (L1|L2)

## Executando o Processador (Exemplo)

Neste exemplo será executado a soma de dois números pelo Processador

A instrunções do processador são de 16Bits onde um conjunto de 16 instruções podem ser elaboradas em conjunto. Um instrução possui a seguinte estrutura:

DEST+OPERATION+R1+R2+INPUT

3B + 3B + 3B + 3B + 4B

Assembly:

```
R1 = 4 #Registrador 1 Recebe valor 4
R2 = 5 #Registrador 2 Recebe valor 5
R3 = R1 + R2 #Registrador 3 Recebe valor da soma entre R1 e R2
```

Instruções em Binário:

```
000 110 000 000 0100
001 110 000 000 0101
010 100 000 001 0000
```

### Passo a passo:

1 - No circuito principal identifique os teclados de entrada

2 - Insira a primeira instrução:

- Selecione 0 para selecionar DEST (L1)
- Selecione -> para escolher a função de atribuição
- Selecione 0 nos dois R1 e R2 (opcional)
- Selecione o número de entrada (4)

3 - Salve a instrução em L2 em 0

4 - Insira a segunda instrução:

- Selecione 1 para selecionar DEST (L1)
- Selecione -> para escolher a função de atribuição
- Selecione 0 nos dois R1 e R2 (opcional)
- Selecione o número de entrada (5)

5 - Insira a terceira instrução:

- Selecione 2 para selecionar DEST (L1)
- Selecione + para escolher a função de soma
- Selecione 000 para definir o primeiro operando em R1
- Selecione 001 para definir o primeiro operando em R2
- Selecione 0 na número de entrada (opcional)

6 - Execute os 2 clock para termiar a operação.

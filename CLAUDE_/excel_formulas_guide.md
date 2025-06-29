# 📊 Guia de Implementação - Fórmulas Excel

## 🎯 Layout Sugerido da Planilha

### Estrutura das Células:

```
A1: "SIMULADOR DE INVESTIMENTOS EM FUNDOS IMOBILIÁRIOS"
A2: [Linha em branco]

A3: "Investimento Mensal (R$):"        | C3: 1000
A4: "Tempo de Investimento (anos):"    | C4: 10
A5: "Taxa de Rendimento Mensal (%):"   | C5: 0.8
A6: "Dividend Yield Mensal (%):"       | C6: 1.0

A8: "RESULTADOS:"
A9: "Patrimônio Acumulado:"            | C9: [Fórmula VF]
A10: "Dividendos Mensais:"             | C10: [Fórmula Dividendos]

A12: "CENÁRIOS DE INVESTIMENTO:"
A13-G18: [Tabela de Cenários]
```

## 🔢 Fórmulas Principais

### 1. Patrimônio Acumulado (Célula C9)
```excel
=VF(C5/100;C4*12;-C3;0;0)
```
**Explicação:**
- `C5/100`: Taxa mensal em decimal
- `C4*12`: Número de meses
- `-C3`: Investimento mensal (negativo pois é saída de caixa)
- `0;0`: Valor presente e tipo (início/fim do período)

### 2. Dividendos Mensais (Célula C10)
```excel
=C9*(C6/100)
```
**Explicação:**
- `C9`: Patrimônio acumulado
- `C6/100`: Dividend yield em decimal

## 📋 Tabela de Cenários

### Cabeçalhos (Linha 13):
```
A13: "Período"
B13: "Total Investido"
C13: "Patrimônio"
D13: "Dividendos/Mês"
E13: "Dividendos/Ano"
F13: "Rentabilidade"
```

### Fórmulas para Cenário de 2 Anos (Linha 14):

```excel
A14: "2 anos"
B14: =$C$3*2*12
C14: =VF($C$5/100;2*12;-$C$3;0;0)
D14: =C14*($C$6/100)
E14: =D14*12
F14: =(C14/B14-1)*100
```

### Fórmulas para Cenário de 5 Anos (Linha 15):

```excel
A15: "5 anos"
B15: =$C$3*5*12
C15: =VF($C$5/100;5*12;-$C$3;0;0)
D15: =C15*($C$6/100)
E15: =D15*12
F15: =(C15/B15-1)*100
```

### Fórmulas para Cenário de 10 Anos (Linha 16):

```excel
A16: "10 anos"
B16: =$C$3*10*12
C16: =VF($C$5/100;10*12;-$C$3;0;0)
D16: =C16*($C$6/100)
E16: =D16*12
F16: =(C16/B16-1)*100
```

### Fórmulas para Cenário de 20 Anos (Linha 17):

```excel
A17: "20 anos"
B17: =$C$3*20*12
C17: =VF($C$5/100;20*12;-$C$3;0;0)
D17: =C17*($C$6/100)
E17: =D17*12
F17: =(C17/B17-1)*100
```

### Fórmulas para Cenário de 30 Anos (Linha 18):

```excel
A18: "30 anos"
B18: =$C$3*30*12
C18: =VF($C$5/100;30*12;-$C$3;0;0)
D18: =C18*($C$6/100)
E18: =D18*12
F18: =(C18/B18-1)*100
```

## 🎨 Formatação

### 1. Formatação de Células Editáveis (C3:C6):
- **Preenchimento**: Verde claro (#E8F5E8)
- **Borda**: Verde escuro (#4CAF50) - 2pt
- **Fonte**: Negrito

### 2. Formatação de Resultados (C9:C10):
- **Preenchimento**: Azul claro (#E3F2FD)
- **Fonte**: Negrito, tamanho 12
- **Formato**: Moeda brasileira

### 3. Formatação da Tabela (A13:F18):
- **Cabeçalho**: Preenchimento verde (#4CAF50), fonte branca, negrito
- **Dados**: Alternância de cores (branco/#F9F9F9)
- **Bordas**: Todas as bordas com linha fina

### 4. Validação de Dados:

#### Para C3 (Investimento Mensal):
```
Permitir: Decimal
Dados: entre 0 e 1000000
```

#### Para C4 (Tempo):
```
Permitir: Número inteiro
Dados: entre 1 e 50
```

#### Para C5 e C6 (Taxas):
```
Permitir: Decimal
Dados: entre 0 e 10
```

## 📊 Criação do Gráfico

### Passos para criar o gráfico:

1. **Selecionar dados**: Coluna A (Períodos) e Coluna C (Patrimônio) da tabela de cenários
2. **Inserir → Gráficos → Linha**
3. **Personalizar**:
   - Título: "Evolução do Patrimônio por Período"
   - Eixo X: "Período de Investimento"
   - Eixo Y: "Patrimônio Acumulado (R$)"
   - Cores: Tema verde

## 🔧 Formatação Condicional

### Para destacar melhor cenário:

1. **Selecionar** a coluna F (Rentabilidade)
2. **Página Inicial → Formatação Condicional → Nova Regra**
3. **Tipo**: "Usar fórmula para determinar quais células formatar"
4. **Fórmula**: `=F14=MAX($F$14:$F$18)`
5. **Formato**: Preenchimento dourado, fonte branca

## 💡 Dicas de Implementação

### 1. Nomes Definidos:
Criar nomes para facilitar as fórmulas:
- `InvestimentoMensal` = $C$3
- `TempoAnos` = $C$4
- `TaxaMensal` = $C$5
- `DividendYield` = $C$6

### 2. Proteção da Planilha:
- Desbloquear apenas células C3:C6
- Proteger a planilha para evitar alterações acidentais

### 3. Comentários nas Células:
Adicionar comentários explicativos nas células principais:
- C9: "Valor calculado pela função VF considerando juros compostos"
- C10: "Renda passiva mensal baseada no dividend yield"

## 🚀 Extensões Avançadas

### 1. Análise de Sensibilidade:
Criar tabela de dupla entrada variando taxa e tempo

### 2. Cenário Pessimista/Otimista:
Adicionar colunas com diferentes premissas de rentabilidade

### 3. Inflação:
Incluir ajuste pela inflação nos cálculos de valor real

### 4. Comparação com Poupança:
Adicionar coluna comparativa com rendimento da poupança
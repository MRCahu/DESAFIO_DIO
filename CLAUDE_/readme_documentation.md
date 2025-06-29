# 📈 Simulador de Investimentos em Fundos Imobiliários (FII)

## 🎯 Sobre o Projeto

Este projeto foi desenvolvido como parte do desafio da **Digital Innovation One (DIO)** para demonstrar habilidades em **Excel avançado** e **análise de investimentos**. O simulador permite calcular projeções de investimentos mensais em Fundos de Investimento Imobiliário (FII), considerando rentabilidade e dividend yield.

## 🚀 Objetivo

Criar uma ferramenta prática e educativa que permita aos usuários:
- Simular investimentos mensais em FIIs
- Visualizar projeções de patrimônio a longo prazo
- Calcular dividendos mensais estimados
- Comparar diferentes cenários de investimento
- Compreender o poder dos juros compostos no mercado imobiliário

## ⚙️ Funcionalidades

### 🎛️ Parâmetros Editáveis
- **Valor do Investimento Mensal**: Valor em reais a ser investido mensalmente
- **Tempo de Investimento**: Período em anos para o investimento
- **Taxa de Rendimento Mensal**: Percentual de valorização mensal dos FIIs
- **Dividend Yield**: Percentual de dividendos mensais sobre o patrimônio

### 📊 Cálculos Automáticos
- **Patrimônio Acumulado**: Calculado usando a função VF (Valor Futuro)
- **Dividendos Mensais**: Baseado no dividend yield aplicado sobre o patrimônio
- **Cenários Múltiplos**: Simulações automáticas para 2, 5, 10, 20 e 30 anos
- **Rentabilidade Total**: Percentual de retorno sobre o valor investido

### 🎨 Recursos Visuais
- Formatação profissional com cores temáticas
- Destaque visual para campos editáveis
- Tabela de cenários organizada e responsiva
- Gráfico de evolução patrimonial (indicação para implementação)

## 🖼️ Capturas de Tela

### Tela Principal do Simulador
![Tela Principal](./screenshots/tela-principal.png)
*Visão geral do simulador com parâmetros de investimento*

### Tabela de Cenários
![Tabela de Cenários](./screenshots/tabela-cenarios.png)
*Comparação entre diferentes períodos de investimento*

### Formatação Excel
![Formatação Excel](./screenshots/formatacao-excel.png)
*Exemplo da formatação aplicada na planilha Excel*

## 📝 Como Usar

### No Excel:
1. **Abra** a planilha `Simulador_FII.xlsx`
2. **Edite** os campos destacados em verde:
   - Investimento mensal (célula C3)
   - Tempo de investimento em anos (célula C4)
   - Taxa de rendimento mensal (célula C5)
   - Dividend yield (célula C6)
3. **Observe** os resultados atualizarem automaticamente
4. **Analise** a tabela de cenários para diferentes períodos
5. **Visualize** o gráfico de evolução patrimonial

### Fórmulas Principais:
```excel
# Patrimônio Acumulado (VF)
=VF(C5/100;C4*12;-C3;0;0)

# Dividendos Mensais
=D8*(C6/100)

# Cenários (exemplo para 10 anos)
=VF($C$5/100;10*12;-$C$3;0;0)
```

## 🛠️ Tecnologias Utilizadas

- **Microsoft Excel**: Ferramenta principal para cálculos e simulações
- **Funções Financeiras**: VF (Valor Futuro), PMT (Pagamento)
- **Formatação Condicional**: Destacar campos editáveis
- **Gráficos Excel**: Visualização da evolução patrimonial
- **Validação de Dados**: Controle de entrada de valores

## 📚 Conceitos Financeiros Aplicados

### Valor Futuro de Anuidade
A fórmula utilizada para calcular o patrimônio acumulado:

```
VF = PMT × [((1 + i)ⁿ - 1) / i]
```

Onde:
- **VF**: Valor Futuro (patrimônio acumulado)
- **PMT**: Pagamento mensal (investimento mensal)
- **i**: Taxa de juros (rendimento mensal)
- **n**: Número de períodos (meses)

### Dividend Yield
Calculado como percentual do patrimônio acumulado:

```
Dividendos = Patrimônio × (Dividend Yield / 100)
```

## 🎓 Aprendizados

Durante o desenvolvimento deste projeto, foram consolidados os seguintes conhecimentos:

- **Funções Financeiras do Excel**: Domínio da função VF e suas aplicações
- **Formatação Avançada**: Criação de interfaces profissionais no Excel
- **Validação de Dados**: Implementação de controles de entrada
- **Mercado de FIIs**: Compreensão dos fundamentos dos Fundos Imobiliários
- **Análise de Cenários**: Técnicas de projeção e comparação
- **Documentação Técnica**: Criação de documentação clara e profissional

## 🎯 Relação com o Desafio DIO

Este projeto atende aos requisitos do desafio da DIO através de:

### ✅ Critérios Técnicos Atendidos:
- **Uso de Funções Avançadas**: Implementação da função VF
- **Formatação Profissional**: Interface visualmente atrativa
- **Cenários Múltiplos**: Análise comparativa de diferentes períodos
- **Automação**: Cálculos automáticos baseados em parâmetros
- **Documentação**: README completo e estruturado

### 🚀 Diferenciais Implementados:
- **Foco em FIIs**: Especialização em um segmento específico
- **Dividend Yield**: Cálculo de renda passiva mensal
- **Interface Intuitiva**: Campos claramente identificados
- **Escalabilidade**: Fácil adaptação para outros investimentos
- **Educativo**: Explicação das fórmulas utilizadas

## 📁 Estrutura do Repositório

```
simulador-fii/
├── 📊 Simulador_FII.xlsx          # Planilha principal
├── 📸 screenshots/                # Capturas de tela
│   ├── tela-principal.png
│   ├── tabela-cenarios.png
│   └── formatacao-excel.png
├── 📋 templates/                  # Templates auxiliares
│   └── template-personalizado.xlsx
├── 📖 docs/                      # Documentação adicional
│   ├── manual-usuario.md
│   └── formulas-financeiras.md
├── 🎨 assets/                    # Recursos visuais
│   └── logo-projeto.png
└── 📄 README.md                  # Este arquivo
```

## 🤝 Como Contribuir

1. **Fork** este repositório
2. **Clone** para sua máquina local
3. **Crie** uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
4. **Commit** suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
5. **Push** para a branch (`git push origin feature/nova-funcionalidade`)
6. **Abra** um Pull Request

## 📧 Contato

- **LinkedIn**: [Seu LinkedIn](https://linkedin.com/in/seu-perfil)
- **GitHub**: [Seu GitHub](https://github.com/seu-usuario)
- **Email**: seu.email@exemplo.com

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

### 🏆 Desenvolvido para o Desafio DIO

**Bootcamp**: [Nome do Bootcamp]  
**Instrutor**: [Nome do Instrutor]  
**Data**: [Data de Conclusão]

---

*"O melhor momento para investir foi há 20 anos. O segundo melhor momento é agora."* 📈
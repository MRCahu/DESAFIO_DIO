# Simulador de Investimentos em Fundos Imobiliários (FIIs)

## Descrição do Projeto

Este projeto apresenta um simulador de investimentos em Fundos de Investimento Imobiliário (FIIs) desenvolvido em uma planilha Excel, acompanhado de uma documentação técnica completa para o GitHub. O objetivo é fornecer uma ferramenta prática e visualmente intuitiva para que investidores possam simular o crescimento de seu patrimônio e a estimativa de dividendos mensais ao longo do tempo, considerando diferentes cenários de investimento.

## Objetivo

O principal objetivo deste projeto é:

*   Oferecer uma ferramenta simples e eficaz para a simulação de investimentos em FIIs.
*   Demonstrar o potencial de acumulação de patrimônio e geração de renda passiva com base em aportes mensais e taxa de rendimento.
*   Servir como um portfólio profissional, evidenciando habilidades em manipulação de dados, automação de planilhas e documentação técnica, conforme os requisitos do desafio da DIO (Digital Innovation One).

## Funcionalidades da Planilha

A planilha `simulador_investimentos_FII.xlsx` possui as seguintes funcionalidades:

*   **Campos Editáveis:**
    *   **Valor do Investimento Mensal (R$):** Permite ao usuário definir o valor que será aportado mensalmente.
    *   **Tempo de Investimento (Anos):** Permite ao usuário especificar o horizonte de tempo do investimento em anos.
    *   **Taxa de Rendimento Mensal (%):** Permite ajustar a taxa de rendimento esperada dos FIIs (ex: 0.8% ao mês).

*   **Cálculos Automáticos:**
    *   **Patrimônio Acumulado (R$):** Calcula automaticamente o valor total do patrimônio ao final do período de investimento, utilizando a função `VF` (Valor Futuro) do Excel, que considera os aportes mensais, a taxa de rendimento e o tempo.
    *   **Dividendos Mensais Estimados (R$):** Estima os dividendos mensais que seriam gerados com base no patrimônio acumulado, considerando uma taxa de 1% ao mês sobre o patrimônio.

*   **Tabela de Cenários:**
    *   Apresenta uma simulação automática para diferentes horizontes de tempo: 2, 5, 10, 20 e 30 anos.
    *   Para cada cenário, são calculados o patrimônio acumulado e os dividendos mensais estimados, permitindo uma análise comparativa rápida do potencial de longo prazo.

*   **Formatação Visual:**
    *   A planilha é formatada com cores, bordas e formatação de moeda para facilitar a leitura e a compreensão.
    *   Os campos editáveis são visualmente destacados para orientar o usuário.

*   **Gráfico de Evolução do Patrimônio (a ser implementado/melhorado):**
    *   Atualmente, a planilha foca nos cálculos e cenários. A inclusão de um gráfico de evolução do patrimônio ao longo do tempo é uma melhoria futura planejada para oferecer uma visualização mais dinâmica.

## Capturas de Tela

(Aqui serão inseridas as capturas de tela da planilha Excel, destacando os campos editáveis, os resultados e a tabela de cenários. Por enquanto, são imagens fictícias.)

*   `./images/captura1.png`
*   `./images/captura2.png`
*   `./images/captura3.png`

## Instruções de Uso

1.  **Download:** Baixe o arquivo `simulador_investimentos_FII.xlsx` deste repositório.
2.  **Abertura:** Abra a planilha em qualquer software compatível com Excel (Microsoft Excel, Google Sheets, LibreOffice Calc, etc.).
3.  **Edição:** Altere os valores nos campos destacados em amarelo:
    *   `Valor do Investimento Mensal (R$)`
    *   `Tempo de Investimento (Anos)`
    *   `Taxa de Rendimento Mensal (%)`
4.  **Análise:** Observe os cálculos automáticos de patrimônio e dividendos, tanto na seção principal quanto na tabela de cenários.

## Tecnologias Utilizadas

*   **Microsoft Excel (ou compatível):** Para a criação e manipulação da planilha de simulação.
*   **Python:** Utilizado para a automação da criação da estrutura inicial da planilha Excel (via biblioteca `openpyxl`).
*   **Markdown:** Para a elaboração desta documentação técnica no GitHub.

## Aprendizados

Durante o desenvolvimento deste projeto, foram aprofundados conhecimentos em:

*   **Funções Financeiras no Excel:** Especialmente a função `VF` (Valor Futuro) para projeções de investimento.
*   **Automação de Planilhas com Python:** Utilização da biblioteca `openpyxl` para gerar e formatar arquivos `.xlsx` programaticamente.
*   **Design de Planilhas:** Melhores práticas para criar interfaces de usuário intuitivas e visualmente agradáveis em planilhas.
*   **Documentação Técnica:** A importância de uma documentação clara e completa para projetos de software, facilitando o entendimento e a replicação.
*   **Controle de Versão (Git/GitHub):** Organização de projetos em repositórios, incluindo a estrutura de arquivos e a documentação.

## Relação com o Desafio da DIO

Este projeto foi desenvolvido como parte do desafio proposto pela Digital Innovation One (DIO), com o objetivo de aplicar conceitos de programação, manipulação de dados e documentação. Ele demonstra a capacidade de criar soluções práticas e bem documentadas, alinhadas com as expectativas de um portfólio profissional na área de tecnologia e finanças. A escolha do tema de investimentos em FIIs reflete um interesse prático e a aplicabilidade das ferramentas aprendidas. 



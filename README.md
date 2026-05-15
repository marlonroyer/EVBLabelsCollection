# EVB LabelsCollection - Gerador de Etiquetas da Coleção do Herbário Evaldo Buttura
 
Sistema web para geração automatizada de etiquetas para o Herbário Evaldo Buttura (EVB). Importa dados de planilhas CSV, permite filtrar por intervalo de IDs e exporta etiquetas formatadas em PDF.

## Funcionalidades

- **Importação de CSV** - Carregue planilhas com dados de famílias, intervalos e códigos
- **Filtro Inteligente** - Filtre etiquetas por intervalo de IDs (digite apenas os números)
- **Pré-visualização** - Visualize as etiquetas antes de gerar o PDF
- **Exportação PDF** - Gere PDF em formato A4 paisagem com 2 etiquetas por linha
- **Ajuste Automático** - Tamanho da fonte se adapta automaticamente ao conteúdo
- **Logo Personalizada** - Inclui logo do EVB com transparência configurável

## Tecnologias Utilizadas

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **Bibliotecas:**
  - [PapaParse](https://www.papaparse.com/) - Parsing de CSV
  - [jsPDF](https://github.com/parallax/jsPDF) - Geração de PDF
  - [html2canvas](https://html2canvas.hertzen.com/) - Captura de HTML para imagem
  - [Font Awesome](https://fontawesome.com/) - Ícones

## Pré-requisitos

- Navegador web moderno (Chrome, Firefox, Edge)
- Arquivo CSV com as seguintes colunas:
  - `ID` - Identificador único (ex: CX-001)
  - `Família` - Nome(s) da(s) família(s)
  - `Intervalos` - Intervalo(s) de coleta
  - `Código` - Código de localização (Armário, Prateleira, Espaço)
- Arquivo de logo: `LogoEVB.png` (na mesma pasta do projeto)

Como Usar
1. Carregar Planilha CSV
Arraste e solte o arquivo CSV na área de upload

Ou clique em "Selecionar Arquivo" para buscar no computador

2. Filtrar Etiquetas
Digite o ID Inicial (apenas os dígitos, ex: 001 ou 1)

Digite o ID Final (apenas os dígitos, ex: 024 ou 24)

Clique em Filtrar Etiquetas

3. Visualizar e Gerar PDF
As etiquetas aparecerão na área de pré-visualização

Verifique se estão corretas

Clique em Gerar PDF para baixar o arquivo

Formato do CSV
O arquivo CSV deve seguir este formato:

csv
ID,Família,Intervalos,Código
CX-001,Myrtaceae,"100-200m, Brasil",A1-P2-E3
CX-002,Fabaceae,"300-500m, Argentina",A1-P2-E4
CX-003,Solanaceae,"0-100m, Paraguai",A2-P1-E1
Colunas Obrigatórias:
Coluna	Descrição	Exemplo
ID	Identificador único	CX-001
Família	Nome da família botânica	Myrtaceae
Intervalos	Intervalos de coleta	100-200m, Brasil
Código	Localização física	A1-P2-E3
Nota: O código de localização (Armário, Prateleira, Espaço) NÃO é exibido nas etiquetas, apenas o ID é mostrado.

Design da Etiqueta
Cada etiqueta possui:

Dimensões: 14cm × 10cm (paisagem)

Coluna Esquerda (35%): ID e lista de Famílias

Coluna Direita (65%): ID (oculto) e lista de Intervalos

Logo: Canto inferior direito com opacidade 50%

Fundo cinza unificado: Barra contínua nos títulos "FAMÍLIA(S)" e "INTERVALO(S)"

Estrutura do Projeto
├── index.html          # Interface principal
├── styles.css          # Estilos da aplicação
├── script.js           # Lógica de funcionamento
├── LogoEVB.png         # Logo do herbário
└── README.md           # Documentação

Funcionalidades Detalhadas
Ajuste Automático de Fonte
O sistema testa tamanhos de fonte (15px → 8px) para garantir que o conteúdo caiba na etiqueta sem transbordar.

Filtro por ID Simplificado
Digite 1 → interpreta como CX-001

Digite 01 → interpreta como CX-001

Digite 001 → interpreta como CX-001

Digite CX-001 → mantém como está

Geração de PDF
Formato: A4 paisagem (297mm × 210mm)

Layout: 2 etiquetas por linha

Margens: 5mm

Alta qualidade (escala 2x no html2canvas)

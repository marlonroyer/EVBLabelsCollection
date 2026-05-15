# EVB LabelsCollection - Gerador de Etiquetas para a Coleção do Herbário

![Version](https://img.shields.io/badge/version-1.0.0-gold)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-production-brightgreen)

Sistema para geração de etiquetas de herbário a partir de arquivos CSV. Desenvolvido para uso interno do **Herbário Evaldo Buttura (EVB)**.

## Funcionalidades

- **Upload de CSV** - Carregue planilhas com dados taxonômicos e de coleta
- **Filtro Inteligente** - Filtre etiquetas por intervalo de IDs usando apenas números
- **Pré-visualização em Tempo Real** - Visualize as etiquetas exatamente como serão impressas
- **Geração de PDF** - Exporte etiquetas em formato A4 paisagem (2 por linha)
- **Layout Profissional** - Etiquetas padronizadas de 14cm × 10cm
- **Ajuste Automático de Fonte** - O texto se adapta ao espaço disponível
- **Logo Personalizada** - Suporte a marca d'água com transparência
- **Interface Moderna** - Design glassmorphism com paleta de cores profissional

## Tecnologias Utilizadas

- [PapaParse 5.3.0](https://www.papaparse.com/) - Parsing de arquivos CSV
- [jsPDF 2.5.1](https://github.com/parallax/jsPDF) - Geração de documentos PDF
- [html2canvas 1.4.1](https://html2canvas.hertzen.com/) - Captura de elementos HTML
- [Font Awesome 6.4.0](https://fontawesome.com/) - Ícones da interface

## Como Usar
- **Carregue o CSV**
Arraste e solte o arquivo CSV na área de upload
Ou clique em "Selecionar Arquivo"

- **Configure o Filtro**
Digite o ID inicial (apenas números, ex: 001)
Digite o ID final (apenas números, ex: 024)

- **Clique em "Filtrar Etiquetas"**

- **Visualize as Etiquetas**
As etiquetas aparecerão na área de pré-visualização
Cada etiqueta mostra: ID, Família(s) e Intervalo(s)

- **Gere o PDF**
Clique em "Gerar PDF" para baixar todas as etiquetas
Formato A4 paisagem com 2 etiquetas por linha
Design da Etiqueta
Cada etiqueta possui:

- **Dimensões: 14cm × 10cm**
- **Cabeçalho: ID da caixa (ex: CX-001)**
- **Coluna Esquerda (35%): Famílias (negrito, alinhado à direita)**
- **Coluna Direita (65%): Intervalos (itálico, alinhado à esquerda)**
- **Logo: Imagem com 50% de opacidade no canto inferior direito**
- **Títulos: Barra cinza unificada para FAMÍLIA(S) e INTERVALO(S)**

## Estrutura do Projeto
evb-labels/
├── index.html          # Página principal
├── styles.css          # Estilos da aplicação
├── script.js           # Lógica do gerador
├── LogoEVB.png         # Logo do herbário
└── README.md           # Documentação

## Licença
- **Este projeto está sob a licença MIT.**

## Autor
- **Marlon Royer de Morais - Herbário Evaldo Buttura (EVB)**
- **EVB LabelsCollection -2026 - Desenvolvido para uso interno**

# Documentação de Requisitos - Aplicativo de Gestão para o "Mercado do Frota"

## Sumário
1. [Visão Geral do Projeto](#visão-geral-do-projeto)
2. [Objetivos do Projeto](#objetivos-do-projeto)
3. [Funcionalidades Principais](#funcionalidades-principais)
4. [Requisitos Funcionais e Não Funcionais](#requisitos-funcionais-e-não-funcionais)
5. [Fluxo do Usuário](#fluxo-do-usuário)
6. [Protótipos e Interface do Usuário (UI)](#protótipos-e-interface-do-usuário-ui)
7. [Estrutura de Diretórios e Organização do Projeto](#estrutura-de-diretórios-e-organização-do-projeto)

---

### Visão Geral do Projeto
O aplicativo "Mercado do Frota" é uma solução mobile para Android, projetada para auxiliar os proprietários na gestão eficiente do mercadinho, com controle de estoque, registro de vendas, acompanhamento de valores a receber, e outras funcionalidades específicas para as necessidades do estabelecimento. Este documento descreve os requisitos para o desenvolvimento do protótipo e das funcionalidades futuras.

---

### Objetivos do Projeto
- **Desenvolver um protótipo** que represente as funcionalidades essenciais do aplicativo até 18 de novembro de 2024.
- **Simplificar e otimizar** o processo de registro de vendas, controle de estoque e gestão de valores a receber, digitalizando registros que anteriormente eram feitos de forma manual.
- **Promover interatividade com os clientes**, permitindo sugestões de produtos e envio de mensagens de interesse diretamente aos proprietários.
- **Automatizar a gestão** de processos internos, aumentando a eficiência e reduzindo o risco de erros.

---

### Funcionalidades Principais
1. **Controle de Estoque**
   - Cadastro de produtos com informações detalhadas (nome, quantidade, preço de custo e venda, validade).
   - Alerta de baixo estoque com mensagens para os proprietários.
   - Histórico de movimentações de estoque.

2. **Registro de Vendas**
   - Sistema de registro rápido de vendas por produto.
   - Relatório diário, semanal e mensal de vendas.

3. **Gestão de Valores a Receber (Fiado)**
   - Cadastro de clientes com controle de valores pendentes.
   - Registro de pagamentos parciais ou totais.

4. **Lista de Desejos dos Clientes**
   - Campo para sugestões de produtos pelos clientes.
   - Notificação para os proprietários quando uma sugestão é adicionada.

5. **Painel de Gestão e Relatórios**
   - Dashboard para visualização de métricas de vendas e estoque.
   - Relatórios exportáveis para planilhas.

---

### Requisitos Funcionais e Não Funcionais

#### Requisitos Funcionais
- **RF01**: Permitir o cadastro e atualização de produtos no estoque.
- **RF02**: Registrar vendas de produtos com ajuste automático no estoque.
- **RF03**: Implementar um sistema de alerta para produtos com estoque baixo.
- **RF04**: Controlar e exibir valores a receber de clientes, com histórico de pagamentos.
- **RF05**: Criar uma interface para clientes sugerirem produtos diretamente.
- **RF06**: Exibir um painel de controle com indicadores de vendas e estoque.

#### Requisitos Não Funcionais
- **RNF01**: Interface amigável e intuitiva, com atenção à usabilidade e acessibilidade.
- **RNF02**: Respeitar as diretrizes de design para Android.
- **RNF03**: Garantir a segurança dos dados dos clientes e dos registros financeiros.
- **RNF04**: O aplicativo deve ser compatível com versões do Android a partir da 8.0 (Oreo).
- **RNF05**: Armazenamento local com opção de backup em nuvem.

---

### Fluxo do Usuário

#### 1. **Proprietário**
   - Acessa o app e visualiza um painel de métricas.
   - Navega até o controle de estoque para registrar novos produtos ou ajustar quantidades.
   - Visualiza alertas de baixo estoque e registros de vendas.
   - Acessa a seção de fiado para verificar valores pendentes e registrar novos pagamentos.
   - Consulta a lista de sugestões de produtos enviadas pelos clientes.

#### 2. **Cliente (via acesso direto em loja)**
   - Sugere produtos pela lista de desejos.
   - Consulta produtos em estoque (opcional e configurável pelos proprietários).

---

### Protótipos e Interface do Usuário (UI)
Os protótipos foram desenvolvidos usando **Canvas** e, adicionalmente, **Figma** para expandir as possibilidades de layout e recursos de navegação.

Para acessar os protótipos:
- Link para o protótipo de navegação: [Protótipo Interativo](https://www.figma.com/design/Bnrti7QwX1siH4k6fPwe1Z/Prot%C3%B3tipo---Mercado-do-Frota?node-id=99-3&t=7aqwldIi8kMsrS2G-1)
- Link para o layout detalhado: [Protótipo UI](#)

**Capturas de Tela**:
- **Tela Inicial**: Acesso rápido ao painel de métricas e navegação simplificada.
- **Controle de Estoque**: Tela para cadastro e visualização de produtos e estoque.
- **Gestão de Fiado**: Interface para gerenciar clientes e valores pendentes.
- **Lista de Desejos**: Tela dedicada para sugestões dos clientes.

*(Imagens podem ser adicionadas em uma pasta chamada `/assets/screenshots`)*

---

### Estrutura de Diretórios e Organização do Projeto

O projeto segue uma organização modular, com pastas e arquivos estruturados conforme a arquitetura MVC (Model-View-Controller) para maior manutenibilidade e clareza.

```plaintext
📦 MercadoFrotaApp
 ┣ 📂 assets
 ┃ ┣ 📂 screenshots
 ┃ ┗ 📂 icons
 ┣ 📂 app
 ┃ ┣ 📂 src
 ┃ ┃ ┣ 📂 main
 ┃ ┃ ┃ ┣ 📂 java/com/mercadofrota/
 ┃ ┃ ┃ ┃ ┣ 📂 model         # Modelos e classes de dados
 ┃ ┃ ┃ ┃ ┣ 📂 controller    # Controladores para lógica de negócios
 ┃ ┃ ┃ ┃ ┗ 📂 view          # Classes e layouts de UI
 ┃ ┃ ┃ ┗ 📂 res
 ┃ ┃ ┃ ┃ ┣ 📂 layout        # Layouts XML para cada tela
 ┃ ┃ ┃ ┃ ┣ 📂 values        # Strings, cores, dimensões etc.
 ┃ ┃ ┗ 📂 test
 ┃ ┃ ┃ ┗ 📂 java/com/mercadofrota
 ┗ README.md

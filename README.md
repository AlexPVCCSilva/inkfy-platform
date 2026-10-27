# 🎨 Inkfy — Marketplace de Tatuagem & Micro-SaaS de Gestão para Estúdios

> Plataforma Web (*Desktop-First SPA*) que conecta clientes a tatuadores por estilo e geolocalização, integrando orçamentos personalizados via chat, trava financeira *anti-no-show* (pagamento de sinal) e gestão contábil de bancada (DRE).

---

## 📌 1. Descrição do Projeto

O **Inkfy** é uma plataforma híbrida que une um **Marketplace B2C** (voltado a clientes que buscam o artista ideal para sua tatuagem autoral) a uma ferramenta **Micro-SaaS B2B** (voltada a tatuadores autônomos e estúdios). 

Diferente de catálogos estáticos, o sistema digitaliza toda a jornada de contratação de uma tatuagem sob medida: desde a descoberta visual do portfólio (incluindo filtro de trabalhos já cicatrizados) e busca geolocalizada em mapa, até o envio estruturado do *briefing*, aprovação de proposta financeira no chat, pagamento automatizado do sinal de reserva e apuração do lucro líquido real do profissional.

---

## ⚠️ 2. Problema Abordado

O mercado de tatuagem enfrenta três gargalos operacionais críticos que geram perda de tempo e prejuízo financeiro:

1. **Triagem manual e orçamentos despadronizados (WhatsApp/Instagram):** Tatuadores gastam horas diárias respondendo mensagens incompletas onde o cliente não informa local do corpo, tamanho em centímetros ou referências visuais.
2. **Prejuízo com desistências de última hora (*No-Show*):** Clientes que desmarcam em cima da hora ou simplesmente não comparecem deixam a cadeira do estúdio ociosa por horas e geram perda de materiais descartáveis e tempo de criação do desenho.
3. **Descontrole financeiro de bancada:** Grande parte dos tatuadores confunde o valor bruto recebido na sessão com lucro líquido, deixando de contabilizar o custo recorrente de insumos (cartuchos, agulhas, tintas, luvas, barreiras de proteção e taxa de estúdio).

---

## 🎯 3. Objetivos do Projeto

### Objetivo Geral
Desenvolver uma aplicação web centralizada capaz de otimizar a descoberta e contratação de tatuadores por meio de *briefings* estruturados, garantindo segurança financeira contra faltas (*no-show*) e controle contábil simplificado para o artista.

### Objetivos Específicos
* Proporcionar uma experiência de descoberta visual em **Modo Swipe** e busca espacial por raio em quilômetros via **Mapa Interativo**;
* Padronizar o processo de orçamento dentro de um **Chat integrado**, permitindo o envio de propostas formais com cálculo flexível de sinal (**Percentual** ou **Valor Fixo** em reais);
* Automatizar a reserva de agenda mediante confirmação de pagamento do sinal (Pix/Cartão) e aplicar regras transparentes de prazo limite para reembolso (ex.: 48h de antecedência);
* Oferecer um **Dashboard Financeiro (DRE de Bancada)** para controle de receitas de sessões versus despesas operacionais de materiais;
* Permitir a criação de **Eventos Relâmpago** para preenchimento rápido de vagas ociosas na agenda com descontos promocionais.

---

## 🛠️ 4. Arquitetura e Principais Tecnologias Previstas

O projeto adota uma **Arquitetura Cliente-Servidor em 3 Camadas**, comunicando uma *Single Page Application* (SPA) a uma API RESTful orientada a objetos e um banco de dados relacional:

| Camada | Tecnologia | Finalidade no Projeto |
| :--- | :--- | :--- |
| **Frontend Web (SPA)** | **Angular + TypeScript + CSS Grid** | Construção das 7 telas responsivas (*Dark Mode* `#15202B`), gerenciamento de estado, *HTTP Interceptors* e proteção de rotas por perfil (*Route Guards*). |
| **Backend (API REST)** | **C# (.NET 8 / ASP.NET Core Web API)** | Implementação das 12 classes de domínio orientadas a objetos, autenticação JWT, regras de cálculo de sinal, política *anti-no-show* e apuração contábil. |
| **ORM e Consultas** | **Entity Framework Core + LINQ** | Mapeamento objeto-relacional seguro e consultas tipadas para filtros de estilos e consolidação de receitas/despesas. |
| **Banco de Dados** | **MySQL 8.0 + MySQL Workbench** | Persistência relacional com suporte a transações ACID nas 12 tabelas normalizadas do esquema `inkfy_db`. |
| **Geolocalização** | **Google Maps API** | Renderização de estúdios no mapa interativo e cálculo de proximidade por latitude e longitude. |
| **Pagamentos** | **API Gateway (Mercado Pago / Asaas)** | Processamento de cobranças de sinal via Pix (QR Code dinâmico) e confirmação automática via *Webhook*. |
| **Armazenamento Cloud** | **Cloudinary / AWS S3** | Hospedagem otimizada para fotos de portfólio de alta resolução e imagens de referência do chat. |
| **Engenharia & Design** | **Figma, Google Stitch e Astah UML** | Prototipação de alta fidelidade (UI/UX) e modelagem do Diagrama de Classes UML. |

---

## 👥 5. Integrantes da Equipe

| Nome Completo | Papel no Projeto | GitHub |
| :--- | :--- | :--- |
| **Alex Silva** | Desenvolvedor  | [@AlexPVCCSilva](https://github.com/AlexPVCCSilva) |
| **Bernardo Medeiros** | [@Bermedmen](https://github.com/bermedmen) |

---
*Projeto acadêmico desenvolvido no curso de Bacharelado em Sistemas de Informação.*

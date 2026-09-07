
# Kredita

## Descrição do Desafio
Conceder crédito para populações historicamente recusadas por grandes instituições financeiras exige ir além da visão tradicional de risco: **exige identificar onde residem o consumo reprimido e a capacidade real de pagamento sustentável.**
Neste projeto, nosso objetivo é explorar e transformar dados econômicos públicos do **Banco Central do Brasil (BCB)** em inteligência territorial para apoiar decisões de crédito mais inclusivas e responsáveis.

---

# Product Backlog

| ID | Sprint | Prioridade | User Story | Critérios de Aceite (Definição de Pronto) | Estimativa |
|:---|:---:|:---:|:---|:---|:---:|
| **US01** | 1 | Alta | **Como analista de crédito**, gostaria de coletar dados do BCB (inadimplência, ticket, etc.) e integrar bases da SPA, IBGE e Data Senado (Bets), para que a análise reflita o real comprometimento financeiro da região. | - Acesso direto via Colab[cite: 2].<br>- Quebra de faixas de atraso (curta e longa).<br>- Integração de fontes sobre apostas (Bets). | |
| **US02** | 1 | Alta | **Como analista de dados**, gostaria que os indicadores estivessem padronizados e limpos, diferenciando dívida saudável de crítica, para garantir a confiabilidade dos cálculos do Score. | - Limpar dados nulos e valores absurdos (infinitos).<br>- Converter valores monetários de vírgula para ponto.<br>- Classificar dívida imobiliária (saudável) vs. consumo/Bets (crítica). | |
| **US03** | 1 | Alta | **Como tomador de decisões**, gostaria de obter um Score de Oportunidade que valorize a "inadimplência de recuperação rápida" (< 20 dias) e penalize o endividamento crítico, para identificar a real capacidade de pagamento sustentável. | - Fórmula no Colab.<br>- Considerar Fatores: Potencial de Mercado, Dinâmica, Risco Relativo e Saturação de Grandes Bancos.<br>- Identificar histórico de baixa conversão para inadimplência longa (>90 dias). | |
| **US04** | 1 | Alta | **Como usuário final**, desejo visualizar os dados reais processados por meio de gráficos, para facilitar a análise e a compreensão rápida das informações. | - Pelo menos um gráfico gerado plotando dados reais dentro do notebook do Colab. | |
| **US05** | 1 | Alta | **Como usuário**, desejo acessar a estrutura inicial do site web, mesmo sem os dados reais conectados, para visualizar a futura organização do sistema. | - Esqueleto (Site inicial) criado em HTML5/CSS3[cite: 2].<br>- Código salvo e versionado no GitHub[cite: 2]. | |
| **US06** | 2 | Alta | **Como desenvolvedor**, desejo que o site consuma os dados limpos através de uma API (1º DSM) em Flask[cite: 2], para automatizar a visualização dos dados reais na web. | - API REST em Flask conectada e retornando os dados do projeto no backend[cite: 2]. | |
| **US07** | 2 | Alta | **Como analista de crédito**, gostaria de visualizar um mapa interativo de potencial de mercado e uma tabela de ranking regional, para focar investimentos nas melhores áreas[cite: 1]. | - Mapa integrado à interface web exibindo o Score.<br>- Tabela classificatória (Ranking) baseada no Score. | |
| **US08** | 2 | Média | **Como analista**, quero poder filtrar os indicadores por cenários e granularidade (Macro/Micro), para analisar dados de forma mais específica e granular[cite: 1]. | - Filtros funcionais aplicados no mapa e na tabela do sistema web. | |
| **US09** | 3 | Média | **Como estrategista**, quero comparar detalhadamente duas regiões lado a lado, para decidir com maior precisão qual mercado focar[cite: 1]. | - Tela de comparação regional com gráficos paralelos implementada. | |
| **US10** | 3 | Baixa | **Como gestor**, desejo exportar os dados do sistema em formatos variados (PDF, CSV, XLSX, XML), para facilitar apresentações e uso offline[cite: 1]. | - Botão de exportação/download na interface gerando os arquivos de maneira válida. | |
| **US11** | 3 | Baixa | **Como usuário do sistema**, desejo que o acesso seja restrito por Autenticação (Login) nas áreas sensíveis, para manter a segurança das análises estratégicas[cite: 1]. | - Tela de Login funcional.<br>- Bloqueio e permissões de rotas privadas aplicados. | |
| **US12** | 3 | Baixa | **Como cliente**, desejo acessar o website institucional, a metodologia e manuais do sistema, para compreender facilmente a origem do Score e como usar a ferramenta[cite: 1]. | - Página pública de documentação, manuais de uso e explicação metodológica online. |

> **Nota para a Equipe Scrum:** A coluna de **Estimativa** foi deixada intencionalmente vazia. Como o refinamento adicionou tarefas mais complexas (como a junção dos dados do IBGE, SPA e do Senado na US01), este campo deve ser preenchido colaborativamente pela *Equipe de Desenvolvimento* durante a cerimônia de *Sprint Planning*[cite: 4, 9]. Para isso, recomenda-se a utilização de técnicas como o *Planning Poker* ou *Story Points*, baseando-se no esforço e tempo necessários para transformar cada item em um incremento do produto funcional[cite: 3, 4].

---



## Sprints e Entregas

| Período da Sprint | Documentação da Sprint | Vídeo do Incremento (YouTube) |
| --- | --- | --- |
| DD/MM/AAAA - DD/MM/AAAA | [Documentação Sprint 1](https://www.google.com/search?q=link-para-doc) | [Assistir no YouTube](https://www.google.com/search?q=link-para-video) |
| DD/MM/AAAA - DD/MM/AAAA | [Documentação Sprint 2](https://www.google.com/search?q=link-para-doc) | [Assistir no YouTube](https://www.google.com/search?q=link-para-video) |
| DD/MM/AAAA - DD/MM/AAAA | [Documentação Sprint 3](https://www.google.com/search?q=link-para-doc) | [Assistir no YouTube](https://www.google.com/search?q=link-para-video) |

---

## Tecnologias Utilizadas

* **Linguagens:** [Ex: Python, JavaScript, TypeScript]
* **Frameworks:** [Ex: React, Node.js, FastAPI]
* **Banco de Dados:** [Ex: PostgreSQL, MongoDB]
* **Ferramentas e DevOps:** [Ex: Git, Docker, Figma, GitHub Actions]

---

## Estrutura do Projeto

```text
nome-do-projeto/
├── .github/workflows/       # Configuração de CI/CD
├── docs/                    # Pasta de documentação detalhada
├── src/                     # Código-fonte da aplicação
│   ├── controllers/
│   ├── models/
│   └── views/
├── .gitignore
├── package.json (ou requirements.txt)
└── README.md

```

---

## Como Executar, Usar e Testar o Projeto

### Pré-requisitos

* [Ex: Node.js instalado na versão 18+]
* [Ex: Git instalado]

### Instalação e Execução

```bash
# Clone este repositório
git clone [https://github.com/seu-usuario/nome-do-projeto.git](https://github.com/seu-usuario/nome-do-projeto.git)

# Acesse a pasta do projeto
cd nome-do-projeto

# Instale as dependências
npm install

# Execute o projeto
npm run dev

```

### Executando Testes

```bash
npm test

```

---

## Pasta de Documentação

Acesse a [Pasta de Documentação](https://www.google.com/search?q=./docs) para verificar artefatos adicionais, diagramas de arquitetura e modelos de dados.

---

## Critérios de Prontidão (DoR) e Conclusão (DoD)

### Definição de Pronto (Definition of Ready - DoR) Geral

* A história de usuário está escrita e compreendida pela equipe.
* Os critérios de aceite estão definidos.
* As dependências técnicas foram mapeadas e resolvidas.
* A pontuação (estimativa) foi realizada pelo time.

### Definição de Concluído (Definition of Done - DoD) Geral

* Código revisado por pelo menos um membro da equipe (Pull Request aprovado).
* Testes unitários/integração implementados e passando com sucesso.
* Sem erros críticos de linting ou build.
* Documentação atualizada.

### DoR e DoD por Sprint

* **Sprint 1:**
* *DoR:* Histórias iniciais validadas pelo PO.
* *DoD:* MVP funcional rodando em ambiente de desenvolvimento.


* **Sprint 2:**
* *DoR:* Contratos de API e protótipos de tela aprovados.
* *DoD:* Testes de integração automatizados e funcionalidades integradas.


* **Sprint 3:**
* *DoR:* Casos de teste de aceitação definidos.
* *DoD:* Sistema estabilizado, revisado e pronto para homologação.



---

## Estratégia de Branch

* `main`: Versão estável, testada e pronta para produção.
* `develop`: Branch de integração para o desenvolvimento contínuo e união das features.
* `feature/nome-da-feature`: Branches criadas a partir da `develop` para o desenvolvimento de novas funcionalidades.
* `fix/nome-do-bug`: Branches criadas para a correção de bugs pontuais.

---

## Manual de Usuário

[Descreva aqui o passo a passo de como o usuário final deve navegar, fazer login, interagir com a interface e utilizar as principais funcionalidades do sistema para atingir seus objetivos.]

---

## Manual de Instalação

[Descreva aqui o passo a passo detalhado para administradores ou equipe técnica realizarem o deploy, configurar variáveis de ambiente e subir a aplicação em servidores de homologação ou produção.]

---

## Equipe

| Nome Completo | Papel | GitHub | LinkedIn |
| --- | --- | --- | --- |
| Karam Diniz Coutinho |  Product Owner | https://github.com/karam-diniz | www.linkedin.com/in/karam-diniz |
| Davi Ribeiro André  | Scrum Master | [](https://www.google.com/search?q=link-github) | [](https://www.google.com/search?q=link-linkedin) |
| Gabriel Herzer Gaspary | Scrum Team | https://github.com/GabrielHerzer | https://www.linkedin.com/in/gabriel-herzer-133220352/ |
| Gabriel Tase Telmo |  Scrum Team | [](https://www.google.com/search?q=link-github) | [](https://www.google.com/search?q=link-linkedin) |
| Igor Makoto Hoshino |  Scrum Team  | [](https://www.google.com/search?q=link-github) | [](https://www.google.com/search?q=link-linkedin) |
| Isadora de Sousa Fanti |  Scrum Team  | https://github.com/zzadoraa | https://www.linkedin.com/in/isadora-fanti-543262286/ |
| Júlio Ferreira Siqueira dos Santos |  Scrum Team  | [](https://www.google.com/search?q=link-github) | [](https://www.google.com/search?q=link-linkedin) |
| Pedro Aurélio Freitas Lemos dos Santos Lira |  Scrum Team  | [](https://www.google.com/search?q=link-github) | [](https://www.google.com/search?q=link-linkedin) |

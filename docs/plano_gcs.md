# Plano de Gestão de Configuração (GCS)

## 1. Objetivo
Definir as práticas e regras de versionamento, integração e entrega contínua para o repositório do projeto, garantindo a qualidade do código e a estabilidade dos ambientes.

## 2. Estratégia de Versionamento
* **Modelo:** Trunk-Based Development.
* A branch principal (`main`) reflete o código de produção e deve estar sempre estável.

## 3. Regras de Proteção e Revisão
* É expressamente proibido fazer *push* direto para a branch `main`.
* Todas as alterações de código devem ser integradas através de *Pull Requests* (PRs).
* É obrigatória a revisão por pares (no mínimo 1 revisor com acesso de escrita) antes de realizar o *merge* para a `main`.

## 4. Gestão de Ambientes (Environments)
O fluxo de CI/CD passará pelos seguintes ambientes:
* **Staging:** Ambiente de testes para validação técnica e homologação das alterações.
* **Production:** Ambiente final destinado aos utilizadores. O *deployment* para este ambiente tem um bloqueio de segurança e exige a aprovação manual obrigatória de um revisor.

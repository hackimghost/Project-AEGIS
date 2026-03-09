# 🛡️ PROJECT AEGIS: Autonomous Equality & Guard Intelligence System

**Status:** Em Desenvolvimento Ativo (Fase de Arquitetura Cognitiva)
**Foco Operacional:** Prevenção à Violência Física, OSINT contra Extremismo de Gênero e Defesa Civil.
**Lançamento Conceitual:** 08 de Março — Dia Internacional da Mulher.

O **Projeto AEGIS** é um framework de inteligência artificial de código aberto e neutro, projetado para atuar na interseção entre a proteção física e o combate à desinformação comportamental. Nascido da necessidade de conter o avanço da violência (com foco principal no combate ao feminicídio) e a crescente polarização de gênero na internet, o AEGIS utiliza motores de grafos e visão computacional de borda (*Edge Computing*) para mapear, prevenir e alertar sobre cenários de risco.

---

## ⚖️ O Manifesto AEGIS: Neutralidade e Proteção

> "A tecnologia não deve ter viés, gênero ou inclinação política; ela deve ter como único norte a preservação da integridade humana e a busca pela verdade dos fatos. O AEGIS nasce para combater o extremismo, venha ele de grupos que incitam a violência e a segregação contra mulheres, ou de redes que orquestram a destruição de reputações através de acusações falsas. Nosso objetivo não é policiar o pensamento, mas desarmar a engrenagem do ódio e oferecer um escudo tecnológico para quem está em risco iminente."

---

## 🏗️ Arquitetura do Escudo (Módulos Principais)

O AEGIS é dividido em dois motores operacionais que não se cruzam, garantindo a privacidade e a conformidade com as leis de proteção de dados e garantias constitucionais:

### 1. Motor Cognitivo OSINT & Grafos (Threat Intelligence)
Operando em servidores em nuvem, este módulo atua como um rastreador passivo de informações públicas (OSINT):
* **Mapeamento Neural (Neo4j):** Varre a internet pública e deep web buscando fóruns, grupos e perfis que disseminam táticas de agressão, segregação de gênero ou campanhas de difamação coordenada.
* **Análise de Dados Públicos:** Cruza informações de bases públicas legais para identificar reincidência em padrões de violência, gerando Relatórios de Inteligência Estratégica para autoridades e pesquisadores, sem expor dados civis em listas públicas.
* **Detector de Viés e Extremismo:** Algoritmos de Processamento de Linguagem Natural (NLP) treinados para identificar tanto a misoginia estrutural quanto a misandria tática, mantendo a neutralidade do sistema.

### 2. Sentinela de Borda (Visão Computacional Privada)
Um módulo de processamento local (sem envio de imagens para a nuvem) que transforma câmeras de smartphones em escudos ativos — **exclusivamente mediante consentimento explícito da usuária:**
* **Detecção de Anomalias Físicas:** Utiliza IA de reconhecimento de pose e cinemática para identificar padrões corporais de agressão (ex: estrangulamento, quedas forçadas, golpes).
* **Protocolo de Intervenção Rápida:** Ao detectar violência física, o sistema ativa um protocolo de contingência: bloqueio temporário de tela com contagem regressiva, envio de localização em tempo real para contatos de confiança e interface de acionamento imediato de autoridades (ex: 190).
* **Privacidade por Design:** O processamento ocorre exclusivamente no hardware do próprio usuário. Nenhuma imagem, vídeo ou dado sensorial é transmitido para servidores externos.

---

## 🔐 Política de Privacidade & Conformidade LGPD

> Esta seção é parte integral do projeto e não um anexo opcional. A privacidade do usuário é tratada como requisito arquitetural, não como funcionalidade adicional.

### Princípios Fundamentais (Privacy by Design)

O AEGIS é construído sobre os seis pilares do Privacy by Design, conforme exigido pela **Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018):**

| Princípio | Implementação no AEGIS |
|---|---|
| **Proativo, não reativo** | Privacidade embutida na arquitetura desde o dia 0 |
| **Privacidade como padrão** | Sem coleta de dados sem ação explícita da usuária |
| **Incorporada ao design** | Destruição automática de dados é infraestrutura, não política |
| **Funcionalidade total** | Proteção máxima sem comprometer a eficácia do sistema |
| **Segurança ponta a ponta** | Criptografia end-to-end em todos os dados em trânsito |
| **Visibilidade e transparência** | Status de dados exibido em tempo real na interface |

---

### 📋 Base Legal para Tratamento de Dados (LGPD Art. 7º)

O AEGIS opera exclusivamente sob a base legal do **consentimento livre, informado, inequívoco e revogável** (LGPD Art. 7º, Inciso I).

**O que isso significa na prática:**

- ✅ Nenhum sensor, câmera ou dado é acessado antes da autorização explícita da usuária
- ✅ O consentimento é concedido por ação positiva e intencional (não por omissão ou pré-marcação)
- ✅ A revogação do consentimento pode ser feita a qualquer momento, com efeito imediato
- ✅ A revogação aciona automaticamente a destruição imediata de todos os dados coletados
- ✅ Nenhuma funcionalidade é condicionada à manutenção do consentimento

---

### 📦 Quais Dados São Coletados e Por Quê

| Dado | Finalidade | Armazenamento | Tempo de Retenção |
|---|---|---|---|
| Feed de câmera (frames) | Detecção de anomalias físicas | **Local — no dispositivo** | Processado e descartado em tempo real |
| Dados de sensores (acelerômetro, giroscópio) | Identificação de padrões de movimento | **Local — no dispositivo** | Processado e descartado em tempo real |
| Localização GPS | Envio a contatos de confiança em emergência | Temporário — apenas durante evento | **Destruído em 48h (salvo Exceção Forense)** |
| Logs de eventos de alerta | Auditoria de acionamentos para melhoria do sistema | Servidor — criptografado e anonimizado | **Destruído em 48h (salvo Exceção Forense)** |
| Contatos de confiança | Acionamento da rede de proteção | **Local — no dispositivo** | Permanece até revogação pela usuária |

> ⚠️ **O AEGIS não coleta:** nome completo, CPF, dados bancários, histórico de navegação, conteúdo de mensagens, fotos pessoais ou qualquer dado não listado acima.

---

### ⏱️ Protocolo de Destruição Automática vs. Cofre Forense

A destruição de dados não é um processo manual — é arquitetural e auditável. Para garantir o cumprimento da LGPD sem destruir provas materiais de crimes (Boletim de Ocorrência), o AEGIS utiliza uma arquitetura de bifurcação de evidências:

```text
[Dado gerado por suspeita de evento]
         │
         ▼
  Gravado com TTL (Time To Live) = 48h
         │
[Houve confirmação de agressão / Acionamento do 190?]
         │
  ├── SIM ──> Exceção Forense: Os dados do evento são movidos para o 
  │           "Cofre Forense" criptografado localmente no dispositivo da vítima.
  │           A prova do crime é preservada exclusivamente para uso policial.
  │
  └── NÃO ──> Falso Positivo / Rotina Normal: O Job automatizado verifica
              e executa a deleção segura em 48 horas.
         │
         ▼
  Log criptográfico de destruição gerado
  (prova de compliance — LGPD Art. 16)

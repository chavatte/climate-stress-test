<pre style="font-size: 0.5rem;">

                              \\\\\\
                           \\\\\\\\\\\\
                          \\\\\\\\\\\\\\\
-------------,-|           |C>   // )\\\\|    .o88b. db   db  .d8b.  db    db  .d8b.  d888888b d888888b d88888b
           ,','|          /    || ,'/////|   d8P  Y8 88   88 d8' '8b 88    88 d8' '8b '~~88~~' '~~88~~' 88'  
---------,','  |         (,    ||   /////    8P      88ooo88 88ooo88 Y8    8P 88ooo88    88       88    88ooooo 
         ||    |          \\  ||||//''''|    8b      88~~~88 88~~~88 '8b  d8' 88~~~88    88       88    88~~~~~ 
         ||    |           |||||||     _|    Y8b  d8 88   88 88   88  '8bd8'  88   88    88       88    88.   
         ||    |______      ''''\____/ \      'Y88P' YP   YP YP   YP    YP    YP   YP    YP       YP    Y88888P
         ||    |     ,|         _/_____/ \
         ||  ,'    ,' |        /          |                 ___________________________________________
         ||,'    ,'   |       |         \  |              / \                                           \ 
_________|/    ,'     |      /           | |             |  |                                            | 
_____________,'      ,',_____|      |    | |              \ |      chavatte@duck.com                     | 
             |     ,','      |      |    | |                |                       chavatte.vercel.app  | 
             |   ,','    ____|_____/    /  |                |    ________________________________________|___
             | ,','  __/ |             /   |                |  /                                            /
_____________|','   ///_/-------------/   |                 \_/____________________________________________/ 
              |===========,'                                                                                  
			  

</pre>

# CLIMATE STRESS TEST

**Idiomas:** 🇺🇸 [English](README.md) · 🇧🇷 **Português** 

## Brasil 2026–2030

### Modelo Baseado em Agentes para Teste de Estresse Exploratório de Risco Climático

> **Versão 2.4.0 — Reprodutibilidade e Verificação Numérica**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22836683.svg)](https://doi.org/10.5281/zenodo.22836683)  
[![NetLogo](https://img.shields.io/badge/NetLogo-7.x-4E9F3D.svg)](https://ccl.northwestern.edu/netlogo/)  
![Model](https://img.shields.io/badge/Model-Agent--Based%20Model-2563EB.svg)  
![Version](https://img.shields.io/badge/version-2.4.0-0f172a.svg)  
[![Research](https://img.shields.io/badge/Research-Exploratory-7C3AED.svg)](https://chavatte.vercel.app/projects/climate-stress-test)  
![Reproducibility](https://img.shields.io/badge/Reproducibility-Seed%20%2B%20Replications-059669.svg)

---

## DOI

**Zenodo DOI:** 10.5281/zenodo.22836683

---

## MODELO

**Plataforma:** NetLogo 7.x  
**Tipo de Modelo:** Modelo Baseado em Agentes (ABM) Exploratório  
**Domínio:** Risco Climático · Risco Sistêmico · Redes Complexas · Resiliência  
**Versão:** 2.4.0

---

## TIPO

**Modelo Baseado em Agentes**

O Climate Stress Test representa um sistema sintético de municípios atuando como agentes interativos expostos a múltiplos estressores externos e conectados por uma rede abstrata de dependências.

O modelo investiga como a vulnerabilidade local, a resiliência, a capacidade de adaptação, as condições de infraestrutura e as cascatas mediadas por redes interagem para gerar risco sistêmico.

O sistema é projetado explicitamente como um **framework computacional para testes de estresse**, e não como um sistema de previsão climática ou socioeconômica oficial.

---

## HORIZONTE

**2026–2030**

A simulação abrange um horizonte experimental de cinco anos.

```text
1 tick   = 1 mês
60 ticks = 5 anos
```

O período de 2026–2030 representa o horizonte de cenários experimentais e não deve ser interpretado como uma previsão exata das condições reais do Brasil nesses anos.

## AGENTES

**Baseline:** 100 municípios sintéticos

Cada município é representado como um agente autônomo com características heterogêneas.

### Atributos estáticos

- Exposição
    
- Vulnerabilidade
    
- Resiliência
    
- Sensibilidade hídrica
    
- Sensibilidade agrícola
    
- Sensibilidade urbana
    
- Sensibilidade ao calor
    
- Classificação regional
    

### Variáveis dinâmicas

- Hazard (Pressão climática)
    
- Estresse hídrico
    
- Impacto agrícola
    
- Estresse energético
    
- Impacto econômico
    
- Carga de cascata
    
- Risco local
    
- Dano
    
- Capacidade de recuperação
    
- Status do sistema
    

Os municípios são **entidades sintéticas** e não correspondem a municípios brasileiros reais específicos.

## PASSO TEMPORAL

**1 tick = 1 mês**

O modelo avança por meio de passos mensais de simulação.

Cada tick representa a interação entre pressão ambiental, vulnerabilidade local, capacidade de proteção, impactos setoriais, dependências de rede, efeitos em cascata, acúmulo de danos e recuperação.

A ordem conceitual do processo é:

Plaintext

```
Configurar Cenário
       ↓
Atualizar Hazard Local
       ↓
Calcular Risco Local
       ↓
Atualizar Impactos Setoriais
       ↓
Propagar Cascatas
       ↓
Aplicar Adaptação
       ↓
Aplicar Recuperação
       ↓
Calcular Métricas Agregadas
       ↓
Atualizar Estado Visual
```

# Início Rápido

## 1. Instalar o NetLogo

Faça o download e instale o **NetLogo 7.x** a partir do site oficial do NetLogo.

## 2. Baixar o modelo

Clone este repositório ou faça o download no formato ZIP:

Bash

```
git clone https://github.com/chavatte/climate-stress-test.git
cd climate-stress-test
```

Em seguida, localize o arquivo do modelo na pasta `model/`:

Plaintext

```
model/[Version_2_4-EN]_Climate_stress_Test_(Brasil-2026-2030).nlogox
model/[Version_2_4-PT-BR]_Climate_stress_Test_(Brasil-2026-2030).nlogox
```

## 3. Abrir o modelo no NetLogo

Inicie o NetLogo e abra o arquivo `.nlogox` do Climate Stress Test.

A interface principal disponibiliza os controles de cenário, botões de execução, monitores, gráficos e saídas do console.

## 4. Executar o experimento baseline

Inicie com os parâmetros padrão (baseline):

|**Variável**|**Valor**|
|---|---|
|Municípios|100|
|Pressão de aquecimento|60|
|Intensidade do El Niño|55|
|Pressão de desmatamento|35|
|Pressão urbana|55|
|Investimento em adaptação|35|
|Resiliência de infraestrutura|45|
|Densidade da rede|6|
|Sensibilidade a cascatas|40|

Execute o comando de inicialização:

Plaintext

```
setup
```

seguido de:

Plaintext

```
go
```

Cada tick representa um mês simulado. Para rodar todo o horizonte experimental automaticamente, utilize:

Plaintext

```
run-to-2030
```

Isso avança o modelo ao longo dos 60 meses do experimento.

## 5. Comparar cenários

O modelo possui três configurações experimentais principais (`FAIL OPEN`, `BALANCED` e `RESILIENT BY DESIGN`).

Para comparar todos os três cenários automaticamente sob condições iniciais idênticas (mesma semente aleatória e mesma estrutura de rede), clique em **COMPARE SCENARIOS** ou execute:

Plaintext

```
compare-scenarios
```

Para rodar cenários individualmente:

Plaintext

```
setup
↓
scenario-balanced
↓
run-to-2030
↓
print-summary
```

> Os nomes dos cenários descrevem configurações do modelo e não representam previsões de políticas públicas ou cenários oficiais do governo.

## 6. Reproduzir a execução baseline

A versão 2.4.0 utiliza:

Plaintext

```
random-seed 20260916
```

Manter a mesma versão do modelo, versão do NetLogo, parâmetros e semente aleatória reproduzirá exatamente a mesma sequência estocástica.

## 7. Executar múltiplas replicações

Para análise estatística exploratória, utilize:

Plaintext

```
replication-test 30
```

O procedimento executa 30 replicações estocásticas com sementes independentes e reporta no terminal:

Plaintext

```
Seed
Risco Sistêmico Final
Pico de Risco Sistêmico
Dano Médio Final
Total de Eventos em Cascata
Grau Médio da Rede
Densidade Realizada da Rede
```

## Fluxo Mínimo

O caminho mais rápido para rodar o modelo é:

Plaintext

```
1. Abrir o arquivo .nlogox
2. Executar setup
3. Selecionar um cenário (ou executar compare-scenarios)
4. Executar go ou run-to-2030
5. Executar print-summary
```

Para testes de reprodutibilidade:

Plaintext

```
setup
run-to-2030
print-summary
```

Para testes de replicação Monte Carlo:

Plaintext

```
replication-test 30
```

## Simulação Interativa no Navegador

Uma versão web interativa também está disponível:

**Web Simulation:** [Climate Stress Test ![Português](https://flagcdn.com/24x18/br.png)](https://chavatte.vercel.app/html-projects/climate_stress_test/pt-br/index.html)

**Web Simulation:** [Climate Stress Test ![English](https://flagcdn.com/24x18/us.png)](https://chavatte.vercel.app/html-projects/climate_stress_test/us/index.html)

A versão web permite explorar a simulação sem a necessidade de instalar a aplicação desktop do NetLogo. Para trabalhos acadêmicos e pesquisas científicas, o modelo oficial do NetLogo deve ser utilizado como artefato primário.

# 1. Resumo

O Climate Stress Test — Brasil 2026–2030 é um Modelo Baseado em Agentes exploratório desenvolvido em NetLogo para investigar a vulnerabilidade sistêmica e as interações em cascata entre municípios sintéticos expostos a estressores climáticos, ambientais, de infraestrutura e de rede.

O objetivo do modelo não é prever o futuro do Brasil, mas operar como um **laboratório computacional para testes de estresse**: cenários controlados permitem examinar como variações na resiliência, na adaptação, na estrutura de rede e na sensibilidade a cascatas influenciam o risco sistêmico e os danos simulados.

A versão 2.4.0 consolida mecanismos de reprodutibilidade (semente fixa), comparação automatizada de cenários (`compare-scenarios`), diagnósticos de densidade de grafos e rotinas de replicação estocástica (`replication-test`).

# 2. Pergunta de Pesquisa

A pergunta central de pesquisa é:

> **Como estressores climáticos interativos, vulnerabilidade municipal heterogênea, capacidade de resiliência e dependências de rede contribuem para o risco sistêmico e efeitos em cascata dentro de um sistema municipal sintético?**

# 3. Objetivos do Modelo

### 3.1 Explorar vulnerabilidade sistêmica

Representar como múltiplos estressores interativos geram riscos além dos impactos locais isolados.

### 3.2 Explorar efeitos em cascata

Demonstrar como o risco em um município pode afetar municípios vizinhos ou dependentes por meio de uma rede abstrata.

### 3.3 Examinar resiliência

Analisar a relação entre resiliência, infraestrutura, adaptação, acúmulo de danos e recuperação.

### 3.4 Suportar experimentação reprodutível

Fornecer controle determinístico por sementes aleatórias, comparações automáticas de cenários e simulações estocásticas repetidas.

# 4. Estrutura Conceitual

Plaintext

```
                 PRESSÃO CLIMÁTICA / AMBIENTAL
                              │
                              ▼
                         ┌─────────┐
                         │ HAZARD  │
                         └────┬────┘
                              │
                              ▼
                 ┌─────────────────────────┐
                 │ Exposição × Vulnerabilidade│
                 └───────────┬─────────────┘
                             │
                             ▼
                       ┌───────────┐
                       │Risco Local│
                       └─────┬─────┘
                             │
                ┌────────────┴────────────┐
                │                         │
                ▼                         ▼
       Resiliência / Adaptação       Impactos Setoriais
                │                         │
                └────────────┬────────────┘
                             │
                             ▼
                     ┌──────────────┐
                     │ Dependências │
                     └──────┬───────┘
                            │
                            ▼
                     ┌──────────────┐
                     │   Cascatas   │
                     └──────┬───────┘
                            │
                            ▼
                    ┌────────────────┐
                    │ Risco Sistêmico│
                    └───────┬────────┘
                            │
                            ▼
                   Dano / Recuperação
```

# 5. Arquitetura dos Agentes

Cada município sintético contém atributos estáticos e estados dinâmicos.

## 5.1 Exposição

Nível de exposição do agente ao ambiente de perigo simulado.

## 5.2 Vulnerabilidade

Suscetibilidade do agente a impactos resultantes do hazard.

## 5.3 Resiliência

Capacidade do agente de absorver estresse e contribuir para a recuperação.

## 5.4 Sensibilidades setoriais

Parâmetros sintéticos individuais para:

- Água
    
- Agricultura
    
- Sistemas urbanos
    
- Calor
    

## 5.5 Status visual

Os municípios alternam entre quatro estados visuais qualificativos:

Plaintext

```
VERDE    → STABLE (Estável)
AMARELO  → WARNING (Alerta)
LARANJA  → HIGH (Alto Risco)
VERMELHO → CRITICAL (Crítico)
```

# 6. Formulação do Risco

## 6.1 Componentes do Hazard

O modelo combina quatro componentes principais de pressão:

|**Componente**|**Peso**|
|---|---|
|Pressão de aquecimento|0,45|
|Intensidade do El Niño|0,20|
|Pressão de desmatamento|0,20|
|Pressão urbana|0,15|

A sazonalidade é modelada com amplitude de aproximadamente ±10%, e uma tendência de crescimento anual de ~1,2% é aplicada.

## 6.2 Risco Local Bruto

Plaintext

```
RawRisk = Hazard × Exposure × Vulnerability / 10000
```

## 6.3 Risco Líquido

O risco local líquido é mitigado pela resiliência, infraestrutura efetiva e investimentos em adaptação:

Plaintext

```
Net Risk = Raw Risk − Efeito Resiliência − Efeito Infraestrutura − Efeito Adaptação
```

## 6.4 Dano e Recuperação

O dano combina risco local, impacto econômico e carga de cascata. A recuperação ocorre de forma gradual (coeficiente de 0,020/mês).

# 7. Mecanismo de Cascata

Os municípios estão conectados por uma rede de dependências abstratas (`dependencies`).

A pressão de cascata depende do risco dos vizinhos, da conectividade da rede e da sensibilidade do agente.

### Memória de cascata

A versão 2.4.0 mantém memória de carga de cascata com decaimento exponencial de 8% ao mês (`cascade-load * 0.92`) antes de incorporar novas entradas de transbordamento (_spillover_).

# 8. Cenários

## 8.1 Fail-Open

Eficiência de adaptação e infraestrutura em **55%** (baixa proteção).

## 8.2 Balanced

Eficiência nominal de **100%** (proteção baseline).

## 8.3 Resilient

Eficiência otimizada de **até 130%** (alta proteção).

# 9. Limitações

- **Municípios Sintéticos:** Os agentes não correspondem a municípios reais específicos.
    
- **Topologia Abstrata:** O arranjo espacial e as conexões de rede são estilizados.
    
- **Parâmetros Normalizados:** As variáveis operam em escalas relativas de 0 a 100, e não em unidades físicas absolutas.
    

# 10. Citação

Se você utilizar ou analisar este modelo em pesquisas acadêmicas, cite esta versão de software:

**Chavatte, João Carlos. (2026). _Climate Stress Test — Brazil 2026–2030: An Exploratory Agent-Based Model for Systemic Climate Risk Stress Testing_. Version 2.4.0. Zenodo.**

**DOI:** 10.5281/zenodo.22836683

O registro em formato legível por máquina está disponível no arquivo `CITATION.cff`.

# 11. Licença

- **Código-Fonte:** Licença MIT (`LICENSE`)
    
- **Documentação:** Creative Commons Atribuição 4.0 Internacional (`LICENSE-DOCS`)
    

# Status

Plaintext

```
╔══════════════════════════════════════════════════════╗
║  CLIMATE STRESS TEST                                 ║
║  BRASIL 2026–2030                                    ║
║                                                      ║
║  VERSÃO         : 2.4.0                              ║
║  MODELO         : BASEADO EM AGENTES                 ║
║  PLATAFORMA     : NETLOGO                            ║
║  HORIZONTE      : 60 MESES                           ║
║  AGENTES        : 100 MUNICÍPIOS SINTÉTICOS          ║
║  REPRODUZÍVEL   : SIM                                ║
║  REPLICAÇÃO     : DISPONÍVEL                         ║
║                                                      ║
║  STATUS         : ARTEFATO DE PESQUISA EXPLORATÓRIA  ║
╚══════════════════════════════════════════════════════╝
```

> **Este modelo é um teste de estresse computacional — não uma previsão oficial.**
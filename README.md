
# Avaliador de Robustez de LLM & Testador de Guardrails

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-00ff88?style=flat-square&logo=github)](https://tavardt-brasil.github.io/llm-robustness-evaluator-br/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![OWASP LLM](https://img.shields.io/badge/OWASP-LLM01%2FLLM02-red?style=flat-square)](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
[![NIST AI RMF](https://img.shields.io/badge/NIST-AI%20RMF-blue?style=flat-square)](https://www.nist.gov/artificial-intelligence)

**Auditoria Defensiva de Guardrails, Injeção de Prompt e Resiliência de Modelos de IA**

Ferramenta interativa e CLI defensiva para desenvolvedores avaliarem a robustez dos guardrails de LLMs contra vetores de injeção, vazamento de prompt e ataques estruturais. Pontuação de Resiliência 0-100 + blueprint defensivo.

***

## Visão Geral

> **OWASP LLM01 & LLM02** | **NIST AI RMF** | **100% Defensive  -  Zero Offensive Payloads**

## 5 Vetores de Teste Defensivos

| # | Vector | Coverage |
|-|-|-|
| 1 | **Escape de Delimitador**  -  Detecta tokens de controle injetados (`</system>`, `[/INST]`, ` ``` `) | ✅ |
| 2 | **Vazamento de System Prompt**  -  Identifica padrões de extração de instruções do sistema | ✅ |
| 3 | **Substituição de Papel/Persona**  -  Verifica resistência a sobreposições (DAN, modo dev) | ✅ |
| 4 | **Ofuscação Estrutural**  -  Avalia cobertura contra Base64, leetspeak, homóglifos Unicode | ✅ |
| 5 | **Injeção Indireta de Contexto**  -  Simula documento RAG com payload embutido | ✅ |

***

## Ferramenta Online

Acesse a ferramenta interativa diretamente:

🌐 **[https://tavardt-brasil.github.io/llm-robustness-evaluator-br/](https://tavardt-brasil.github.io/llm-robustness-evaluator-br/)**

***

## Uso via CLI

### Instalação

```bash
git clone https://github.com/TAVARDT-Brasil/llm-robustness-evaluator-br.git
cd llm-robustness-evaluator-br
pip install -r requirements.txt
```

### Execução

```bash
python llm_robustness_evaluator.py -prompt "You are a helpful assistant."
```

```
Resilience Score: 85/100
✅ V1 Delimiter Escape  -  PASS
✅ V2 System Prompt Leakage  -  PASS
✅ V3 Role/Persona Override  -  PASS
✅ V4 Structural Obfuscation  -  PASS
⚠️  V5 Indirect Context Injection  -  WARNING
```

***

## Arquitetura Defensiva

O blueprint defensivo inclui:

- 🐍 Filtro Python para detecção de padrões de injeção
- 📦 Middleware TypeScript para APIs Next.js
- 🔒 Template de System Prompt reforçado com delimitadores imutáveis

***

## Portais Oficiais

Acesse a rede oficial de portais TAVARDT:

| Portal | URL |
|-|-|
| Portal Oficial TAVARDT | [Portal Institucional](https://ag.tavardt.com/br/) |
| Central de Ferramentas | [Central de Ferramentas](https://tools.tavardt.com/br/) |
| Contato | [Canal de Contato](https://ag.tavardt.com/br/contact/) |
| GitHub | [https://github.com/TAVARDT-Brasil](https://github.com/TAVARDT-Brasil) |

***

## Licença

MIT License  -  uso livre para fins defensivos e educacionais.

***

<p align="center">
  <strong>TAVARDT  -  Brasil</strong><br>
  <a href="https://ag.tavardt.com/br/">https://ag.tavardt.com/br/</a> &bull;
  <a href="https://tools.tavardt.com/br/">https://tools.tavardt.com/br/</a><br>
  &copy; 2026 TAVARDT. Todos os direitos reservados.
</p>

***

© 2026 TAVARDT. Todos os direitos reservados.

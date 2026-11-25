# Avaliador de Robustez de LLM & Testador de Guardrails

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-5b3cf5.svg)](https://tavardt-brasil.github.io/llm-robustness-evaluator-br/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

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

## Licença

MIT License  -  uso livre para fins defensivos e educacionais.

***

## Links Úteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suíte de Diagnósticos:** https://tools.tavardt.com/br/
* **Contato Técnico:** https://ag.tavardt.com/br/contato/

***

### Licença
Distribuído sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter detalhes completos.

***

© 2026 TAVARDT. Todos os direitos reservados.

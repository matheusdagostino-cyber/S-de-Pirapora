# Agentes de Análise de Edital de Concessão de RSU

## Uso no claude.ai/code
Um agente por vez (evita timeout). Os agentes 01–03 têm 2 fases; 04 e 05 são tarefa única; 06 consolida.

| Comando | O que faz | Output |
|---|---|---|
| `siga agentes/01_concessao.md fase 1` | Extrai dispositivos de concessão | `01a_concessao_extracao.md` |
| `siga agentes/01_concessao.md fase 2` | Analisa (lê 01a + 02a + 03a + 05) | `01b_concessao_analise.md` |
| `siga agentes/02_licitacao.md fase 1` | Extrai dispositivos de habilitação | `02a_licitacao_extracao.md` |
| `siga agentes/02_licitacao.md fase 2` | Analisa (lê 02a + 01a + 03a) | `02b_licitacao_analise.md` |
| `siga agentes/03_gestao_riscos.md fase 1` | Extrai gestão comercial + matriz de riscos | `03a_gestao_riscos_extracao.md` |
| `siga agentes/03_gestao_riscos.md fase 2` | Analisa (lê 03a + 01a + 05) | `03b_gestao_riscos_analise.md` |
| `siga agentes/04_erros_inconsistencias.md` | Varredura formal integral | `04_erros_inconsistencias.md` |
| `siga agentes/05_caderno_encargos.md` | Análise técnico-operacional | `05_caderno_encargos.md` |
| `siga agentes/06_consolidacao.md` | Funde, deduplica e prioriza tudo | `06_consolidacao.md` |

## Sequência recomendada
0. Declare a **perspectiva** da análise (ver `CLAUDE.md`).
1. Fases 1 dos agentes 01, 02 e 03 (paralelizáveis se não der timeout).
2. Agente 04 (independente) e agente 05.
3. Fases 2 dos agentes 01, 02 e 03 — cada um já enxerga as extrações dos demais e o relatório de erros (04).
4. Agente 06 — consolidação final.
5. O `06_consolidacao.md` é o entregável-base para impugnação, representação ou nota interna.

## Para novo edital
1. Crie repositório privado no GitHub.
2. Copie `CLAUDE.md` e a pasta `agentes/`.
3. Suba os PDFs.
4. No claude.ai/code, conecte o repo e rode os agentes.
5. Se for rodar mais de um edital no mesmo repo, prefixe os outputs com a sigla do edital (evita sobrescrita).

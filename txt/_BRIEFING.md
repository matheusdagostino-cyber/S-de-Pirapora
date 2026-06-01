# BRIEFING COMPARTILHADO — Análise do Edital de Concessão de RSU (Salto de Pirapora)

## Perspectiva declarada
Não foi declarada perspectiva pelo solicitante. Conforme `CLAUDE.md`, **assume-se a perspectiva do LICITANTE / PROPONENTE** (achados viram impugnação, pedido de esclarecimento, risco a precificar ou risco a alocar). Registrar essa premissa no topo do output.

## Fontes (texto já extraído dos PDFs — use estes arquivos, NÃO os PDFs)
Todos em `/home/user/S-de-Pirapora/txt/`:
- `edital.txt` — Edital da Concorrência Presencial 001/2026. Contém o corpo do edital (Caps. I–VIII), e os anexos no MESMO arquivo:
  - ANEXO I – Modelos de cartas/declarações (~linha 6500)
  - ANEXO II – Diretrizes Proposta Comercial + **PLANO DE NEGÓCIOS (MODELO B)** = template a preencher pelo licitante (~6590–7290)
  - ANEXO III – Diretrizes Proposta Técnica (~7294)
  - Caderno de encargos / projeto básico / especificações técnicas (diagnóstico, tecnologias, CTR, módulos, ecopontos, educação ambiental, aterro) (~8100–14200)
  - Indicação de Bens Reversíveis (~14225)
  - Indicadores de Desempenho (~14763)
  - Diretrizes Ambientais (~15614)
  - **MATRIZ DE RISCOS** (tabela Concessionária/Poder Concedente/Entidade Reguladora) (~16000–16500)
  - ANEXO XI – Minuta do Termo de Recebimento do Aterro (~16489)
- `contrato.txt` — ANEXO VIII, Minuta do Contrato de Concessão Administrativa.
- `etp.txt` — Estudo Técnico Preliminar (ETP) da concessão do aterro.

**Nota importante:** não há Plano de Negócios com números reais — o PN é o MODELO B (template) que o licitante preenche. Onde uma instrução pedir "valores reais do PN", registrar que o PN é template e que os parâmetros econômicos (inadimplência, custo de cobrança, CAPEX detalhado) não estão fixados pelo edital; extrair o que houver nas diretrizes/ETP.

## Como ler os .txt
São grandes (edital ~16.700 linhas). Use a ferramenta Read com `offset`/`limit` em blocos, ou `grep`/Bash para localizar trechos por palavra-chave e então ler o entorno. Cite sempre: documento + cláusula/item + transcrição literal.

## Regras de citação e jurisprudência (de CLAUDE.md — INVIOLÁVEIS)
- Legislação: "art. XX, § Y.º, inciso Z, da Lei n.º XXXXX/XXXX".
- **NUNCA fabricar** número de acórdão/ementa/relatoria. Verificar na web antes de citar.
- Se o portal oficial (pesquisa.apps.tcu.gov.br, scon.stj.jus.br) não puder ser acessado/confirmado: **dizer isso expressamente**, não citar de memória, e registrar o achado apenas com ancoragem legal/doutrinária — sem precedente.
- Se não localizar: escrever "não localizei precedente específico".
- Ancoragem normativa de cada achado: *dispositivo expresso* / *construção interpretativa* / *sem fundamento localizado*.
- **Não** classificar a tese como forte/fraca. Sinalizar o contra-argumento provável da Administração/TCU.

## Legislação-base
Lei 14.133/2021 · Lei 8.987/1995 · Lei 11.079/2004 · Lei 11.445/2007 · Lei 14.026/2020 · Lei 12.305/2010 · Decreto 11.599/2023 · IN RFB 1.700/2017 · NR 1/ANA (Res. 79/2021) · NR 13/ANA (Res. 271/2025) · Súmulas 253 e 263/TCU. Lex specialis do contrato: 8.987/1995, 11.079/2004, 11.445/2007.

## Saída
Salvar o output na RAIZ do repositório (`/home/user/S-de-Pirapora/`) com o nome de arquivo indicado na instrução do agente. Markdown, em português.

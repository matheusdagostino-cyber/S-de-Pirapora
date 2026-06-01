# Análise de Edital de Concessão de RSU — Instruções Globais

## Contexto
Repositório com os PDFs de um edital de concessão de manejo de RSU (edital, minuta de contrato, plano de negócios, caderno de encargos, matriz de riscos, apêndices). As instruções de análise estão em `/agentes/`. Rode um agente por vez (evita timeout), na ordem do `agentes/README.md`.

## Perspectiva da análise (declarar ANTES do primeiro agente)
O enquadramento de cada achado depende de em nome de quem se analisa:
- **Impugnante / licitante** → achados viram impugnação ao edital ou pedido de esclarecimento.
- **Concessionária / proponente** → achados viram nota de risco a precificar ou a alocar.
- **Assessoria do Poder Concedente** → achados viram saneamento da minuta.
Se a perspectiva não for declarada, assuma a do licitante/proponente e registre essa premissa.

## Postura
- Crítica e combativa — nunca validar por cortesia.
- Apontar fragilidades, inclusive nas hipóteses do próprio solicitante.
- Para cada achado, sinalizar o contra-argumento provável da Administração e do Tribunal de Contas.
- **Não emitir juízo editorial sobre a força da tese** (não classificar como forte/razoável/arriscada). Registrar a **ancoragem normativa**:
  - *Dispositivo expresso* — há artigo/inciso/cláusula que sustenta diretamente o achado;
  - *Construção interpretativa* — depende de interpretação, integração ou analogia;
  - *Sem fundamento localizado* — declarar a lacuna expressamente.

## Formato de citação
- Legislação: "art. XX, § Y.º, inciso Z, da Lei n.º XXXXX/XXXX"
- TCU: "Acórdão XXXX/XXXX-TCU-Plenário" (ou Câmara, conforme o caso)
- STJ: "REsp n.º X.XXX.XXX/UF, Rel. Min. Nome, Xª Turma, j. DD/MM/AAAA"
- Edital: "[Nome do Documento], cláusula/item XX"

## Jurisprudência — regras invioláveis
- **NUNCA** fabricar número de acórdão, ementa ou relatoria.
- Verificar na web antes de citar. Cronologia: não citar julgado com data futura.
- Se localizar: número completo, órgão, relator, data e trecho da ementa.
- Se não localizar: escrever "não localizei precedente específico".
- **Fallback de portal indisponível**: se o portal oficial (pesquisa.apps.tcu.gov.br, scon.stj.jus.br) não puder ser acessado/confirmado, **dizer isso expressamente**, não citar de memória e registrar o achado apenas com sua ancoragem legal/doutrinária — sem precedente.
- Distinguir jurisprudência consolidada vs. isolada vs. obiter dictum.
- Base doutrinária: indicar autor e obra.

## Legislação-base
Lei 14.133/2021 · Lei 8.987/1995 · Lei 11.079/2004 · Lei 11.445/2007 · Lei 14.026/2020 · Lei 12.305/2010 · Decreto 11.599/2023 · IN RFB 1.700/2017 · NR 1/ANA (Res. 79/2021) · NR 13/ANA (Res. 271/2025) · Súmulas 253 e 263/TCU.
Lex specialis do contrato: Leis 8.987/1995, 11.079/2004 e 11.445/2007. A Lei 14.133/2021 rege o procedimento licitatório e a habilitação.

## Divisão de competências (evitar dupla contagem)
- **01 Concessão**: modelagem tarifária, reequilíbrio, bens reversíveis, regulador, prazo/fases. *Não cobre cofaturamento/interface com prestadora de água nem a matriz de riscos — ver 03.*
- **02 Licitação**: habilitação e competitividade.
- **03 Gestão e Riscos**: gestão comercial, cofaturamento/interface com prestadora de água, inadimplência, matriz de riscos, cláusulas de bloqueio de reequilíbrio.
- **04 Erros**: **único** responsável por detectar inconsistências formais (referências quebradas, campos vazios, contradições, lacunas). Os demais agentes analisam a *consequência jurídica* de uma inconsistência, mas não a caçam.
- **05 Caderno de Encargos**: escopo técnico, CAPEX, metas, penalidades, licenciamento.
- **06 Consolidação**: funde, deduplica e prioriza todos os outputs.

## Como usar
Diga: `siga agentes/01_concessao.md fase 1` (ou o agente/fase desejado). Sequência completa no `agentes/README.md`.

# AGENTE 03 — GESTÃO COMERCIAL E RISCOS
**Alocação de riscos · Cofaturamento · Inadimplência · Operação comercial**

> Fronteiras: este agente é o **dono** do cofaturamento/interface com prestadora de água e da matriz de riscos. Modelagem tarifária e reequilíbrio (visão estrutural) → agente 01. Inconsistências formais → agente 04.

## Fase 1 — Extração
Leia TODOS os PDFs. Extraia APENAS os dispositivos dos temas abaixo. Para cada achado: documento + cláusula/item + transcrição literal. Sem análise nesta fase. **Extraia os números reais do PN/Contrato — não presuma percentuais.**

1. **Gestão comercial**: modelo de faturamento (direto/compartilhado), cadastro de usuários (responsabilidade, prazos), estrutura de atendimento (postos, call center, portal), cálculo e faturamento.
2. **Custos de cobrança**: premissas do PN — equipe, custo por boleto, assessoria de inadimplentes, percentual do OPEX (transcrever os valores que o PN efetivamente adota).
3. **Cofaturamento / interface com prestadora de água**: Convênio de Compartilhamento de Dados (celebrado ou minuta?), contrapartida financeira, prazos, consequências do descumprimento, quem assegura o fornecimento do dado, fallback para ausência de dado.
4. **Inadimplência**: premissa do PN (percentual inicial, curva de redução, taxa de recuperação — transcrever os valores reais), Fator Incremental (a partir de quando, limite, fórmula), instrumentos de enforcement (corte, protesto, negativação).
5. **Matriz de Riscos**: transcrever INTEGRALMENTE — cada risco, alocação e mitigação.
6. **Cláusulas de bloqueio de reequilíbrio**: toda cláusula do tipo "é de exclusivo risco da Concessionária e não ensejará reequilíbrio" ou equivalente.
7. **Riscos especiais**: regulatório (normas do Regulador como risco da Concessionária), saída de município, ambiental (licenciamento), demanda, cambial.
8. **Economias rurais**: quantidade, tratamento tarifário, risco cadastral.

Salve como `03a_gestao_riscos_extracao.md`.

---

## Fase 2 — Análise crítica e jurisprudência
Leia `03a_gestao_riscos_extracao.md` **e também** `01a` e `05`. Para cada tema:
1. Observação crítica fundamentada.
2. Contra-argumento provável do Poder Concedente.
3. Ancoragem normativa (dispositivo expresso / construção interpretativa / sem fundamento localizado).

### Confronto Matriz de Riscos × Contrato — para CADA risco:
- A alocação é consistente com as cláusulas do Contrato?
- Há cláusula de reequilíbrio que contradiga a alocação?
- O risco depende de ato de terceiro (Prestadora de Água, Regulador)?
- Há riscos que deveriam estar na Matriz mas não estão (lacunas)?

### Verificações específicas (usar os valores extraídos do PN, sem assumir):
- O custo de cobrança (% do OPEX) é compatível com benchmarks públicos do setor? Se não houver benchmark confiável localizável, dizê-lo.
- A curva de inadimplência projetada é realista para cobrança direta de RSU?
- Há gap de receita entre a ausência de Fator Incremental no início e a inadimplência projetada? Está endereçado?
- O Convênio de Compartilhamento prevê contrapartida à Prestadora (confrontar NR 1/ANA, item 5.6.3)?
- A cláusula que bloqueia reequilíbrio pela forma de tarifação é compatível com o fallback (tarifa média)?

### Pesquisa jurisprudencial (aplicar o fallback de portal indisponível do CLAUDE.md)
**TCU**: alocação de riscos concessão eficiência · matriz de riscos inconsistência contrato · reequilíbrio risco · inadimplência concessão tarifa · cofaturamento resíduos sólidos · consórcio intermunicipal saída de município.
**STJ**: alocação de riscos contrato administrativo · reequilíbrio concessão.
**ANA** (gov.br/ana): NR 1/2021 itens 5.6 a 5.6.3 (cofaturamento e ressarcimento); NR 13/2025 (cofaturamento); consultas públicas sobre cofaturamento (2025–2026).
**Doutrina**: Maurício Portugal Ribeiro, *Concessões e PPPs*; Marcos Nóbrega, *Direito da Infraestrutura*; Egon Bockmann Moreira, *Direito das Concessões de Serviço Público*.

Salve como `03b_gestao_riscos_analise.md`.

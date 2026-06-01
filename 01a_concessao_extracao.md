# AGENTE 01 — CONCESSÃO · FASE 1 (EXTRAÇÃO)
## Concorrência Presencial 001/2026 — Concessão Administrativa (PPP) de manejo de RSU — Salto de Pirapora/SP

> **Premissa de perspectiva (CLAUDE.md / _BRIEFING.md):** não houve declaração do solicitante; assume-se a perspectiva do **LICITANTE / PROPONENTE**.
> **Natureza do contrato:** o modelo é **concessão administrativa (PPP) regida pela Lei 11.079/2004**, remunerada por **CONTRAPRESTAÇÃO pública mensal** — não por tarifa cobrada do usuário. Os achados de "estrutura tarifária" foram lidos sob essa chave (não há tarifa de usuário; há contraprestação + fonte de custeio TMRSU).
> **Fronteiras:** cofaturamento/interface com prestadora de água e a Matriz de Riscos são do agente 03; inconsistências formais (campos `[•]` em branco, referências cruzadas erradas) são do agente 04. Aqui apenas se **extrai** o dispositivo. Esta fase **não** contém análise.
> **Fontes:** `contrato.txt` (Minuta do Contrato — Anexo VIII), `edital.txt` (corpo + anexos), `etp.txt` (ETP).

---

## TEMA 1 — ESTRUTURA "TARIFÁRIA" (remuneração: CONTRAPRESTAÇÃO + TMRSU)

**1.1 — Não há tarifa de usuário; remuneração é a CONTRAPRESTAÇÃO pública.**
- `contrato.txt`, Cláusula 1.11 (Definições): *"CONTRAPRESTAÇÃO: é a remuneração mensal a ser paga pelo PODER CONCEDENTE à CONCESSIONÁRIA em decorrência da prestação dos SERVIÇOS, calculada conforme especificado neste CONTRATO e com base nos valores constantes da PROPOSTA COMERCIAL da LICITANTE VENCEDORA;"*
- `contrato.txt`, Cláusula 22.1 (Fontes de Receita): *"A remuneração da CONCESSIONÁRIA advirá da receita decorrente do pagamento da CONTRAPRESTAÇÃO pelo PODER CONCEDENTE, em razão da prestação dos SERVIÇOS na ÁREA DA CONCESSÃO, [...] sem prejuízo do recebimento de RECEITAS EXTRAORDINÁRIAS, nos termos deste CONTRATO."*

**1.2 — Fonte de custeio: Taxa de Manejo de RSU (TMRSU), sem exclusividade.**
- `contrato.txt`, Cláusula 22.1.1: *"[...] declara o PODER CONCEDENTE que o Município instituiu, por meio de legislação municipal específica, a Taxa de Manejo de Resíduos Sólidos Urbanos – TMRSU, a qual constitui fonte relevante de receita pública municipal destinada ao custeio dos serviços objeto da CONCESSÃO, sem caráter exclusivo, podendo o PODER CONCEDENTE utilizar, para fins de adimplemento da CONTRAPRESTAÇÃO, outras fontes de recursos orçamentários, observada a legislação aplicável."*
- `contrato.txt`, Cláusula 1.32 (RECEITAS): *"são as receitas arrecadadas pelo PODER CONCEDENTE, incluindo aquelas decorrentes da prestação dos SERVIÇOS e outras fontes orçamentárias, destinadas ao sistema de pagamento da CONCESSÃO, a serem direcionadas à CONTA VINCULADA [...]"*

**1.3 — Critério de julgamento / "tarifa-base": Fator K aplicado sobre tabela de CONTRAPRESTAÇÃO de referência.**
- `edital.txt`, Seção V – Critério de Julgamento, item 10: *"A LICITAÇÃO será processada e julgada pela combinação dos critérios de menor valor da CONTRAPRESTAÇÃO a ser paga pelo PODER CONCEDENTE combinado com a melhor técnica, nos termos do artigo 12, inciso II, alínea 'b', da Lei federal nº 11.079/2004."*
- `edital.txt`, item 133: *"A PROPOSTA COMERCIAL deverá conter a oferta do multiplicador K (Fator K), com 4 (quatro) casa decimais, a ser aplicado sobre os valores das CONTRAPRESTAÇÕES constantes do Anexo II deste EDITAL [...]"*
- `edital.txt`, Anexo II, MODELO A: *"[...] oferta do Fator K, com 4 (quatro) casa decimais, cujo valor máximo é de 1,0000 (um inteiro) e será aplicado linearmente sobre os valores da CONTRAPRESTAÇÃO constante deste EDITAL."*
- `edital.txt`, Anexo II: *"O somatório total de CONTRAPRESTAÇÕES máximo admitido é de R$ R$ 566.135.178,00 (Quinhentos e sessenta e seis milhões, cento e trinta e cinco mil, cento e setenta e oito reais);"*
- `edital.txt`, Anexo II, MODELO A (tabela de CONTRAPRESTAÇÃO de referência, valores preenchidos): Ano 1 = **R$ 11.088.000**; Anos 2–4 = **R$ 12.240.540**; Anos 5 a 30 = **R$ 19.645.630** (por ano).
- `edital.txt`, item 167.b (desclassificação): desclassifica proposta que *"considerarem CONTRAPRESTAÇÃO anual acima dos montantes indicados no Anexo II deste EDITAL"*.
- `edital.txt`, fórmula da Nota Comercial — Anexo II e item 166: **NC = 1000 x (X1 / X2)**, onde *"X1 - Menor Fator K proposto entre os LICITANTES classificados; X2 – Fator K do Contrato proposto pelo LICITANTE classificado."* Pesos: **NF = (0,60 x NT) + (0,40 x NC)** (técnica 60 / comercial 40).
- `contrato.txt`, Cláusula 23.1: a CONTRAPRESTAÇÃO mensal consta em **tabela ano a ano (anos 1 a 30), com todos os valores em branco `[•]`** (a ser preenchida pela proposta vencedora).

**1.4 — Redutor de desempenho sobre a CONTRAPRESTAÇÃO (não há tarifa social, volume mín./máx., categorias de usuário, fator de progressão tarifária).**
- `contrato.txt`, Cláusula 23.2: *"[...] deverá ser aplicado aos valores constantes da tabela acima eventual redutor decorrente do não atendimento aos INDICADORES DE DESEMPENHO referentes à prestação dos SERVIÇOS no mês imediatamente precedente, nos termos previstos no Anexo V do EDITAL e na Cláusula 17 deste CONTRATO."*
- *Registro de ausência:* não há, no contrato/edital, tarifa-base de usuário, categorias de usuários, fator de progressão, tarifa social, volume mínimo/máximo — coerente com o modelo PPP por contraprestação. **Lacuna a confirmar pelo 04.**

---

## TEMA 2 — FORMA DE ARRECADAÇÃO COMO ELEMENTO DA MODELAGEM

**2.1 — Fluxo de pagamento via CONTA VINCULADA / AGENTE DEPOSITÁRIO (estrutura de garantia da PPP).** (detalhamento de cofaturamento/interface = agente 03)
- `contrato.txt`, Cláusula 1.1 (AGENTE DEPOSITÁRIO — campo `[•]` em branco), 1.9 (CONTA GARANTIA), 1.10 (CONTA VINCULADA): RECEITAS são destinadas à CONTA VINCULADA, *"cuja finalidade é pagar a CONTRAPRESTAÇÃO à CONCESSIONÁRIA, e compor e repor o SALDO MÍNIMO na CONTA GARANTIA, quando necessário"*.
- `contrato.txt`, Cláusula 23.4.1: *"A partir da emissão da primeira Nota Fiscal [...] as RECEITAS deverão ser direcionadas à CONTA VINCULADA, em valores suficientes para os pagamentos devidos, mediante mecanismos operacionais que assegurem a sua alocação automática ou sistemática [...]"*
- `contrato.txt`, Cláusula 23.4.1.1: *"O PODER CONCEDENTE adotará as providências necessárias para implementação de fluxo financeiro que priorize a destinação das RECEITAS à CONTA VINCULADA, podendo, para tanto, estabelecer instruções permanentes junto às instituições arrecadadoras ou ao agente financeiro responsável."*

**2.2 — Ordem de pagamento mensal e gatilho de garantia.**
- `contrato.txt`, Cláusula 23.4 (itens 1 a 5) e 23.5: pagamento mensal por NF (vencimento 20 dias), transferência automática até o valor da CONTRAPRESTAÇÃO, recomposição do SALDO MÍNIMO, devolução do remanescente ao Poder Concedente; *"se no vencimento da Nota Fiscal a CONTRAPRESTAÇÃO não tiver sido integralmente paga, será adotado o procedimento de acionamento da GARANTIA DE PAGAMENTO DA PPP, conforme Cláusula 24."*
- `contrato.txt`, Cláusula 23.6 (inadimplemento > 90 dias): faculta à Concessionária *"suspender os investimentos em curso, bem como as atividades que não sejam estritamente necessárias à continuidade dos SERVIÇOS, sem prejuízo da rescisão do CONTRATO."*
- `contrato.txt`, Cláusula 1.37 + 24.3/24.4: **SALDO MÍNIMO = 3x a média das 3 últimas CONTRAPRESTAÇÕES**, recalculado trimestralmente.

---

## TEMA 3 — RECEITAS EXTRAORDINÁRIAS / ACESSÓRIAS

**3.1 — Definição (art. 11 da Lei 8.987/95) — inclui resíduos de terceiros/outros Municípios.**
- `contrato.txt`, Cláusula 1.33: *"RECEITAS EXTRAORDINÁRIAS: são as receitas alternativas, complementares, acessórias ou oriundas de projetos associados, referidas no artigo 11 da Lei federal nº 8.987/95, que a CONCESSIONÁRIA poderá auferir, direta ou indiretamente, [...] incluídas aquelas decorrentes da disposição e/ou da destinação final ambientalmente adequada de resíduos sólidos recebidos de outros Municípios e de geradores privados;"* (definição equivalente em `edital.txt`, linha ~685).

**3.2 — Cláusula 26 (Receitas Extraordinárias) — fontes, aprovação prévia, compartilhamento, natureza aleatória.**
- `contrato.txt`, Cláusula 26.1: exploração *"por sua exclusiva responsabilidade"*, *"desde que previamente aprovado pelo PODER CONCEDENTE"*.
- `contrato.txt`, Cláusula 26.3 — fontes listadas (rol exemplificativo "dentre outras"): (1) *"serviços de publicidade que envolvam a exploração de mídias publicitárias, em todos os formatos possíveis"*; (2) *"comercialização de resíduos recicláveis ou subprodutos resultantes do processo de tratamento e destinação final operado pela CONCESSIONÁRIA"*; (3) *"destinação final de resíduos sólidos oriundos de geradores privados e/ou de outros Municípios."*
  - **Registro de ausência:** o rol **não menciona expressamente** biogás, biometano, CDR ou créditos de carbono. Podem ser lidos como "subprodutos" (26.3.2) ou "dentre outras", mas não há dispositivo expresso nominando-os. (Cruzamento com Caderno de Encargos = agente 05; efeito jurídico = Fase 2.)
- `contrato.txt`, Cláusula 26.4: *"Não serão consideradas RECEITAS EXTRAORDINÁRIAS aquelas decorrentes de aplicações no mercado financeiro, valores recebidos de seguros e por penalidades pecuniárias [...]"*
- `contrato.txt`, Cláusulas 26.5 e 26.6: exige *"plano comercial de exploração"* prévio (objeto, fluxo de caixa, viabilidade técnica/jurídica); Poder Concedente pode objetar em 30 dias; **silêncio = aceitação tácita.**
- `contrato.txt`, Cláusula 26.7: ausência de objeção não implica responsabilidade do Poder Concedente nem garantia de remuneração.
- `contrato.txt`, Cláusula 26.8: **compartilhamento de 2% da receita líquida** das Receitas Extraordinárias *"em prol da redução da CONTRAPRESTAÇÃO."*
- `contrato.txt`, Cláusula 26.9: contabilização separada + relatórios.

**3.3 — Receitas Extraordinárias são "aleatórias" — bloqueio de reequilíbrio e de indenização (cruza com Tema 4).**
- `contrato.txt`, Cláusula 26.10: *"A CONCESSIONÁRIA será integralmente responsável pelas projeções de RECEITAS EXTRAORDINÁRIAS, não sendo cabível qualquer tipo de recomposição do equilíbrio econômico-financeiro do CONTRATO em razão da frustração, alteração, não confirmação ou prejuízo decorrente da [...] RECEITAS EXTRAORDINÁRIAS por ela estimadas."*
- `contrato.txt`, Cláusula 26.11: *"[...] as RECEITAS EXTRAORDINÁRIAS são consideradas aleatórias, de modo que a CONCESSIONÁRIA não fará jus ao reequilíbrio econômico-financeiro, tampouco a quaisquer indenizações pelos investimentos realizados."*

**3.4 — Como entram no Plano de Negócios (template).**
- `edital.txt`, Anexo II, MODELO B – Plano de Negócios, "FLUXO DE CAIXA DA CONCESSIONÁRIA", item RECEITA: lista *"RECEITA REQUERIDA TOTAL paga à CONCESSIONÁRIA"* e *"RECEITAS EXTRAORDINÁRIAS"* como linhas de receita. **Nota (do _BRIEFING):** o PN é template (Modelo B); não há valores reais fixados pelo edital.

---

## TEMA 4 — REEQUILÍBRIO ECONÔMICO-FINANCEIRO

**4.1 — Conceito e gatilho: alocação de risco na Matriz (Anexo IX) — remissão expressa.**
- `contrato.txt`, Cláusula 27.1: *"Sempre que atendidas as condições deste CONTRATO, considera-se mantido seu equilíbrio econômico-financeiro."*
- `contrato.txt`, Cláusula 27.2: *"A análise da recomposição do equilíbrio econômico-financeiro restringe-se à neutralização dos efeitos financeiros dos eventos causadores de desequilíbrio contratual [...]"*
- `contrato.txt`, Cláusula 27.3 (**remissão à Matriz de Riscos — Anexo IX**, detalhe é do agente 03): *"Considera-se caracterizado o desequilíbrio econômico-financeiro do CONTRATO quando qualquer das PARTES sofrer os efeitos financeiros, positivos ou negativos, de evento cujo risco não lhe tenha sido alocado nos termos da matriz de riscos constante do Anexo IX ao EDITAL."*
- `contrato.txt`, Cláusula 27.4 (**bloqueio geral**): *"Nenhuma PARTE fará jus à recomposição do equilíbrio econômico-financeiro do CONTRATO caso quaisquer dos riscos por ela assumidos no CONTRATO venham a se materializar."*

**4.2 — Métrica do reequilíbrio: TIR do Plano de Negócios.**
- `contrato.txt`, Cláusula 28.2: *"A apuração do desequilíbrio econômico-financeiro do CONTRATO far-se-á com base na Taxa Interna de Retorno (TIR) do projeto fixada no PLANO DE NEGÓCIOS apresentado na PROPOSTA COMERCIAL."*

**4.3 — Modalidades / mecanismos de recomposição (prerrogativa do Poder Concedente).**
- `contrato.txt`, Cláusula 28.3: *"Cabe ao PODER CONCEDENTE a prerrogativa de escolher as medidas [...] individual ou conjuntamente: (1) alteração do valor da CONTRAPRESTAÇÃO; (2) alteração do prazo da CONCESSÃO ADMINISTRATIVA; (3) alteração das obrigações contratuais da CONCESSIONÁRIA; ou (4) outra forma definida de comum acordo [...]"*
- `contrato.txt`, Cláusula 7.2: o prazo *"também poderá ser prorrogado para fins de readequação do equilíbrio econômico-financeiro [...] devendo ser observado o disposto na Cláusula 27."*

**4.4 — Revisão Extraordinária (Cláusula 28).**
- 28.1: objetiva compensar perdas/ganhos *"em razão da ocorrência dos eventos elencados na subcláusula 27.3"*.
- 28.4: procedimento concluído na Entidade Reguladora *"em prazo não superior a 90 (noventa) dias"* (prorrogável justificadamente).
- 28.5: de ofício ou a pedido da Concessionária. 28.6: instrução do pedido (laudo/perícia, quantitativos no fluxo de caixa, impactos). 28.10: silêncio da outra Parte (≥30 dias) = concordância. 28.11: novos investimentos solicitados pelo Poder Concedente exigem recomposição prévia. 28.15: medidas provisórias da Entidade Reguladora.

**4.5 — Revisão Ordinária (Cláusula 29).**
- 29.1: reavaliação das condições, revisão de indicadores/metas, incorporação de impactos de alterações do **PLANO MUNICIPAL** (*"DE SANEAMENTO BÁSICO"* em 29.1.3 / *"DE RESÍDUOS"* em 29.2 — divergência de nomenclatura: agente 04).
- 29.2: **primeira revisão após 4 anos** da Ordem de Serviço (ou no ano da próxima revisão do Plano Municipal de Resíduos, o que ocorrer primeiro), depois a cada 4 anos.
- 29.4: prazo de conclusão não superior a 90 dias. 29.8: mecanismo de reequilíbrio nos termos da subcláusula 28.3.

**4.6 — Hipóteses específicas que ensejam reequilíbrio (dispersas).**
- `contrato.txt`, Cláusula 6.3: novos investimentos/serviços (subcl. 6.2) só por termo aditivo *"e o pertinente reequilíbrio econômico-financeiro deste CONTRATO."*
- `contrato.txt`, Cláusula 13.3: vícios/defeitos/passivos nos Bens Reversíveis transferidos, se corrigidos pela Concessionária, *"mediante reequilíbrio econômico-financeiro do CONTRATO"*.
- `contrato.txt`, Cláusula 33.11: se a Entidade Reguladora aderir às normas de referência da ANA, as Normas de Regulação serão revistas *"assegurado o equilíbrio econômico-financeiro do CONTRATO."*

**4.7 — Hipóteses que BLOQUEIAM reequilíbrio (além de 27.4 e 26.10/26.11).**
- `contrato.txt`, Cláusula 26.10 e 26.11 (Receitas Extraordinárias aleatórias — ver Tema 3.3).
- `contrato.txt`, Cláusula 42.2 (Advento do termo): *"não caberá indenização à CONCESSIONÁRIA, salvo se o PODER CONCEDENTE solicitar ou autorizar novos investimentos não abarcados em processos de revisão [...]"*

**4.8 — "Fator Incremental".**
- *Registro de ausência:* **não foi localizada** a expressão/instituto "Fator Incremental" no `contrato.txt` nem no `edital.txt`. Existe "Fator de Avaliação (FA)" na fórmula de reajuste (Cl. 25.1) e "Fator K" (critério de julgamento), institutos distintos. **Lacuna declarada expressamente.**

**4.9 — Reajuste (distinto de revisão) — Cláusula 25.**
- `contrato.txt`, Cláusula 25.1, fórmula paramétrica: **CONTRAPRESTAÇÃO REAJUSTADA = ((I1 x 48%) + (I2 x 42%) + (I3 x 10%) + 1) x FA) x PA**, onde I1 = dissídio coletivo da mão de obra do cargo preponderante; I2 = IPCA-IBGE; I3 = variação do preço do Óleo Diesel S10 (ANP, Salto de Pirapora/Sorocaba); FA = Fator de Avaliação (indicadores de desempenho); PA = preço atual da contraprestação. (A escrita da fórmula tem parênteses desbalanceados — apontamento formal = agente 04.)
- Periodicidade: a cada 12 meses; primeiro reajuste 12 meses após a assinatura (25.2). Homologação pela Entidade Reguladora em 15 dias; silêncio autoriza a aplicação (25.6/25.7).
- `contrato.txt`, Cláusula 36 — Compartilhamento de ganhos econômicos de reestruturação financeira (art. 5º da Lei 11.079/2004), implementado por mecanismo de reequilíbrio (redução de contraprestação, *"revisão de tarifas ou receitas"* [sic, 36.6.b], pagamento direto). Remissão expressa à *"matriz de riscos estabelecida neste CONTRATO"* (36.7).

---

## TEMA 5 — BENS REVERSÍVEIS

**5.1 — Definição e lista.**
- `contrato.txt`, Cláusula 1.4 (BENS REVERSÍVEIS): *"são os bens necessários e vinculados à adequada prestação dos SERVIÇOS, relacionados no Anexo VI do EDITAL, bem como aqueles que venham a ser adquiridos ou implantados pela CONCESSIONÁRIA durante a vigência [...] os quais reverterão em favor do PODER CONCEDENTE após o término [...], estando excluídos os bens de uso administrativo e/ou aqueles cuja reversibilidade não seja possível ou adequada e conveniente ao MUNICÍPIO;"* (Cláusula 1.5 define BENS NÃO REVERSÍVEIS.)
- `edital.txt`, ANEXO VI — "INDICAÇÃO DE BENS REVERSÍVEIS" (linha ~14225): caracteriza os bens existentes; lista expressamente o **Aterro Sanitário Municipal** (gleba de **118.056 m²**, acesso pela SP-264 / estrada SLR-166); inclui *"(i) Todas as OBRAS, equipamentos, máquinas, aparelhos, acessórios [...] diretamente relacionados com a prestação dos SERVIÇOS"* e *"(ii) Os bens adquiridos ou construídos pela CONCESSIONÁRIA [...] ao longo de todo o prazo da CONCESSÃO."*
  - **Registro:** o Anexo VI **não traz inventário individualizado/quantitativo** dos bens existentes além do aterro (lista genérica). Vistoria conjunta posterior gerará laudo do estado dos bens. (Detalhamento/lacuna = agente 04.)

**5.2 — Transferência inicial e estado dos bens.**
- `contrato.txt`, Cláusula 13.1/13.2: bens transferidos *"inteiramente livres e desembaraçados de quaisquer ônus, encargos ou passivos [...] em condições normais de operação"*; Poder Concedente declara inexistência de ônus/passivos.
- `contrato.txt`, Cláusula 13.3: condições divergentes/vícios/passivos serão submetidos à Entidade Reguladora para definir se a correção cabe ao Poder Concedente ou à Concessionária (neste caso com reequilíbrio).
- `edital.txt`, Anexo VI: vistoria conjunta posterior e elaboração de laudo do estado dos bens efetivamente transferidos; transferência via *"Termo de Recebimento do ATERRO SANITÁRIO"* (Cl. 12.1.c, 12.3.a do contrato; Anexo XI – Minuta do Termo).

**5.3 — Inventário e manutenção pela Concessionária.**
- `contrato.txt`, Cláusula 13.7: *"É de integral responsabilidade da CONCESSIONÁRIA a manutenção do inventário dos BENS REVERSÍVEIS em condições atuais [...]"*
- `contrato.txt`, Cláusula 13.8: registro contábil distinto de bens reversíveis/não reversíveis *"observadas as normas contábeis vigentes."*
- `edital.txt`, Anexo VI: a Concessionária elabora **anualmente** a Relação dos Bens Reversíveis (cobrindo aquisições do ano anterior), sujeita à aprovação do Poder Concedente, que pode incluir/retirar bens.
- `contrato.txt`, Cláusula 13.5/13.11: dever de manter/reformar/substituir; devolução em estado normal de utilização *"excetuado o desgaste proveniente de seu normal funcionamento."*
- `contrato.txt`, Cláusula 13.9 / `edital.txt` Anexo VI: vedada alienação/oneração, salvo substituição por outros de condição idêntica ou superior, mediante autorização do Poder Concedente.

**5.4 — Critério de depreciação / amortização.**
- *Registro de ausência:* **não há, no contrato nem no edital, critério/método de depreciação definido** (taxas, vida útil contábil por classe de bem). Há remissões indiretas:
  - `contrato.txt`, Cláusula 20.1.14 (Entidade Reguladora): *"auditar e certificar os investimentos realizados [...] os valores amortizados, a depreciação e os respectivos saldos, conforme previsto no artigo 42, § 2º, da Lei federal nº 11.445/2007;"*
  - `edital.txt`, Anexo VI: *"Os gastos com manutenção, conservação ou renovação dos BENS REVERSÍVEIS que importem aumento do período de amortização desses bens devem ser previamente aprovados pelo PODER CONCEDENTE."* **Lacuna metodológica declarada.**

**5.5 — Indenização na extinção (por hipótese).**
- **Regra geral de reversão e indenização** — `contrato.txt`, Cláusula 41.2/41.3: extinta a concessão, opera-se reversão dos bens (Cl. 48) e retomada, *"pagando-se à CONCESSIONÁRIA a respectiva indenização de acordo com a hipótese de extinção"*; indenização sobre investimentos *"auditados e certificados pela ENTIDADE REGULADORA"* (subcl. 20.1.14), calculada por consultoria de lista tríplice (custos pela Concessionária).
- `contrato.txt`, Cláusula 41.4: *"A metodologia de cálculo da indenização [...] será definida conforme normas de regulação da Agência Nacional de Águas e Saneamento ou de decreto eventualmente editado pelo Poder Executivo federal."* (Metodologia remetida a norma externa futura — registrar.)
- **Advento do termo** — `contrato.txt`, Cláusula 42.2: *"não caberá indenização à CONCESSIONÁRIA, salvo se o PODER CONCEDENTE solicitar ou autorizar novos investimentos não abarcados em processos de revisão ordinária ou extraordinária [...]"* Pagamento em até 6 parcelas (42.7).
- **Encampação** — `contrato.txt`, Cláusula 43 (art. 37 da Lei 8.987/95): indenização **prévia** à reversão, englobando: investimentos não depreciados/amortizados corrigidos; custos de rescisão de contratos com terceiros; custos de rescisão/vencimento antecipado de financiamentos; indenizações de reequilíbrio já apuradas; **lucros cessantes** *"por meio da aplicação da Taxa Interna de Retorno (TIR) do projeto fixada no PLANO DE NEGÓCIOS"* (43.2.5); custos de desmobilização.
- **Caducidade** — `contrato.txt`, Cláusula 44.7: indenização considera investimentos não depreciados/amortizados e indenizações de reequilíbrio já apuradas, corrigidos; descontados prejuízos, multas e seguros (44.8); **sem lucros cessantes** (diferentemente da encampação). Pagamento em até 6 parcelas (44.12).
- **Rescisão** (por inadimplemento do Poder Concedente) — `contrato.txt`, Cláusula 45.1/45.4: cálculo conforme subcl. "40.2" (remissão cruzada provavelmente equivocada → 41.2; agente 04). Pagamento em até 6 parcelas (45.5).

**5.6 — Reversão (Cláusula 48) e desmobilização.**
- `contrato.txt`, Cláusula 48.2: entrega *"inteiramente livres e desembaraçados de quaisquer ônus ou encargos [...] em condições normais de operacionalidade [...] sem prejuízo do normal desgaste"*; 48.3: programa de desmobilização operacional com **12 meses** de antecedência; 48.4: comissão de recebimento (≥3 membros) com acompanhamento da Entidade Reguladora; 48.6: treinamento de pessoal nos **6 meses** finais.

**5.7 — Vida útil do aterro.**
- `contrato.txt`, Cláusula 14.5: *"Após o advento do termo contratual, o ATERRO SANITÁRIO, consideradas as áreas eventualmente incorporadas no curso da CONCESSÃO, será revertido ao PODER CONCEDENTE, devendo possuir pelo menos 5 (cinco) anos de vida útil contados da data do advento do termo contratual."*
- `contrato.txt`, Cláusula 14.6: 6 meses antes do termo, entregar *"projeto sobre a operação, manutenção, conservação e monitoramento do ATERRO SANITÁRIO nos próximos 5 (cinco) anos de vida útil após a data do advento do termo contratual."*
- `contrato.txt`, Cláusula 14.1.6: dever de adotar técnicas *"para o melhor aproveitamento e o máximo de extensão da vida útil do ATERRO SANITÁRIO"*; 14.2/14.3: expansão de área/capacidade (com desapropriação — Cl. 34); 14.4: obras e custos por conta da Concessionária.
- `edital.txt`, Caderno (linhas ~9144 a ~9233): estimativa de vida útil do aterro **≈ 30,79 anos (369 meses)**, expressamente *"de caráter exclusivamente referencial"*, *"não constitui garantia física imutável"*.
- `contrato.txt`, Cláusula 1.3 (ATERRO SANITÁRIO): aterro existente *"localizado nas coordenadas geográficas [•]"* (campo em branco — agente 04), *"cuja área poderá ser expandida no curso da CONCESSÃO."*

**5.8 — Cessão de Propriedade Intelectual (PI).**
- `contrato.txt`, Cláusula 15.11: *"A propriedade intelectual sobre todos os projetos e documentos relacionados às especificações técnicas dos SERVIÇOS, inclusive das obras necessárias, concebidos pela CONCESSIONÁRIA para a execução deste CONTRATO, é do PODER CONCEDENTE, sendo vedada sua utilização pela CONCESSIONÁRIA para outros fins não previstos neste CONTRATO."*
- `contrato.txt`, Cláusula 15.10: entrega de croquis, as built, manuais e demais documentos ao final de cada obra.

---

## TEMA 6 — ENTIDADE REGULADORA

**6.1 — Definição: divergência edital × contrato.**
- `edital.txt`, Definições (linha ~534): *"ENTIDADE REGULADORA: é a **Agência Reguladora de Serviços Públicos do Estado de São Paulo (ARSESP)**, entidade responsável pela regulação e fiscalização dos SERVIÇOS [...]"* (nome definido).
- `contrato.txt`, Cláusula 1.15: *"ENTIDADE REGULADORA: é a **[•]**, entidade responsável pela regulação e fiscalização dos SERVIÇOS [...], cuja delegação foi autorizada pela Lei Municipal n° **[•]** e pelo convênio firmado com o MUNICÍPIO em **[•]**;"* (**campo em aberto** no contrato + lei e data do convênio em branco).
- `contrato.txt`, Cláusula 33.1.1: *"A regulação e a fiscalização [...] serão exercidas pela **[NOME DA ENTIDADE REGULADORA]**, nos termos do instrumento jurídico de delegação firmado com o PODER CONCEDENTE [...]"* (também em branco — apontamento formal/contradição = agente 04; aqui só se registra).

**6.2 — Convênio / delegação.**
- `contrato.txt`, Cláusula 1.15 e 33.1.1: a atuação depende de *"convênio firmado com o MUNICÍPIO"* / *"instrumento jurídico de delegação"* (Lei Municipal n.º `[•]` e data `[•]` em branco).
- `contrato.txt`, Cláusula 1.22 (NORMAS DE REGULAÇÃO): inclui *"as normas de referência instituídas pela Agência Nacional de Águas e Saneamento Básico – ANA, se adotadas pela ENTIDADE REGULADORA [...]"*

**6.3 — Competências atribuídas (Cláusula 20).**
- `contrato.txt`, Cláusula 20.1, incisos 1 a 16, incluindo: regular e fiscalizar; **editar Normas de Regulação** (em conflito com o contrato, prevalece o contrato — 20.1.2); aplicar penalidades; **promover as revisões ordinária e extraordinária** (20.1.5); garantir reequilíbrio (20.1.6); assinar termos aditivos como interveniente-anuente (20.1.7); **homologar o reajuste** da contraprestação (20.1.8); avaliar metas/indicadores; emitir parecer em intervenção e em extinção antecipada e realizar levantamentos de indenização (20.1.10/20.1.11); **vistoriar periodicamente os bens reversíveis** (20.1.12); **auditar e certificar investimentos, amortização e depreciação** (art. 42, §2º, Lei 11.445/2007 — 20.1.14); decidir recursos (20.1.15).

**6.4 — Regulação, fiscalização e taxa de regulação.**
- `contrato.txt`, Cláusula 33: princípios (independência decisória, autonomia, transparência, tecnicidade); livre acesso a bens/dados; relatórios anuais; **taxa de regulação** em percentual em branco — *"a CONCESSIONÁRIA deverá pagar, mensalmente, à ENTIDADE REGULADORA, [•]% ([•]) de [•] referente ao exercício anterior [...]"* (33.10).
- `edital.txt`, item 234: fixa a taxa de regulação em *"0,5% (meio por cento) do faturamento anual diretamente obtido com a prestação dos serviços [...] subtraídos os valores dos tributos incidentes sobre o faturamento"* (divergência com o contrato, que mantém `[•]%` — registro; tratamento formal = agente 04).
- `contrato.txt`, Cláusula 33.11: adesão futura às normas de referência da ANA (Lei 14.026/2020), assegurado o equilíbrio.

---

## TEMA 7 — PRAZO E FASES

**7.1 — Prazo total.**
- `contrato.txt`, Cláusula 7.1: *"O prazo de vigência da CONCESSÃO ADMINISTRATIVA é de **30 (trinta) anos** contados a partir da data de emissão da ORDEM DE SERVIÇO, podendo ser prorrogado por iniciativa do PODER CONCEDENTE, desde que devidamente justificado e observado o limite previsto na legislação aplicável, mediante a celebração de termo aditivo."*
- `edital.txt`, item 137.f: *"deverá ser considerado o prazo de 30 (trinta) anos para a vigência da CONCESSÃO ADMINISTRATIVA;"* (e Anexo II, MODELO B: planilhas por 30 anos).
- `contrato.txt`, Cláusula 7.1.1 (prorrogação a pedido da Concessionária — comprovação de regularidade + plano de investimento); 7.2 (prorrogação para reequilíbrio); 7.3 (novos investimentos amortizados no novo prazo).

**7.2 — Fases: Período de Transição → Ordem de Serviço → operação.**
- `contrato.txt`, Cláusula 1.26 (PERÍODO DE TRANSIÇÃO): da assinatura do contrato até a emissão da Ordem de Serviço.
- `contrato.txt`, Cláusula 12.1: *"A partir da data de assinatura do CONTRATO, terá início o PERÍODO DE TRANSIÇÃO [...], com duração de **120 (cento e vinte) dias** [...]"* — obrigações do Poder Concedente (transferência dos bens, contrato de vinculação de receitas, garantia de adimplemento) e da Concessionária (mobilização, preposto, Plano de Implantação, seguros). 12.2: prorrogável por igual prazo por acordo.
- `contrato.txt`, Cláusula 12.3/12.4: emitida a **ORDEM DE SERVIÇO**, o contrato torna-se plenamente eficaz e a Concessionária inicia os serviços, fazendo jus à contraprestação.
- `contrato.txt`, Cláusula 12.5: **Plano de Implantação, Operação e Manutenção** a ser submetido em até **120 dias** da assinatura (manifestação do Poder Concedente em 15 dias — 12.6); 12.8: relatórios semestrais.
  - **Registro:** o contrato não rotula expressamente uma "fase pré-operacional"/"fase operacional" autônomas; a estrutura temporal é Período de Transição (120 dias) → Ordem de Serviço → 30 anos de operação. Cronograma de investimentos detalhado fica no Plano de Implantação e na Proposta Técnica/Caderno (agente 05).

**7.3 — Cronograma de investimentos.**
- `contrato.txt`, Cláusula 15.1: a Concessionária elabora projetos básico e executivo das obras (inclusive expansão do aterro), conforme Termo de Referência, Proposta Técnica e Plano de Implantação. 15.6: obras podem iniciar a partir da entrega do projeto.
- `edital.txt`, Anexo II, MODELO B – Quadro Q2 "Projeção de Investimentos" (template a preencher pelo licitante, 30 anos). **Não há cronograma físico-financeiro de investimentos fixado pelo edital** no que diz respeito ao Tema 1 (escopo técnico/CAPEX detalhado = agente 05).

---

## NOTAS DE FRONTEIRA / LACUNAS REGISTRADAS (sem análise — para 04/03 conforme o caso)
- **Campos em branco `[•]`** relevantes para esta extração: tabela de CONTRAPRESTAÇÃO mensal (Cl. 23.1); nome da Entidade Reguladora, Lei e data do convênio (Cl. 1.15 e 33.1.1); percentual e base da taxa de regulação (Cl. 33.10); coordenadas do aterro (Cl. 1.3); Agente Depositário (Cl. 1.1); data-base da proposta. → **detecção formal é do agente 04.**
- **Divergências entre documentos** (edital nomeia ARSESP e fixa taxa de 0,5%; contrato mantém `[•]`): registradas; consolidação/efeito = agentes 04 e Fase 2.
- **"Fator Incremental":** instituto não localizado nos textos (lacuna declarada).
- **Matriz de Riscos (Anexo IX)** e **cofaturamento/TMRSU operacional:** apenas remissões aqui (Cl. 27.3, 36.7, 22.1.1); conteúdo é do **agente 03.**
- **Biogás/biometano/CDR/créditos de carbono:** não nominados na Cl. 26.3; cruzamento com Caderno de Encargos = **agente 05.**

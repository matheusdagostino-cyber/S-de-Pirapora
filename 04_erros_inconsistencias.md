# AGENTE 04 — ERROS E INCONSISTÊNCIAS
**Concorrência Presencial nº 001/2026 — Concessão Administrativa de Manejo de RSU — Salto de Pirapora/SP**

> **Perspectiva:** não declarada pelo solicitante → assumida a do **LICITANTE / PROPONENTE** (premissa registrada conforme `CLAUDE.md` e `_BRIEFING.md`). Este relatório apenas **detecta** o defeito formal; a consequência jurídica é dos agentes de domínio (01, 02, 03, 05) e da consolidação (06).
>
> **Fontes varridas integralmente:** `edital.txt` (16.714 linhas — corpo + Anexos I a XI, inclusive Caderno de Encargos, Indicadores, Diretrizes Ambientais, Matriz de Riscos), `contrato.txt` (6.941 linhas — Anexo VIII, Minuta do Contrato), `etp.txt` (817 linhas — Estudo Técnico Preliminar).
>
> **Nota metodológica:** os `.txt` derivam de OCR; quebras de página e números de página soltos ("17", "22", "46") aparecem no meio de itens e geram falsos "saltos" de numeração. Toda numeração suspeita foi conferida por leitura do entorno; só foram reportadas as descontinuidades **reais**. Não foi localizada nenhuma ocorrência literal de "Erro! Fonte de referência não encontrada".

---

## RESUMO QUANTITATIVO POR CATEGORIA
| Categoria | Achados |
|---|---|
| 1. Referências cruzadas quebradas | 6 |
| 2. Erros de redação (fórmula, numeração, gramática) | 5 |
| 3. Campos não preenchidos (`[•]`/`[●]`/`[___]`) | blocos catalogados abaixo (≈ dezenas de marcadores; 3 críticos no corpo do Contrato) |
| 4. Inconsistências entre documentos | 5 |
| 5. Inconsistências internas | 3 |
| 6. Lacunas | 4 |

---

## 1. REFERÊNCIAS CRUZADAS QUEBRADAS (ordenado por gravidade)

### 1.1 — Edital: cadeia de remissões "item 119.a/d/f" aponta para item que na verdade é o 118 (qualificação econômico-financeira)
- **Documento/localização:** `edital.txt`. Cabeçalho real da qualificação econômico-financeira = **item 118** (linha 3165: "A qualificação econômico-financeira da LICITANTE será comprovada mediante a apresentação de: a) ... f) ..."). Porém o item seguinte numerado **"119."** (linha 3317) já começa com "Para fins do **item 119.f)**", e o item 120 (linha 3349) também invoca "item 119.f)".
- **Remissões afetadas (todas dizem "119" mas o conteúdo está no 118):** linha 3203 ("item 119.a)"), 3278 ("item 119.a)"), 3411 ("item 119.f) e o capital social previsto no item 119.d)"), 3460 ("item 119.a)").
- **Natureza:** referência cruzada quebrada sistemática — provável renumeração do bloco (118) sem atualizar as remissões internas (mantidas em 119). Os índices financeiros (ILG, ISG, IE, ISG, IA), o capital social mínimo e os documentos contábeis estão todos sob o **item 118**, não 119.
- **Correção:** uniformizar toda a cadeia para "item 118.a)/.d)/.f)" (ou renumerar o cabeçalho de qualificação para 119 e ajustar os subitens), conferindo cada alínea.

### 1.2 — Contrato: "empresa de consultoria especializada de que trata a subcláusula 38.3" — subcláusula inexistente
- **Documento/localização:** `contrato.txt`, linhas 5662, 5888 e 6437 (também ecoada na 6502).
- **Transcrição (l. 5660-5662):** "Na hipótese da subcláusula 39.2, a empresa de consultoria especializada **de que trata a subcláusula 38.3** procederá, nos 180 (cento e oitenta) dias que antecederem o termo final do CONTRATO, aos levantamentos e avaliações..."
- **Natureza:** referência quebrada. A **Cláusula 38** é "PROCEDIMENTO DE APLICAÇÃO DE PENALIDADES" e **não possui subcláusula 3** (sua numeração começa em "5." — ver achado 2.3); tampouco menciona "empresa de consultoria especializada". O instituto da consultoria especializada para cálculo de indenização nunca é efetivamente criado/disciplinado no Contrato — só é remetido.
- **Correção:** criar a subcláusula que institui a empresa de consultoria especializada (escolha, custeio, prazo) e corrigir as três remissões para o dispositivo correto.

### 1.3 — Contrato: remissão à "Cláusula 48" para o mecanismo de solução de controvérsias, que está na Cláusula 49
- **Documento/localização:** `contrato.txt`. A **Cláusula 49** é "MECANISMO DE SOLUÇÃO DE CONTROVÉRSIAS E ARBITRAGEM" (linha 6591); a **Cláusula 48** é "REVERSÃO DOS BENS REVERSÍVEIS" (linha 6509).
- **Remissões erradas a "Cláusula 48" querendo dizer 49:** linha 3577 ("mecanismo de solução de controvérsias previstos na Cláusula 48"), 5155 ("controvérsias previsto na Cláusula 48"), 6351 ("controvérsias previsto na Cláusula 48"), 6589 ("previsto na Cláusula 48"). (As demais remissões a "Cláusula 49" — l. 3695, 4342, 5362, 5690, 5756, 5916, 5949, 6186, 6220, 6399, 6403, 6507 — estão corretas.)
- **Natureza:** referência cruzada quebrada (resíduo de ordenação anterior das cláusulas finais).
- **Correção:** trocar "Cláusula 48" por "Cláusula 49" nas quatro ocorrências indicadas.

### 1.4 — Contrato: remissões à "subcláusula 39.x" (Causas Justificadoras da Inexecução) no contexto de extinção/indenização
- **Documento/localização:** `contrato.txt`, Cláusula 42 (ADVENTO DO TERMO), linhas 5649 ("subcláusula 39.1.1") e 5660 ("Na hipótese da subcláusula 39.2"); e Cláusula 41/42 que tratam de indenização.
- **Natureza:** a **Cláusula 39** é "CAUSAS JUSTIFICADORAS DA INEXECUÇÃO" (força maior/caso fortuito — linha 5157), tema estranho à sub-rogação de contratos e ao cálculo de indenização por advento do termo. As remissões parecem apontar a dispositivos de outra cláusula (extinção/indenização), revelando renumeração não propagada.
- **Correção:** revisar e reapontar as remissões "39.1.1" e "39.2" para os dispositivos efetivamente pretendidos.

### 1.5 — Contrato (Cláusula 49 – Arbitragem): remissões a "subcláusula 46.4" e "subcláusula 46.15" — Cláusula 46 é "ANULAÇÃO", não arbitragem
- **Documento/localização:** `contrato.txt`. Cláusula 46 = "ANULAÇÃO DA CONCESSÃO ADMINISTRATIVA" (linha 6275). A Cláusula 49 (arbitragem) contém:
  - linha 6643: "...no prazo de até 10 (dez) dias contados do recebimento da **notificação de arbitragem de que trata a subcláusula 46.4**." (a notificação de arbitragem está na própria Cláusula 49, não na 46.)
  - linha 6719: "...conhecer ações cujo objeto, **nos termos da subcláusula 46.15**, não possa ser discutido por meio de arbitragem..." (a definição de matérias não arbitráveis também é da Cláusula 49.)
- **Natureza:** referência cruzada quebrada (deveriam apontar a subcláusulas da própria Cláusula 49).
- **Correção:** reapontar "46.4" e "46.15" para as subcláusulas corretas da Cláusula 49.

### 1.6 — Contrato: remissão a "subcláusula 36.1" para penalidades, que estão na Cláusula 37
- **Documento/localização:** `contrato.txt`, linha 4975: "Sem prejuízo das penalidades previstas na **subcláusula 36.1** ...".
- **Natureza:** o dispositivo está inserido na Cláusula 37 ("INFRAÇÕES E SANÇÕES APLICADAS PELA ENTIDADE..."), e a **Cláusula 36** é "DO COMPARTILHAMENTO DE GANHOS ECONÔMICOS" (linha 4543) — não trata de penalidades. A remissão "36.1" provavelmente deveria ser à própria Cláusula 37.
- **Correção:** corrigir para "subcláusula 37.1" (ou ao item de penalidades pretendido).

---

## 2. ERROS DE REDAÇÃO (ordenado por gravidade)

### 2.1 — Contrato (Cláusula 25 – Reajuste): fórmula paramétrica com parênteses desbalanceados
- **Documento/localização:** `contrato.txt`, linhas 3107-3108.
- **Transcrição literal:** "CONTRAPRESTAÇÃO REAJUSTADA = **((I1 x 48%) + (I2 x 42%) + (I3 X 10%) + 1) x FA) x PA**"
- **Natureza:** erro de redação que altera o sentido jurídico/matemático. Há **3 parênteses de abertura "(" e 4 de fechamento ")"**; o fechamento "...+ 1) x FA)" encerra um parêntese nunca aberto, tornando o agrupamento ambíguo (não fica claro se FA multiplica todo o bloco indexado ou apenas a parcela final). Subsidiariamente, "I3 **X** 10%" usa "X" maiúsculo onde os demais fatores usam "x" minúsculo. Os pesos somam corretamente (48% + 42% + 10% = 100%).
- **Correção:** redigir de forma inequívoca, p.ex.: `CONTRAPRESTAÇÃO REAJUSTADA = [ ( (I1 × 48%) + (I2 × 42%) + (I3 × 10%) + 1 ) × FA ] × PA`.

### 2.2 — Edital (item 118.f.iv): fórmula do Índice de Solvência Geral sem parênteses no denominador
- **Documento/localização:** `edital.txt`, linha 3315.
- **Transcrição:** "ISG = Ativo Total**/** Passivo Circulante + Passivo Não Circulante"
- **Natureza:** erro de redação de fórmula. Sem parênteses, lê-se (Ativo Total ÷ Passivo Circulante) + Passivo Não Circulante, quando o índice de solvência geral é Ativo Total ÷ (Passivo Circulante + Passivo Não Circulante). Compare-se com o ILG (linha 3284), que **usa** parênteses no denominador. Afeta diretamente a aferição da habilitação econômico-financeira.
- **Correção:** "ISG = Ativo Total / (Passivo Circulante + Passivo Não Circulante)".

### 2.3 — Contrato (Cláusula 38): numeração das subcláusulas começa em "5." (faltam subcláusulas 1 a 4)
- **Documento/localização:** `contrato.txt`, linhas 5041-5043. Após o título "CLÁUSULA 38 – PROCEDIMENTO DE APLICAÇÃO DE PENALIDADES", a primeira subcláusula é numerada "**5.**" ("O processo de aplicação de penalidades previstas na Cláusula 37 terá início com a lavratura..."), seguindo 6, 7, 8...
- **Natureza:** erro de numeração (subcláusulas iniciais puladas/ausentes). Agrava a referência quebrada do achado 1.2 ("subcláusula 38.3" inexistente).
- **Correção:** renumerar a partir de "1." ou recuperar as subcláusulas 1-4 omitidas.

### 2.4 — Contrato (Cláusula 4 – Interpretação): subcláusula "Em quarto lugar" repetida; falta "quinto lugar"
- **Documento/localização:** `contrato.txt`, linhas 558-563.
- **Transcrição:** item 4 — "Em **quarto** lugar, as disposições da PROPOSTA COMERCIAL e da PROPOSTA TÉCNICA;" / item 5 — "Em **quarto** lugar, as NORMAS DE REGULAÇÃO."
- **Natureza:** erro de redação/ordinal duplicado em cláusula de **ordem de prevalência**. Cria empate hierárquico entre Proposta Comercial/Técnica e Normas de Regulação — defeito de sentido jurídico relevante (qual prevalece em conflito?).
- **Correção:** "Em **quinto** lugar, as NORMAS DE REGULAÇÃO."

### 2.5 — Contrato (Cláusula 25): subcláusula com hierarquia trocada ("2." seguida de "1." e depois "3.")
- **Documento/localização:** `contrato.txt`, linhas 3143-3155. Subcláusula "2." (l. 3143) é seguida de uma "1." (l. 3148, sobre prazo de 20 dias) e depois "3." (l. 3152) no mesmo nível do "2.".
- **Natureza:** erro de numeração/aninhamento (a "1." parece dever ser subitem "2.1", não item autônomo).
- **Correção:** rebaixar a "1." para subitem da subcláusula 2 ou renumerar a sequência.

---

## 3. CAMPOS NÃO PREENCHIDOS (`[•]`, `[●]`, `[___]`)

> Catalogados por bloco. A maioria dos `[•]` em `edital.txt` integra **modelos de cartas/declarações do Anexo I e Anexo II** e o **Termo de Recebimento do Aterro (Anexo XI)** — preenchimento próprio do licitante/momento da assinatura. Listados em bloco; destacados à parte os campos do **corpo do Edital** e da **Minuta de Contrato** cuja indefinição recai sobre cláusulas estruturais.

### 3.1 — Corpo do Edital
- `edital.txt` l. 3861 — "aviso publicado no site **[•]**" (canal oficial de publicação não definido).

### 3.2 — Minuta de Contrato (corpo) — `contrato.txt`
- l. 53-54 — "CONCORRÊNCIA PÚBLICA N° **[•]**" / "CONTRATO N° **[•]**".
- l. 63-86 — preâmbulo: data, CNPJ do Município, nome do Prefeito, qualificação da CONCESSIONÁRIA e da ENTIDADE REGULADORA interveniente (todos `[•]`).
- l. 94-95 — **definição 1 (AGENTE DEPOSITÁRIO):** "é a **[●]**, instituição financeira com sede na **[●]**, inscrita no CNPJ sob nº **[●]**".
- l. 123 — definição 3 (ATERRO SANITÁRIO): "coordenadas geográficas **[•]**".
- l. 214-217 — **definição 15 (ENTIDADE REGULADORA):** "é a **[•]**, ... cuja delegação foi autorizada pela Lei Municipal n° **[•]** e pelo convênio firmado com o MUNICÍPIO em **[•]**". (Regulador não identificado.)
- l. 264 — definição 19 (LICITAÇÃO): "Concorrência Pública nº **[•]**".
- l. 716-717 — **Cláusula 8 (VALOR DA CONTRATAÇÃO):** "R$ **[• valor a ser calculado de acordo com a proposta vencedora]**".
- l. 738 — **Cláusula 9.3 (capital subscrito mínimo):** "R$ **[• valor a ser calculado de acordo com a proposta vencedora]**".
- l. 2679-2759 — **Cláusula 23 (CONTRAPRESTAÇÃO):** tabela de contraprestação mensal dos 30 anos toda preenchida com **[•]** (30 linhas em branco).
- l. 4070 — Cláusula 32 (Garantia de Execução): "R$ **[•] ([•])**, equivalente a 5%...".
- l. 4364-4369 — Cláusula 33 (taxa de regulação/fiscalização): "**[•]%** (**[•]**) de **[•]** referente ao exercício anterior ... até o **[•]** dia do mês".
- l. 6782-6786 — Cláusula 50 (Comunicações): endereços de PODER CONCEDENTE, CONCESSIONÁRIA e ENTIDADE REGULADORA = **[•]**.

### 3.3 — Anexo II / Plano de Negócios (Modelo B) — `edital.txt`
- l. 7229 — "na data base de **[●]** de **[●]**, ou seja, sem inflação."
- l. 6915 — Carta de Proposta Comercial (Modelo A): "Fator K na ordem de **[•]**" (campo do licitante).

### 3.4 — Anexo I (modelos de cartas/declarações) — `edital.txt`
- Marcadores `[•]` em série nas linhas 5269, 5371, 5381, 5389, 5440, 5503, 5513, 5570, 5621, 5707, 5775, 5843, 5903, 5959, 6014, 6030, 6089, 6140, 6154, 6197-6223, 6268, 6288, 6343, 6403, 6473-6495, 6565, 6879, 6885 (referências ao nº do Edital, dados do banco fiador, valores de fiança/seguro, datas) — campos de preenchimento pelo licitante/garantidor.

### 3.5 — Anexo XI (Termo de Recebimento do Aterro) — `edital.txt`
- Marcadores `[•]` nas linhas 16525-16691 (data, CNPJ do Município, nome do Prefeito, qualificação da Concessionária e da interveniente, coordenadas geográficas, nº do Contrato/Edital, data de vistoria).

---

## 4. INCONSISTÊNCIAS ENTRE DOCUMENTOS (ordenado por gravidade)

### 4.1 — Modalidade da licitação: "Concorrência Presencial" (Edital) × "Concorrência Pública" (Contrato)
- **Edital:** define LICITAÇÃO como "**Concorrência Presencial** nº 001/2026" (`edital.txt` l. 591; ver tb. l. 183, 255 — há até Seção justificando "A adoção da forma presencial").
- **Contrato:** cabeçalho "**CONCORRÊNCIA PÚBLICA** N° [•]" (`contrato.txt` l. 53) e definição 19 "LICITAÇÃO: é a **Concorrência Pública** nº [•]" (l. 264).
- **Natureza:** discrepância terminológica sobre a própria modalidade entre Edital e Contrato.
- **Correção:** uniformizar a designação no Contrato para "Concorrência Presencial nº 001/2026".

### 4.2 — Forma societária da Concessionária: "sociedade anônima" × "[limitada/anônima]"
- **Edital, item 202** (`edital.txt` l. 4543): a CONCESSIONÁRIA "assumirá ... a forma de **sociedade anônima**".
- **Contrato, preâmbulo** (`contrato.txt` l. 68): "[•], **sociedade anônima**" (coerente).
- **Anexo XI – Termo de Recebimento do Aterro** (`edital.txt` l. 16535): "[•], **sociedade [limitada/anônima]**" — campo de escolha aberto, admitindo limitada.
- **Natureza:** contradição/indefinição entre a exigência de SPE sob forma de S.A. (item 202) e o modelo do Anexo XI, que mantém a alternativa "limitada".
- **Correção:** fixar "sociedade anônima" no Anexo XI, eliminando a opção "limitada".

### 4.3 — Receitas: "RECEITAS EXTRAORDINÁRIAS" (Contrato/corpo do Edital) × "receitas acessórias" / "tarifas" (Caderno de Encargos/ETP)
- **Contrato** define e usa "**RECEITAS EXTRAORDINÁRIAS**" (definição 33, Cláusula 26).
- **Caderno de Encargos / Diretrizes (Edital):** "Previsão de **receitas acessórias**" (l. 11246) e seção "**IDENTIFICAÇÃO DAS RECEITAS ACESSÓRIAS**" (l. 11589); ainda "modicidade das **tarifas**" (l. 11613), embora o modelo seja de **contraprestação pública sem tarifa ao usuário** (l. 11240-11242: "não havendo cobrança de tarifa ou qualquer tipo de pagamento direto pelos usuários").
- **Natureza:** discrepância terminológica entre documentos para o mesmo instituto (receitas alternativas/acessórias/extraordinárias) e uso impróprio de "tarifa/modicidade tarifária" em concessão administrativa remunerada por contraprestação.
- **Correção:** padronizar para "RECEITAS EXTRAORDINÁRIAS" (termo definido) e substituir "modicidade das tarifas" por "modicidade da CONTRAPRESTAÇÃO".

### 4.4 — Valor do contrato e capital social mínimo: percentual de 10% não fecha
- **Edital, item 13** (`edital.txt` l. 973): valor estimado do CONTRATO = **R$ 558.596.000,00**.
- **Edital, item 118.d** (l. 3248-3254): capital social mínimo = **R$ 56.613.517,80**, declarado como "correspondente a **10% (dez por cento) do valor estimado do CONTRATO previsto no item 13**".
- **Natureza:** inconsistência numérica entre documentos. 10% de R$ 558.596.000,00 = **R$ 55.859.600,00**, e não R$ 56.613.517,80 (este corresponde a 10% de ≈ R$ 566.135.178,00). Os dois números não se conciliam.
- **Correção:** reconciliar o valor estimado do CONTRATO (item 13) e o capital social mínimo (item 118.d) de modo que a relação de 10% feche; corrigir o algarismo/extenso do que estiver desatualizado.

### 4.5 — Garantia de adimplemento referida sob duas designações
- Ver achado 5.1 (também é inconsistência interna ao Contrato). A definição 16 ("GARANTIA DE ADIMPLEMENTO DA PPP") é o termo correto; "GARANTIA DE PAGAMENTO DA PPP" aparece sem definição.

---

## 5. INCONSISTÊNCIAS INTERNAS (mesmo documento)

### 5.1 — Contrato: "GARANTIA DE PAGAMENTO DA PPP" (sem definição) × "GARANTIA DE ADIMPLEMENTO DA PPP" (termo definido)
- **Documento/localização:** `contrato.txt`. Termo **definido** = "GARANTIA DE ADIMPLEMENTO DA PPP" (definição 16, l. 219; usado nas l. 102, 287, 2862, 2865, 2875). Aparece, porém, "GARANTIA DE **PAGAMENTO** DA PPP" nas l. 343 (dentro da própria definição 32 de RECEITAS) e 2827.
- **Natureza:** termo grafado em maiúsculas (sugere termo definido) **sem definição correspondente** no rol da Cláusula 1 — uso de variante não definida do mesmo instituto.
- **Correção:** substituir as duas ocorrências por "GARANTIA DE ADIMPLEMENTO DA PPP".

### 5.2 — Contrato: "CONTROLE SOCIETÁRIO" usado uma vez, sendo o termo definido "CONTROLE"
- **Documento/localização:** `contrato.txt` l. 793: "se houver a assunção do **CONTROLE SOCIETÁRIO** da CONCESSIONÁRIA pelas entidades financiadoras". O termo definido (definição 13, l. 202) é "**CONTROLE**".
- **Natureza:** uso de expressão em maiúsculas divergente do termo definido.
- **Correção:** uniformizar para "CONTROLE" (ou definir "CONTROLE SOCIETÁRIO").

### 5.3 — Edital: dois itens consecutivos numerados "119" (duplicidade)
- **Documento/localização:** `edital.txt`. O cabeçalho da qualificação econômico-financeira é o item 118 (l. 3165); logo após, surge o item "**119.**" (l. 3317) que **já invoca seu próprio "119.f)"** e é seguido do item 120 (l. 3349), também citando "item 119.f)". O conteúdo das alíneas a)–f) ("119.f)") está sob o item 118.
- **Natureza:** numeração inconsistente — ou o cabeçalho de qualificação deveria ser 119, ou o item 3317 não deveria ser 119; em qualquer hipótese as remissões internas (achado 1.1) não fecham.
- **Correção:** renumerar de forma única e propagar às remissões (ver 1.1).

---

## 6. LACUNAS (ordenado por gravidade)

### 6.1 — "Empresa de consultoria especializada" para cálculo de indenização: instituída por remissão a dispositivo inexistente
- **Documento/localização:** `contrato.txt` l. 5660-5668, 5888, 6437, 6502. O cálculo da indenização nas hipóteses de extinção (advento do termo, encampação, falência) é atribuído a uma "empresa de consultoria especializada de que trata a subcláusula 38.3", **que não existe** (ver 1.2 e 2.3). Não há, no Contrato, regra sobre quem contrata, quem custeia, qual o procedimento de escolha, prazo e vinculação do laudo.
- **Natureza:** lacuna — direito/procedimento de quantificação da indenização sem disciplina efetiva (apenas remissão vazia).
- **Correção:** inserir cláusula que efetivamente institua e discipline a empresa de consultoria especializada e ajustar as remissões.

### 6.2 — "Taxa de regulação e fiscalização" sem parâmetros: percentual, base de cálculo e vencimento em branco
- **Documento/localização:** `contrato.txt` (Cláusula 33) l. 4364-4369: "[•]% ([•]) de [•] referente ao exercício anterior ... até o [•] dia do mês". Além de campos em branco (categoria 3), **não há piso/teto nem fórmula** que delimite a obrigação pecuniária da Concessionária com a Entidade Reguladora.
- **Natureza:** lacuna — obrigação pecuniária periódica sem qualquer parâmetro quantitativo no Contrato (remete-se de fato à definição futura do regulador).
- **Correção:** fixar percentual/base/vencimento ou, ao menos, balizas mínimas no Contrato.

### 6.3 — Remissões genéricas a "NORMAS DE REGULAÇÃO" / "norma do Regulador" para matéria de núcleo contratual
- **Documento/localização:** `contrato.txt`. A definição 22 (NORMAS DE REGULAÇÃO, l. 276) e múltiplas cláusulas remetem ao regulador matérias estruturais — p.ex. metas/indicadores e redutor da contraprestação (Cláusula 17, "sistema de mensuração ... constam do Anexo V do EDITAL" + atos do regulador), contabilidade regulatória, e o próprio "Fator de Avaliação" (FA) da fórmula de reajuste (l. 3139), cuja metodologia não é fechada no Contrato. Agrava-se pela indefinição da própria ENTIDADE REGULADORA (definição 15 em branco — campo `[•]`).
- **Natureza:** lacuna/remissão genérica a "norma do Regulador" para matéria que deveria estar parametrizada no Contrato (sobretudo a mecânica do redutor/FA, que impacta a remuneração).
- **Correção:** parametrizar no Contrato o núcleo do mecanismo (faixas do FA, gatilhos do redutor) e identificar o regulador.

### 6.4 — Penalidades de impedimento/inidoneidade/caducidade sem procedimento próprio de gradação
- **Documento/localização:** `contrato.txt` l. 5000-5022 (Cláusula 37): além das multas (estas, sim, com gradação por Grupos 1/2/3 e procedimento na Cláusula 38), preveem-se "impedimento de licitar" (≤ 3 anos), "inidoneidade" (3 a 6 anos) e "caducidade do CONTRATO" **sem critério de dosimetria** que vincule cada conduta à respectiva sanção e **sem remissão expressa** ao procedimento da Cláusula 38 (que se refere a "Auto de Infração" e "multa", não a estas sanções expropriatórias/restritivas).
- **Natureza:** lacuna — penalidades graves sem gradação/critério de escolha e com procedimento de aplicação apenas implícito.
- **Correção:** disciplinar a dosimetria e o rito (contraditório, recurso, autoridade competente) específicos para impedimento, inidoneidade e caducidade.

---

## NOTAS DE ENCERRAMENTO
- **ETP** (`etp.txt`): documento de natureza argumentativa/justificadora; não contém valores fechados, tabelas, campos `[•]` nem remissões a dispositivos numerados — não foram detectadas inconsistências formais autônomas. O "valor estimado do contrato" é tratado de forma narrativa (l. 456-502), sem repetir o algarismo do Edital (logo, não conflita nem confirma o achado 4.4).
- **Numeração das cláusulas do Contrato** (1 a 52) e do **rol de definições** (1 a 40): sequenciais e completas — as descontinuidades aparentes na varredura automática eram números de página soltos do OCR; conferidas e descartadas.
- **Numeração dos anexos** Edital (I–XI) × Contrato (A–F): o Contrato lista seus próprios anexos como "Anexo A–F" (Cláusula 3) e remete aos anexos do Edital por algarismos romanos (I–XI); não há colisão de sistemas, mas convém atentar que "Anexo E – Contrato de Vinculação de Receitas" (Contrato) e "Anexo VI/V do EDITAL" coexistem — sem conflito detectado, registrado para a consolidação.

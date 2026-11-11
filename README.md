<p align="center">
  <img src="docs/img/abertura.png" alt="Abertura da landing page do Boletim Popus: a marca em letras grandes sobre papel amarelo, o slogan e o botão Assinar o abaixo-assinado" width="640">
</p>

# Boletim Popus

**Promovendo a voz do povo brasileiro contra o rentismo.**

O Boletim Popus é um abaixo-assinado permanente contra a política de juros do Banco Central. Antes de cada reunião do COPOM, as assinaturas e os números agregados dos relatos viram um relatório em PDF, entregue ao Banco Central e ao Ministério da Fazenda e publicado no site.

É um contraponto ao [Boletim Focus](https://www.bcb.gov.br/publicacoes/focus): o Focus reúne as projeções dos economistas do mercado; o Popus reúne a voz de quem toma crédito.

> **Status:** protótipo. A landing page e a minuta da política de privacidade estão prontas, sem backend. O primeiro relatório oficial está previsto para a reunião do COPOM de 16–17 de março de 2027.

## A ideia

A landing page é uma sequência de cartazes no estilo lambe-lambe, um por tema, cada um com um ícone, uma pergunta e o refrão *"Essa luta também é sua!"*. O objetivo é mostrar a quem já se incomoda com os juros que o problema chega no emprego, na empresa, nas dívidas, no carro e na casa.

<p align="center">
  <img src="docs/img/card-endividamento.png" alt="Cartaz laranja com o ícone de uma nota de dinheiro afundando e a pergunta: Está com sua família ou sua empresa afogada em dívidas? Essa luta também é sua!" width="640">
</p>

<p align="center">
  <img src="docs/img/icones-dobras.png" alt="Os cinco ícones das dobras temáticas: placa de não há vagas, fábrica em ruínas, nota afundando, carro com etiqueta de porcentagem e casa com placa de vende-se" width="640">
  <br>
  <sub>Emprego · Empresas · Endividamento · Carro · Moradia</sub>
</p>

## Como funciona

| Passo | O que acontece |
|---|---|
| 1. Você assina | Com nome, e-mail e CPF. O CPF garante uma assinatura por pessoa e nunca é publicado. |
| 2. Você confirma pelo e-mail | Sem o clique no link de confirmação, a assinatura não conta. |
| 3. Sua assinatura vai no relatório | A assinatura vale para todos os ciclos até ser retirada. O nome só aparece se a pessoa autorizar; caso contrário, ela entra apenas na contagem. |

## O relatório

Cada reunião do COPOM gera um relatório, congelado 8 dias antes da reunião. Ele traz o total de assinaturas (com as novas do ciclo em destaque), números agregados dos relatos sobre o impacto dos juros, contexto com dados oficiais, a metodologia e um anexo só com os nomes de quem autorizou a publicação.

<p align="center">
  <img src="docs/img/relatorio-exemplo.png" alt="Modelo do relatório com números fictícios e carimbo de Exemplo: 12.480 assinaturas, empresas que deixaram de expandir, empresas que fecharam, empregos não criados, famílias endividadas e o anexo de nomes" width="420">
  <br>
  <sub>Modelo com números fictícios, como aparece na landing page.</sub>
</p>

Os números são **relatos dos signatários**, de uma amostra autosselecionada, e nunca são apresentados como estatística do país. O relatório diz o que a validação garante (uma assinatura por CPF com formato válido e e-mail confirmado) e nunca afirma que o CPF foi verificado na Receita Federal.

### Ciclo

| Quando | O quê |
|---|---|
| D-14 | Lembrete de que é possível rever ou retirar a assinatura (só para quem aceitou lembretes) |
| D-8 | Congelamento: snapshot imutável das assinaturas ativas e dos relatos aprovados |
| D-7 | Geração do PDF e do hash SHA-256, protocolo no Banco Central e no Fala.BR, envio ao Ministério da Fazenda, publicação no site |
| D+1 | E-mail com a decisão do COPOM (opcional) |

## Privacidade

Assinar um abaixo-assinado revela uma opinião política, que a LGPD trata como dado sensível. Por isso, a base inteira é tratada como sensível:

- consentimentos em caixas separadas e não marcadas, com registro de data, versão do termo e IP;
- CPF guardado só como HMAC, com a chave fora do banco; nunca publicado nem enviado a terceiros;
- gestão da assinatura sem senha, por link mágico de uso único, com retirada a qualquer momento;
- sem ferramentas de análise de audiência, pixels, publicidade ou rastreamento de e-mails;
- fontes servidas pelo próprio site, sem Google Fonts.

A minuta da política está em [`privacidade.html`](privacidade.html) (versão 0.1, em revisão jurídica, ainda não em vigor).

## Estrutura do repositório

```
.
├── index.html          # Landing page (protótipo: HTML, CSS e JS num arquivo só)
├── privacidade.html    # Minuta da política de privacidade (v0.1)
└── docs/
    └── img/            # Imagens deste README
```

Para ver o protótipo, basta abrir `index.html` no navegador. Links para páginas que ainda não existem mostram um aviso de "em construção" (atributo `data-em-breve`).

## Stack planejada

- **Backend:** Django + PostgreSQL, com o painel administrativo para moderar relatos e acionar os ciclos.
- **Frontend:** templates do Django com um pouco de HTMX, reaproveitando o HTML e o CSS da landing.
- **PDF:** WeasyPrint ou Typst, gráficos com matplotlib.
- **E-mail:** Brevo, com rastreamento de aberturas e cliques desligado.
- **Proteção:** Cloudflare e Turnstile.
- **Design:** Big Shoulders Display e Atkinson Hyperlegible (SIL OFL), cores em variáveis CSS.

## Roteiro

| Fase | Período | Entregas |
|---|---|---|
| 0. Protótipo e fundamentos | nov–dez 2026 | Landing page, especificação, metodologia, política de privacidade, revisão jurídica |
| 1. MVP de assinatura | dez 2026–jan 2027 | Formulário com confirmação por e-mail, página Meus Dados, painel administrativo |
| 2. Relatos e relatório | jan–fev 2027 | Formulário de relato, geração do PDF, ciclo de teste na reunião de 26–27 de janeiro |
| 3. Conteúdo e divulgação | fev–mar 2027 | Biblioteca, Compartilhe, artigos "Entenda" |
| Primeiro relatório | mar 2027 | Entrega antes da reunião de 16–17 de março |

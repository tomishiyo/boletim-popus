Boletim Popus — Especificação do projeto
10 de nov. de 2026 · @Guilherme
Visão geral
O Boletim Popus é um site de abaixo-assinado contra a política de juros do Banco Central. Antes de cada reunião do COPOM, gera um relatório em PDF com as assinaturas e números agregados dos relatos, entregue ao Banco Central e ao Ministério da Fazenda e publicado no site.
• Objetivo: mobilizar pessoas insatisfeitas com os juros e dar a elas um canal de pressão recorrente, sincronizado com o calendário do COPOM.
• Público: quem já concorda com a pauta. O tom é de mobilização, não de convencimento de indecisos.
• Posicionamento: contraponto ao Boletim Focus. O Focus reúne projeções de economistas do mercado; o Popus reúne a voz de quem toma crédito. Para ter credibilidade, o relatório precisa de metodologia publicada e números apresentados como relatos, nunca como estatística do país.
• Slogan: "Promovendo a voz do povo brasileiro contra o rentismo".
Estado atual e fases
O protótipo da landing page está pronto (index.html, HTML, CSS e JS num arquivo só). A meta é entregar o primeiro relatório oficial antes da reunião do COPOM de 16–17 de março de 2027.
Fase
Período
Entregas
0. Protótipo e fundamentos
nov–dez 2026
Landing page (feita), especificação, metodologia, política de privacidade, revisão jurídica, questionário do relato
1. MVP de assinatura
dez 2026–jan 2027
Formulário com confirmação por e-mail, página Meus Dados, painel administrativo, e-mail configurado
2. Relatos e relatório
jan–fev 2027
Formulário de relato, geração do PDF, ciclo de teste interno na reunião de 26–27 de janeiro
3. Conteúdo e divulgação
fev–mar 2027
Biblioteca, Compartilhe, artigos "Entenda", página de obrigado
Primeiro relatório
congelamento por volta de 8 de março de 2027
Entrega antes da reunião de 16–17 de março
"Protótipo" é a landing sem backend; "MVP" é a primeira versão que coleta assinaturas de verdade.
Estrutura do site
Só a landing page existe hoje. Os demais endereços já estão linkados nela e mostram um aviso de "em construção" (atributo data-em-breve).
Página
Endereço
Conteúdo
Status
Landing page
/
Chamada, dobras temáticas, como funciona, modelo do relatório
Protótipo pronto
Assinatura
/assinar
Formulário de nome e e-mail, consentimentos. Fica numa página separada para não ser confundida com o formulário de relato
A fazer
Relato detalhado
a definir
Questionário do impacto dos juros
A fazer
Entenda
/entenda-os-juros, com âncoras por tema (#emprego, #empresas, #endividamento, #carro, #moradia)
Artigo único explicando como os juros afetam cada tema, com uma seção por dobra
A fazer
Biblioteca
/biblioteca
Vídeos, posts e leituras sobre juros
A fazer
Quem somos
/quem-somos
Descrição autobiográfica do criador
A fazer
Meus dados
/meus-dados
Ver, corrigir e retirar assinatura por link mágico
A fazer
Privacidade
/privacidade
Política de privacidade e contato do encarregado
A fazer
Relatórios
a definir
Arquivo dos PDFs publicados, com hash
A fazer
Compartilhe
a definir
Textos prontos para WhatsApp, Instagram, X e Facebook
A fazer
Obrigado
a definir
Pós-assinatura, com botões de compartilhar
Adiado
Sugestões ainda não decididas: página de Metodologia, painel com contador de assinaturas (adiado), simulador "quanto os juros te custam", Transparência, FAQ e kit de imprensa.
Landing page
A landing segue a ordem chamada → "você se reconhece aqui?" → como funciona → chamada final, com uma dobra de tela por tema.
Conteúdo, de cima para baixo
1. Abertura: "Boletim Popus", slogan, a declaração "Assine o abaixo-assinado e some sua voz à nossa: contra a política de juros absurda e antipopular praticada pelo Banco Central!", a frase sobre a entrega do relatório antes de cada COPOM e o botão "Assinar o abaixo-assinado". Fecha com "Não sabe como os juros afetam sua vida? Deslize para descobrir por que essa luta também é sua."
2. Dobras temáticas, cada uma com ícone, pergunta, o refrão "Essa luta também é sua!" e o link "Quero entender melhor como os juros afetam isso":
    ◦ Emprego: placa "não há vagas"
    ◦ Empresas: fábrica em ruínas
    ◦ Endividamento: nota de dinheiro afundando
    ◦ Carro: carro com etiqueta "%"
    ◦ Moradia: casa com placa "vende-se"
3. Como funciona: três passos (assina, confirma pelo e-mail, nome vai no relatório), o modelo do relatório com números fictícios e o carimbo "Exemplo", e três garantias (retirada até o fechamento, dados não vendidos, link para Quem Somos).
4. Fechamento: "Junte-se ao Popus e faça sua voz ser ouvida!", botão de assinatura e link para a Biblioteca.
5. Rodapé: Quem somos, Biblioteca, Política de privacidade, Meus dados, Contato.
Decisões tomadas
• O tom do título fica combativo: o público é quem já concorda.
• Os botões dizem "abaixo-assinado", nunca "assinar o boletim", que soaria como newsletter. "Boletim Popus" é o nome do relatório.
• A landing não tem formulário. Os botões levam para /assinar, para não confundir com o formulário de relato no futuro.
• As dobras não explicam o mecanismo; o link de cada uma leva à seção correspondente do artigo único.
• Os números do modelo do relatório são fictícios e marcados como tal, para que um print não seja tomado por dado real.
• Contador de assinaturas e página de obrigado ficaram para depois.
Design
• Estética de cartaz lambe-lambe: tinta preta sobre papéis coloridos, um cartaz por dobra (amarelo, ciano, rosa, laranja, lima, lilás; "Como funciona" em branco).
• Fontes: Big Shoulders Display (títulos) e Atkinson Hyperlegible (texto), do Google Fonts.
• Um único movimento: a marca "colada" ao abrir a página, desligado para quem pede movimento reduzido. Sem rolagem forçada entre dobras.
• Cores definidas como variáveis CSS em :root, para trocar a paleta num lugar só.
Dados coletados
A assinatura do MVP pede só nome e e-mail; o CPF ainda está em aberto. Campos fechados (listas e faixas) têm preferência sobre texto livre, porque viram estatística e dispensam moderação.
Assinatura
Campo
Formato
Situação
Nome completo
Texto
Decidido
E-mail
Texto, confirmado por link (double opt-in)
Decidido
Consentimentos
Caixas separadas, não marcadas, com data e versão do termo
Decidido
CPF
Validação dos dígitos; guardado só como hash HMAC, nunca publicado
Em aberto
UF e município
Lista
Sugerido
Perfil
Pessoa física, MEI, pequena empresa, produtor rural, outro
Sugerido
Relato detalhado (opcional, fase 2)
• Tipo de impacto, múltipla escolha: desistiu de crédito para expandir negócio, para comprar um bem, empresa fechou, família endividada.
• Expansão não feita: setor, porte, valor do investimento em faixas, empregos que seriam criados em faixas.
• Bem não comprado: tipo (imóvel, veículo, máquina, reforma) e faixa de valor.
• Empresa fechada: ano, setor, funcionários em faixas, papel dos juros (principal ou um dos fatores), CNPJ opcional.
• Endividamento: % da renda comprometida em faixas, atraso acima de 90 dias, modalidades (rotativo, cheque especial, consignado, financiamento).
• Texto livre opcional, com limite de caracteres e moderação.
Não coletar: renda exata, endereço, telefone, data de nascimento.
Banco de dados (PostgreSQL): pessoas, consentimentos (histórico, nunca sobrescrito), assinaturas (ativa ou retirada), relatos, ciclos_copom, relatorios, envios_email.
Consentimento, LGPD e gestão da assinatura
A base inteira é tratada como dado sensível, porque assinar revela opinião política (LGPD, art. 5º, II). A base legal é o consentimento específico e destacado (art. 11). Antes do lançamento, fazer uma consulta pontual com advogado de proteção de dados.
Obrigações
• Consentimentos separados: nome no relatório enviado às autoridades; nome exibido no site; receber e-mails; relato citado de forma anônima.
• Política de privacidade com finalidade, dados, prazo de guarda, compartilhamento (autoridades, provedor de e-mail, hospedagem) e como exercer direitos.
• Indicar um encarregado (pode ser o próprio criador), com e-mail publicado.
• Relatório de Impacto (RIPD) simples.
• Transferência internacional (art. 33) se hospedagem ou e-mail ficarem fora do Brasil.
• No relatório, relatos só como números agregados; nunca CPF.
Gestão da assinatura sem perfil nem senha (link mágico)
• A assinatura só conta depois do clique no e-mail de confirmação.
• "Meus dados" tem só um campo de e-mail e envia um link de uso único, válido por 30–60 minutos. A resposta é sempre "se houver cadastro, enviamos um link", para ninguém descobrir quem assinou.
• O link só abre a página; a retirada exige clicar num botão, porque filtros de e-mail visitam links automaticamente.
• Retirar é reversível até o congelamento: um e-mail avisa "se não foi você, clique para restaurar".
• Descadastrar dos e-mails é diferente de retirar a assinatura.
• Limite de tentativas por e-mail e IP, Turnstile no formulário, tokens guardados como hash, registro de eventos de consentimento que só cresce.
• A retirada pode ser feita a qualquer momento, sem esperar e-mail do projeto. Todo e-mail traz o link "gerenciar ou retirar minha assinatura".
• Quem perdeu o acesso ao e-mail escreve ao encarregado, que confere a identidade e retira manualmente.
• Limite, escrito ao lado do botão de assinar: depois do congelamento, o nome sai do site e dos próximos relatórios, mas não do relatório já enviado.
Conflito de CPF (se o CPF for coletado): alguém pode assinar com o CPF de outra pessoa. Nesse caso, os dois registros saem da contagem e vão para revisão manual.
Ciclo do relatório
Cada reunião do COPOM gera um relatório, congelado 8 dias antes do primeiro dia da reunião (D). São 8 reuniões por ano. A assinatura vale para todos os ciclos até ser retirada.
Etapas de cada ciclo
1. D-14: e-mail lembrando que é possível retirar a assinatura até o congelamento.
2. D-8: congelamento. Snapshot imutável das assinaturas ativas e dos relatos aprovados.
3. D-7: geração do PDF e do hash SHA-256; protocolo na Ouvidoria do Banco Central e no Fala.BR; envio ao Ministério da Fazenda; publicação no site; e-mail aos signatários.
4. D+1 (opcional): e-mail com a decisão do COPOM e convite para compartilhar.
Conteúdo do PDF
• Capa e resumo executivo.
• Em destaque, as novas assinaturas do ciclo e o total acumulado até o momento. Depois, números agregados com gráficos: empresas que não expandiram, empresas que fecharam, empregos não criados, famílias endividadas.
• Contexto com dados oficiais (endividamento das famílias, inadimplência, recuperações judiciais).
• Metodologia e limitações: amostra autosselecionada; os números são relatos dos signatários, não o total do país.
• Anexo com nome e UF, sem CPF. Com dezenas de milhares de nomes, o anexo pode virar um arquivo separado.
Calendário 2026–2027
Reunião
Congelamento (D-8)
Uso
8–9 dez 2026
30 nov
Cedo demais
26–27 jan 2027
18 jan
Ciclo de teste interno
16–17 mar 2027
8 mar
Primeiro relatório oficial
27–28 abr 2027
19 abr
Ciclo regular
15–16 jun 2027
7 jun
Ciclo regular
3–4 ago 2027
26 jul
Ciclo regular
21–22 set 2027
13 set
Ciclo regular
26–27 out 2027
18 out
Ciclo regular
7–8 dez 2027
29 nov
Ciclo regular
Fonte do calendário: Comunicado nº 45.452 do Banco Central, de 23/06/2026 (cobertura da EuQueroInvestir).
Stack, hospedagem e custos
A proposta é Django com PostgreSQL, a um custo estimado de R$ 50 a R$ 250 por mês na fase inicial. Valores de novembro de 2026; confirmar na hora de contratar.
Stack sugerida
• Django: painel administrativo pronto para moderar relatos, ver assinaturas e acionar ciclos; formulários, CSRF e migrações inclusos.
• PostgreSQL como banco.
• PDF com WeasyPrint (HTML/CSS → PDF) ou Typst; gráficos com matplotlib.
• Tarefas agendadas (lembretes, congelamento) com cron ou Celery/RQ.
• Frontend: templates do Django com um pouco de HTMX, reaproveitando o HTML e CSS da landing.
Custos estimados
Item
Opção
Custo aproximado
Domínio .com.br
Registro.br
R$ 40/ano
Frontend estático
Cloudflare Pages ou Vercel
Grátis
Backend Python
VPS pequena (Hetzner, DigitalOcean ou nacional)
R$ 30–80/mês
PostgreSQL
Na VPS ou gerenciado (Supabase, Neon)
Grátis a US$ 25/mês
Anti-robô
Cloudflare + Turnstile
Grátis
Backup
Armazenamento de objetos, criptografado
Poucos reais
E-mail
Brevo
Grátis a US$ 18/mês
E-mail: Brevo, que cobra por e-mail enviado e não por contato. O plano grátis permite 300 e-mails por dia; o Starter começa em US$ 9/mês para 5.000 e-mails. A alternativa para quando a base passar de centenas de milhares é o Amazon SES (US$ 0,10 por 1.000 e-mails), que exige montar lista, descadastro e templates. Em qualquer caso, enviar do domínio próprio com SPF, DKIM e DMARC configurados.
Volume previsto: 8 reuniões por ano, 2–3 e-mails por ciclo, cerca de 25 e-mails por pessoa por ano.
Organização do trabalho: um Projeto no Claude com esta especificação e o index.html como arquivos de referência, um chat por frente de trabalho, código num repositório Git.
Questões em aberto e próximos passos
Em aberto
[ ] Coletar CPF ou não? Dá peso formal e evita duplicidade, mas aumenta o risco num vazamento e abre o problema do CPF de terceiros.
[ ] Incluir UF/município e perfil na assinatura?
[ ] A assinatura vale para todos os ciclos até ser retirada? Decidido: sim. O relatório destaca as novas assinaturas do ciclo e o total acumulado.
[ ] Nome público no site ou só no relatório enviado às autoridades?
[ ] Hospedagem no Brasil ou fora (afeta a transferência internacional)?
[ ] Quem é o encarregado e qual o e-mail de contato?
[ ] Texto de "Quem somos" e e-mail de contato do rodapé (hoje contato@exemplo.org).
[ ] Entrar com páginas de Metodologia, FAQ, Transparência e simulador?
Próximos passos
[ ] Criar o repositório e versionar o index.html.
[ ] Registrar o domínio.
[ ] Escrever a política de privacidade e o termo de consentimento.
[ ] Consultar advogado de proteção de dados.
[ ] Desenhar a página /assinar e o fluxo de confirmação por e-mail.
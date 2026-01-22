# 💸 App FinCtrl - Seu parceiro financeiro inteligente - by G-abriele 

PRD refinado no Copilot Web

---

# PRD – Aplicativo de Organização Financeira Conversacional

## Contexto 
O aplicativo busca transformar o controle financeiro em uma experiência simples e contínua, baseada em conversas naturais. A ideia é oferecer uma alternativa acessível para pessoas que têm dificuldades em manter a disciplina financeira, tornando o processo semelhante à interação com um assistente pessoal.

## Problema
Aplicativos financeiros tradicionais sofrem com baixa retenção devido a:
- Cadastros extensos e burocráticos.  
- Necessidade de categorização manual de gastos.  
- Falta de adaptação ao comportamento real do usuário.  

Isso gera frustração, abandono precoce e a percepção de que controlar finanças é complexo e desgastante.

## Público-Avo
- Jovens adultos no início da vida financeira.  
- Trabalhadores autônomos que precisam de praticidade.  
- Usuários que nunca utilizaram aplicativos financeiros e buscam uma solução intuitiva e acessível.  

## Diretriz de Design Universal 
Uma solução deve ser projetada com Design Universal, garantindo:
- Experiência inclusiva para o maior número possível de usuários.  
- Interface clara e acessível, com linguagem simples e visual amigável.  
- Compatibilidade com diferentes dispositivos e tamanhos de tela.  
- Consideração de boas práticas de acessibilidade digital (ex.: contraste adequado, suporte a leitores de tela, navegação intuitiva).  
- Fluxos que não dependem de conhecimento técnico prévio, permitindo uso imediato.  

## Funcionalidades-Chave
- Registro de gastos via linguagem natural: o usuário informa despesas como se estivesse conversando (“gastei R$50 no mercado”).  
- Classificação automática de transações: categorização inteligente com base no contexto da conversa.  
- Metas financeiras simples: criação e acompanhamento de objetivos como reserva de emergência ou quitação de dívidas.  
- Sugestões personalizadas de economia: recomendações práticas do agente financeiro virtual.  
- Relatórios resumidos e adaptados: visualizações simples e relevantes para o perfil do usuário.  
- Alertas inteligentes: notificações quando padrões de gastos fora do normal foram detectados.  

---

## Entregável da IA (MVP) 
O MVP deve conter:

**Principais telas e fluxos de conversa:**
- Tela inicial com resumo financeiro.  
- Chat interativo para registro e acompanhamento.  
- Tela de metas financeiras.  
- Relatórios visuais simplificados.  

**Interações com o Lovable:**
> Olá Lovable!! Crie um App de Finanças Pessoais com base no seguinte PRD (Documento de Requisitos do Produto): {PRD}

> Preciso atualizar algumas funcionalidades do aplicativo para:
login com e-mail e adicionar senha.
Após login com e-mail e senha, o app deve iniciar um fluxo de onboarding em 3 passos:
2.1. Solicitar renda mensal principal do usuário.
2.2. Confirmar categorias básicas de despesas e receitas.
2.3. Exibir saldo inicial e conectar às metas financeiras.
Categorizar finanças em tópicos (Salário, Despesas Fixas, Gastos Variáveis ​​Médios, Saldo Atual) e subcategorias (Aluguel, Água, Luz, Internet, Alimentação, Transporte, Saúde).
A tela inicial deve mostrar saldo atual, receitas e despesas categorizadas, conectando-se diretamente às metas financeiras.
Metas devem ter barras de progresso simples e claras, com impacto visível do saldo e dos gastos.
Usar ícones consistentes, relatórios visuais simplificados e dicas curtas relacionadas ao comportamento do usuário.
Garantir design universal: contraste adequado, textos acessíveis e suporte a leitores de tela.
Toda a interação deve ser feita em linguagem natural, mantendo o tom de conversa simples e acessível.

> Consegue atualizar o aplicativo com essas funcionalidades:
Autenticação:
Login com e-mail e senha.
Onboarding pós-login (3 passos):
2.1 Solicitar renda mensal principal do usuário.
2.2 Confirmar categorias básicas de receitas e despesas.
2.3 Exibir saldo inicial e oferta de criação de metas financeiras.
Dados:
No primeiro acesso, inicie com dados zerados.
Nos acessos a seguir, carregue automaticamente os dados salvos do usuário após o login.
Tipos obrigatórios:
Transação: { id, título, categoria, valor, data de criação }
ResumoFinanceiro: { saldoAtual, rendaTotal, despesasTotal, taxaDePoupança }
ObjetivoFinanceiro: { id, nome, valorAlvo, valorAtual, dataDeCriação }
Categorias:
Tópicos: Salário, Despesas Fixas, Gastos Variáveis ​​Médios, Saldo Atual.
Subcategorias: Casa (Aluguel, Água, Luz, Internet), Alimentação (Mercado, Delivery, Fora de Casa), Transporte (Uber, Combustível, Outros), Saúde.
Categorização automática: transações registradas em linguagem natural devem ser classificadas na categoria correta (ex.: “Paguei R$ 120 de internet” → Casa/Internet).
Tela inicial (Painel de controle):
Mostrar saldo atual, receitas e despesas categorizadas.
Exibir últimas transações com dados (createdAt).
Conectar-se diretamente às metas financeiras.
Props tipadas corretamente: { summary: FinancialSummary; transactions: Transaction[] }
Metas:
Criar, editar e excluir metas financeiras.
Exibir barras de progresso simples e claras.
Mostrar impacto visível do saldo e dos gastos.
Atualizar automaticamente o progresso das metas quando novas receitas ou despesas forem registradas.
Props digitados corretamente: { metas: FinancialGoal[] }
Relatórios:
Relatórios visuais simplificados (semanais/mensais).
Gráficos claros e acessíveis.
UI/UX:
Ingredientes consistentes.
Dicas curtas relacionadas ao comportamento do usuário.
Design Universal: contraste adequado, textos acessíveis, suporte a leitores de tela.
Interação:
Toda a interação deve ser feita em linguagem natural.
Tom de conversa simples, educativo e acessível. 

> Quando eu adiciono dinheiro a uma meta, quero que esse valor seja descontado do saldo atual automaticamente.

> Poderia adicionar botão de sair/logout. Ao clicar, encerrar sessão e redirecionar para tela de login. Não apague os dados salvos do usuário, apenas limpe a sessão.

> Poderia mudar o nome do App para FinCtrl - Seu parceiro financeiro inteligente (o subtitulo gostari de colocar abaixo)

## Resultado Final no Lovable: https://ask-my-wallet.lovable.app/auth

<img width="461" height="775" alt="image" src="https://github.com/user-attachments/assets/796b51a2-774d-4760-9a45-5e1943b8dd92" /> <img width="478" height="775" alt="image" src="https://github.com/user-attachments/assets/a199c8cd-7a4e-412c-aed9-5121f5285483" />

## Funcionalidades

# FinCtrl 
**FinCtrl – Seu parceiro financeiro inteligente** é um aplicativo de gestão financeira pessoal que ajuda o usuário a organizar, acompanhar e planejar suas finanças de forma simples e intuitiva. ##
Principais funcionalidades 
- **Interação via chat**: todas as transações são registradas e categorizadas através de conversas em linguagem natural, tornando o uso mais prático e acessível.
- **Dashboard inteligente**: mostra saldo atual, últimas transações e progresso das metas em barras visuais.
- **Metas financeiras conectadas**: ao investir em uma meta, o saldo atual é atualizado automaticamente, garantindo consistência entre metas e finanças.
- **Relatórios visuais**: gráficos semanais e mensais exibem evolução de receitas, despesas e saldo.
- **Experiência acessível e moderna**: design com contraste adequado, ícones consistentes e suporte a leitores de tela.

**Propósito:**
O app foi criado para ser **um aliado no controle financeiro pessoal**, oferecendo clareza, praticidade e confiança. Ele simplifica o acompanhamento do dinheiro, ajuda a planejar metas e garante que o usuário tenha sempre uma visão completa das suas finanças — tudo isso de forma interativa pelo chat.


## Reflexão sobre o processo:

### O que funcionou bem?  
A previa do PRD feito no Copilot, ajudou muito para dar o primeiro comando no Lovable, para entender do que se tratava o App e como ele iria funcionar. Com isso as divisões das telas ficaram certinhas (inicio, conversar, metas e relatorios). 

### O que não funcionou como o esperado?  
Varias funcionalidades não saíram como esperava, por isso levei 3 dias para concluir o projeto (ansiedade bateu viu kk). Vou pontuar aqui o que tive que pedir para o Lovable modificar: 

- Tela de Login - não havia opção clara para o usuário sair da conta e retornar à tela de login, tive que adicionar o fluxo de logout, que encerra a sessão e redireciona corretamente para a tela de login, sem apagar dados salvos. 
- Onboarding - o app não guiava o usuário de forma clara no primeiro acesso, estruturei um onboarding simplificado, explicando como registrar transações via chat, visualizar o dashboard e criar metas financeiras.
- Categorização de Transações - as transações não eram classificadas automaticamente, exigindo esforço manual do usuário, implementei uma categorização automática via chat, interpretando entradas em linguagem natural (ex.: "paguei internet" → categoria Casa/Internet).
- Metas Financeiras - ao investir em uma meta, o saldo não era atualizado corretamente, causando inconsistência entre metas e finanças, com a modificação agora as metas estão integradas ao saldo, garantindo que qualquer investimento reduza o valor disponível e mantenha os relatórios consistentes.
- Relatórios e Dashboard - os relatórios visuais não refletiam corretamente as transações e metas, por isso criei gráficos que mostram evolução de receitas, despesas e saldo, além de um dashboard claro com saldo atual e progresso das metas.
- Identidade do App - nome genérico e sem destaque, com a ajuda do Copilot defini o nome final **FinCtrl – Seu parceiro financeiro inteligente**, reforçando o caráter tech e acessível do app. ---

### O que aprendeu sobre conversar com IAs?
Aprendi que conversar com IAs não é apenas dar comandos, mas estruturar ideias com clareza e contexto. Quanto mais objetivo e organizado é o pedido, mais a IA se torna uma parceira criativa e eficiente na construção de soluções.


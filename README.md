# fila-demandas-dados-bi
# Atividade 9: Fila de demandas de dados e BI

**Área:** Dados e Business Intelligence | **Método:** Kanban | **Tempo Estimado:** 35 min

## 📌 Cenário
A equipe de dados (composta por 3 pessoas) recebe pedidos de relatórios e dashboards de todas as áreas da empresa, sendo que **todos** chegam rotulados como urgentes. Atualmente, existem **25 pedidos na fila**, e o tempo médio de espera para atendimento chegou a **6 semanas**.

---

## 🛠️ O que foi feito (Passo a Passo)

### 1. Processo de Entrada para Novos Pedidos (Ingestão)
Para evitar pedidos desorganizados enviados por mensagens informais (Slack, WhatsApp, e-mail direto), criamos um formulário padrão obrigatório:
* **Informações Obrigatórias:**
  * **Título e Descrição:** O que precisa ser feito e qual é o objetivo de negócio.
  * **Área Solicitante e Solicitante:** Quem está pedindo e quem é o responsável pela validação.
  * **Impacto Esperado:** Quantas pessoas serão beneficiadas e qual o ganho (ex: redução de horas gastas, aumento de receita).
  * **Prazo Limite / Data Crítica:** Há alguma obrigatoriedade legal ou regulatória?
* **Quem decide a prioridade?**
  * Um comitê semanal composto por um representante de Dados e líderes de negócio define a prioridade com base nos critérios objetivos abaixo.

---

### 2. Critérios Objetivos de Priorização
Para eliminar o argumento de que "tudo é urgente", adotamos uma matriz de pontuação baseada em impacto e esforço:
1. **Valor de Negócio (Impacto financeiro ou estratégico):** Alto (3 pts), Médio (2 pts), Baixo (1 pt).
2. **Prazo Legal / Regulatório:** Há multa ou risco jurídico se não for feito? (Sim = Prioridade máxima / Não = Segue o fluxo normal).
3. **Quantidade de Usuários Impactados:** Equipe inteira, diretoria ou apenas uma pessoa?
4. **Esforço Técnico (Estimativa da equipe de dados):** Tarefas rápidas (quick wins) ganham tração para aliviar a fila.

---

### 3. Desenho do Quadro Kanban com Limite de WIP
Para visualizar o fluxo e evitar gargalos com uma equipe de 3 pessoas, estruturamos o quadro com os seguintes estágios e **Limites de WIP (Work in Progress / Trabalho em Andamento)**:

| Backlog | A Fazer (To Do) | Em Andamento (WIP Max: 3) | Validação com Solicitante (WIP Max: 2) | Concluído (Done) |
| :--- | :--- | :--- | :--- | :--- |
| *Novos pedidos triados aguardando priorização.* | *Itens priorizados para o ciclo atual (Sprint).* | *Máximo de 1 tarefa por analista (Total: 3 simultâneas).* | *Entregue para o solicitante testar e aprovar.* | *Dashboards e relatórios publicados em produção.* |

* **Regra do WIP:** Nenhum analista puxa uma nova tarefa se o limite da coluna "Em Andamento" ou "Validação" estiver estourado, garantindo foco na entrega em vez de iniciar múltiplos projetos ao mesmo tempo.

---

### 4. Ação para Reduzir Pedidos Repetidos e de Baixo Valor
* **Criação de um Painel de Autoatendimento (Self-Service BI):**
  * Desenvolver dashboards coringa ou treinamentos básicos para as áreas de negócio (ex: Power BI / Looker Studio), permitindo que os próprios solicitantes filtrem e extraiam os dados mais comuns sem precisar abrir chamados recorrentes.
  * **FAQ / Central de Conhecimento:** Documentar relatórios já existentes para evitar duplicação de pedidos.

---

## 🎯 Resultado Esperado Alcançado
* Processo de entrada padronizado e transparente.
* Fim do critério "quem grita mais alto" através de priorização objetiva.
* Visibilidade do fluxo de trabalho com controle de gargalos via limites de WIP.

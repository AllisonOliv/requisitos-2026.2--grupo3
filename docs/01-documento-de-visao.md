# 1. Documento de Visão — GOI

## 1.1 Contexto
A Unifor mantém convênios com mais de 140 instituições em 30 países **[D]**. As oportunidades de mobilidade (editais, bolsas, vagas em parceiras) envolvem prazos, critérios de elegibilidade e documentação que variam de uma oportunidade para outra. A divulgação e o acompanhamento desses itens tendem a ser dispersos (site, e-mail, redes sociais, atendimento presencial) **[H]**.

## 1.2 Declaração do problema

| | |
|---|---|
| **O problema** | Informações sobre editais, bolsas e oportunidades de mobilidade estão espalhadas e difíceis de acompanhar |
| **Afeta** | Estudantes interessados, equipe do NEI/DRI, coordenadores de curso |
| **Impacto** | Estudantes perdem prazos ou desistem por não saberem se são elegíveis; a equipe responde às mesmas dúvidas repetidamente e acompanha manifestações de interesse manualmente **[H]** |
| **Uma solução de sucesso** | Centralizar o cadastro, a divulgação e o acompanhamento de editais, bolsas e manifestações de interesse em um único sistema, com critérios e prazos claros |

## 1.3 Objetivos
**Geral:** especificar um sistema web (responsivo) para gestão e acompanhamento de oportunidades internacionais.

**Específicos**
1. Permitir ao NEI/DRI cadastrar, publicar e manter editais e bolsas com requisitos, prazos e documentação.
2. Permitir ao estudante encontrar oportunidades, verificar pré-elegibilidade e manifestar interesse.
3. Permitir o acompanhamento do status das manifestações por estudantes e equipe.
4. Reduzir perda de prazos e retrabalho de atendimento.

## 1.4 Escopo

**Dentro do escopo (produto mínimo / MVP)**
- Cadastro, publicação, edição e encerramento de editais e bolsas.
- Critérios de elegibilidade, prazos e lista de documentos por edital.
- Busca e filtros de oportunidades.
- Verificação de pré-elegibilidade pelo estudante.
- Manifestação de interesse e acompanhamento de status.
- Notificações de prazos e mudanças de status.
- Painel e relatórios básicos para o NEI/DRI.

**Fora do escopo (nesta fase)**
- Processo completo de seleção, ranqueamento e resultado final.
- Gestão de convênios, aproveitamento de créditos e pós-intercâmbio.
- Rede social/fórum/Tandem (outros temas do Eixo I).
- Pagamento ou gestão financeira de bolsas.

## 1.5 Usuários
Estudante · Equipe NEI/DRI · Coordenador de curso · Administrador do sistema (ver `02-stakeholders.md`).

## 1.6 Principais funcionalidades (visão geral)
Catálogo de oportunidades · critérios configuráveis de elegibilidade · autoavaliação · manifestação de interesse · acompanhamento de status · checklist de documentos · calendário de prazos · notificações · relatórios.

## 1.7 Premissas
- **P1 [H]** Será possível autenticar usuários com credenciais institucionais.
- **P2 [H]** Dados acadêmicos (percentual concluído, média, reprovações) podem ser obtidos do sistema acadêmico, mediante autorização.
- **P3 [H]** O NEI/DRI designará responsáveis por manter os editais atualizados.

## 1.8 Restrições
- **R1** Tratamento de dados pessoais conforme a LGPD.
- **R2** Integrações institucionais dependem de autorização e acesso (conforme material da disciplina).
- **R3** Prazo da disciplina: documentação e modelagem apenas, sem implementação obrigatória.

## 1.9 Riscos

| ID | Risco | Prob. | Impacto | Mitigação |
|---|---|---|---|---|
| RS1 | Sem acesso ao NEI/DRI para validar requisitos | Média | Alto | Análise documental + validação com ex-intercambistas |
| RS2 | Critérios de elegibilidade variam muito entre editais | Alta | Médio | Critérios configuráveis por edital |
| RS3 | Sem integração com sistema acadêmico | Média | Alto | MVP com autodeclaração + conferência pelo NEI |
| RS4 | Escopo crescer demais | Alta | Médio | MVP definido; extras no backlog (Could/Won't) |
| RS5 | Desatualização dos editais | Média | Alto | Responsável por edital + alerta de revisão |

## 1.10 Critérios de sucesso **[H]**
- Todo edital publicado exibe prazo, requisitos e documentos em uma única tela.
- Estudante consegue verificar pré-elegibilidade em poucos passos.
- Redução das dúvidas repetitivas ao NEI/DRI (a medir com a equipe).

## 1.11 Justificativa da escolha do tema
O tema 3 foi escolhido por ter problema bem delimitado, usuários acessíveis (estudantes e equipe do NEI/DRI) e regras de negócio ricas (elegibilidade, prazos, estados do processo), o que favorece a prática de elicitação e modelagem.

## 1.12 Glossário

| Termo | Definição |
|---|---|
| NEI | Núcleo de Estratégias Internacionais (nome usado no material da disciplina) |
| DRI | Diretoria/Departamento de Relações Internacionais (nome usado em outro material; **confirmar com a equipe se são o mesmo setor**) |
| Edital | Documento que abre o processo de seleção para uma oportunidade de mobilidade |
| Bolsa | Apoio financeiro ligado ou não a um edital |
| Mobilidade | Período de estudo em instituição de outro país |
| Manifestação de interesse | Registro do estudante de que deseja participar de uma oportunidade |
| Elegibilidade | Conjunto de critérios que o estudante precisa atender |
| Pré-elegibilidade | Verificação automática preliminar; não garante aprovação |
| MVP | Produto mínimo viável |
| LGPD | Lei Geral de Proteção de Dados |

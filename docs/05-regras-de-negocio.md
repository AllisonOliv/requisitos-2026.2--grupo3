# 5. Regras de Negócio

Legenda: **[D]** base documental · **[H]** hipótese a validar com o NEI/DRI.

| ID | Regra | Status |
|---|---|---|
| RN01 | Apenas editais com status **Publicado** são visíveis aos estudantes | H |
| RN02 | Só é possível manifestar interesse em edital com inscrições **abertas** (dentro do período definido) | H |
| RN03 | Ao fim do período de inscrição, o edital passa automaticamente para **Encerrado** | H |
| RN04 | Cada estudante pode ter **uma única manifestação ativa** por edital | H |
| RN05 | A pré-elegibilidade é calculada pelos critérios cadastrados no edital | D |
| RN06 | Critério de elegibilidade padrão: matrícula ativa, **30% a 70%** do curso concluído, **média ≥ 7,0** e **sem reprovações** (valores a confirmar; cada edital pode ter critérios próprios) | D / H |
| RN07 | A pré-elegibilidade **não garante** aprovação; a decisão final cabe ao NEI/DRI | H |
| RN08 | Estudantes não elegíveis podem consultar o edital, mas o sistema deve avisar o motivo da inelegibilidade | H |
| RN09 | Apenas usuários NEI/DRI autorizados (ou o responsável designado) podem criar, alterar, publicar ou encerrar editais | H |
| RN10 | Um edital não pode ser publicado sem **título, período de inscrição, critérios e lista de documentos** | H |
| RN11 | Alteração de prazo ou de requisito de edital publicado deve notificar quem manifestou interesse e registrar no histórico | H |
| RN12 | Dados acadêmicos (percentual concluído, média, reprovações) são **somente leitura** e vêm de fonte institucional oficial; o aluno não pode editá-los | H |
| RN13 | Um estudante só visualiza as **próprias** manifestações; o NEI/DRI vê todas; o coordenador vê apenas as do seu curso | H |
| RN14 | Os status de uma manifestação seguem o fluxo: **Registrada → Em análise → (Pendência de documentos ↔ Em análise) → Aprovada para próxima fase / Não elegível / Cancelada / Encerrada** | H |
| RN15 | O estudante pode cancelar a manifestação somente enquanto o edital estiver aberto | H |
| RN16 | O uso de dados pessoais exige informar a finalidade ao usuário e respeitar a LGPD | D |
| RN17 | Editais encerrados são mantidos em arquivo para consulta e relatórios, sem possibilidade de novas manifestações | H |
| RN18 | Notificações de prazo são enviadas ao estudante com manifestação ou favorito nos prazos de 7 e 1 dia antes do encerramento (valores a confirmar) | H |

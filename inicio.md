## NOME DO PROJETO:
   Sistema de Doações de Materiais Escolares

## INTEGRANTES:
  Thiago
  André
  Gabriel
  Eduardo
  Endrew

## 2) OBJETIVO DO SISTEMA:
   O sistema tem como objetivo cadastrar instituições de ensino (escolas, faculdades, etc.), estudantes e materiais escolares, permitindo o controle de estoque e registro de doações.
   O público-alvo são estudantes de baixa renda, que poderão receber doações de materiais escolares por meio das instituições cadastradas.

## 3) FUNCIONALIDADES PRINCIPAIS:
### - CADASTRO DE INTITUICAO
   Cadastrar informações da instituição (nome, CNPJ, telefone, endereço).
   Cadastrar estudantes vinculados à instituição.

### - AUTENTICACOS (LOGIN)
   Tela de login específica para instituições.
   Tela de login específica para estudantes.

### - CADASTRO DE ITENS EM ESTOQUE
   Cadastro de materiais escolares (ex.: cadernos, mochilas, canetas).
   Controle de quantidade disponível.

### - REGISTRO DE DOACOES
   Instituições podem registrar doações recebidas.
   Relacionar doação a estudante(s) específico(s).

### - RELATORIOS/LISTAGENS
   Listagem de estudantes beneficiados.
   Relatório de doações por instituição e por material.

## 4) MODELO DE DADOS
| Entidade        | Campos principais                                               | Relacionamentos                                                              |
|-----------------|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| **Instituição** | id, nome, CNPJ, telefone, endereço                              | 1 Instituição possui muitos Estudantes, muitas Doações                       |
| **Estudante**   | id, nome, CPF, data_nascimento, id_instituicao                  | Estudante pertence a 1 Instituição                                          |
| **Material**    | id, nome, descrição, quantidade_estoque                         | Material pode estar em muitas Doações                                        |
| **Doação**      | id, id_instituicao, id_estudante, id_material, data, quantidade | 1 Doação pertence a 1 Instituição e 1 Estudante; envolve 1 ou mais Materiais |

	
## 5) PROTOTIPO DAS TELAS
### - TELA DE LOGIN (Instituição e Estudante)
   Campos: email, senha + botão “Entrar”.

### - DESHBOARD
   Menu lateral com opções: “Instituições”, “Estudantes”, “Materiais”, “Doações”, “Relatórios”.

### - TELA DE CADASTRO DE ITEMN (Material Escolar)
   Formulário com: nome, descrição, quantidade, botão “Salvar”.

### - TELA DE REGISTRO DE DOACAO
   Selecionar instituição → selecionar estudante → escolher material → definir quantidade → botão “Registrar Doação”.

## 6) FLUXO DO SISTEMA
  ### 1) Usuário acessa o sistema e realiza login (Instituição ou Estudante).

  ### 2) Ao logar como Instituição:
   - Acessa dashboard.
   - Cadastra materiais no estoque.
   - Registra doações para estudantes vinculados.
   - Gera relatórios.

  ### 3) Ao logar como Estudante:
   - Consulta seus dados e histórico de doações.
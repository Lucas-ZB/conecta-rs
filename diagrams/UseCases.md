usecaseDiagram
    actor "Administrador" as admin
    actor "Usuário Padrão" as user

    package "Módulo Gestão Patrimonial (PoALAB)" {
        usecase "Fornecer senha ao usuário" as UC_FornecerSenha
        usecase "Criar novos materiais\n(consumo e capital)" as UC_CriarMateriais
        usecase "Listar materiais" as UC_ListarMateriaisAdmin
        usecase "Remover materiais" as UC_RemoverMateriais
        usecase "Listar usuários" as UC_ListarUsuarios
        usecase "Remover usuários" as UC_RemoverUsuarios

        usecase "Solicitar senha" as UC_SolicitarSenha
        usecase "Cadastrar-se" as UC_Cadastrar
        usecase "Fazer Login" as UC_Login
        usecase "Editar senha" as UC_EditarSenha
        usecase "Listar itens" as UC_ListarItensUser
        usecase "Adicionar quantidade de item" as UC_AddQtdItem
    }

    admin --> UC_FornecerSenha
    admin --> UC_CriarMateriais
    admin --> UC_ListarMateriaisAdmin
    admin --> UC_RemoverMateriais
    admin --> UC_ListarUsuarios
    admin --> UC_RemoverUsuarios

    user --> UC_SolicitarSenha
    user --> UC_Cadastrar
    user --> UC_Login
    user --> UC_EditarSenha
    user --> UC_ListarItensUser
    user --> UC_AddQtdItem

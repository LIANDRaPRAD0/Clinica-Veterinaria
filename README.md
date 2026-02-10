# Clinica-Veterinaria

erDiagram
    DONO ||--o{ PET : possui
    CLIENTE ||--|| DONO : "é"
    CLIENTE ||--o{ VENDA : realiza
    VENDA ||--o{ ITEM_VENDA : contém
    PRODUTO ||--o{ ITEM_VENDA : vendido_em
    CLINICA ||--o{ PRODUTO : oferece
    CLINICA ||--o{ FUNCIONARIO : emprega
    FUNCIONARIO ||--o{ VENDA : registra
    PET ||--o{ ATENDIMENTO : recebe
    FUNCIONARIO ||--o{ ATENDIMENTO : realiza

    DONO {
        int id_dono
        string nome
        string telefone
        string email
        string endereco
    }

    CLIENTE {
        int id_cliente
        date data_cadastro
        string tipo
    }

    PET {
        int id_pet
        string nome
        string especie
        string raca
        int idade
        float peso
    }

    PRODUTO {
        int id_produto
        string nome
        string categoria
        float preco
        int estoque
    }

    VENDA {
        int id_venda
        date data
        float valor_total
        string forma_pagamento
    }

    ITEM_VENDA {
        int id_item
        int quantidade
        float preco_unitario
    }

    FUNCIONARIO {
        int id_funcionario
        string nome
        string cargo
    }

    ATENDIMENTO {
        int id_atendimento
        date data
        string tipo
        string observacoes
    }

    CLINICA {
        int id_clinica
        string nome
        string cnpj
        string endereco
    }

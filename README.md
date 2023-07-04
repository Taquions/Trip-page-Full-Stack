Será feito um sistema de reserva de viagens, com frontend e backend

Estrutura:
    - Buscar viagens
        -Por localização, por data inicial, orçamneto máximo
    - Ver detalhes de uma viagem
        -Fotos(4), descrição, foto principal, destaques, preço por noite, data, hospedes
    -Reservar uma viagem
        - Garantir que data selecionada não foi reservada por outro usuário
        - Garantir que número máximo de hóspedes seja respeitado
    -Ver viagens já reservadas
        -Pegar viagens do usuário
    -Cancelar essas viagens
        - Ao cancelar uma viagem, data precisa ficar disponível


Bamco de dados:
    -Será usado o Postgres
    Estrutura:
        Trip:
            -ID(string)[PK]
            -Location(String)
            -Start Date (Date)
            -End Date (Date)
            -Price per day (Number)
            -Description (String)
            -Cover Image (String)
            -Images URL (String[])
            -Highlights (String)
            -Max Guests (Number)
            -Name (String)
        Trip Reservations:
            -ID (String) [PK]
            -Trip ID (String) [FK]
            -User ID (String) [FK]
            -Start Date (Date)
            -End Date (Date)
            -Total paid (Number)
        User:
            - ID (string) [Pk]
            

# Sintaxe do Diagrama de Sequência
@startuml
actor Engenheiro
participant Sistema
participant Registro
participant Aplicacao

Engenheiro -> Sistema : login(usuário, senha)
Sistema --> Engenheiro : confirmação de login

Engenheiro -> Sistema : solicitarData()
Sistema -> Registro : buscarRelatorios(data)
Registro --> Sistema : lista de relatorios
Sistema --> Engenheiro : exibir relatorios

Engenheiro -> Sistema : selecionarRelatorio()
Sistema --> Engenheiro : exibir relatorio

Engenheiro -> Sistema : criarRelatorio(dados)
Sistema -> Registro : gerarRelatorio(dados)
Registro -> Aplicacao : gerarDados()
Aplicacao --> Registro : guardarDados(dados)
Registro --> Sistema : relatorio gerado
Sistema --> Engenheiro : relatorio adicionado

Engenheiro -> Sistema : alterarRelatorio(novosDados)
Sistema -> Registro : atualisarRelatorio(novosDados)
Registro -> Aplicacao : gerarDados(novosDados)
Aplicacao --> Registro : guardarDados(dados)
Registro --> Sistema : dados confirmados
Sistema --> Engenheiro : dados atualisados
@enduml

## URL do diagrama

//www.plantuml.com/plantuml/png/hPD1ReCm44NtdC9B8fKBT16b4hr0UeA9xTAHZ0UDnrMlKtNHWt2n6YeCH7MKHRVscyUV3vo204liNGLQYDMpxwn_iyXK3Ua2DGxWHRrW4Dl3xkniktHw1JuD3ZLeeAfQLQevBWRrg1nrwEiOulZ9I0yg90eErG8q2Lv74w_9loBtC7wFNwIC_HMK_O5I11JW5WJgZVYO8oVg4eC6Fbi7GemKQWEIKcIYsMV6830zc_D0ER3zm0lo5YrdjSvg9Bz9KX_kDvV5cd7hD60ebAheBF_1Ba22yrlDT3inAUbwqLmv8x1PkDbOx3PlCwiDbTTVIJ0ursPkL01EzejvUgVGtce298B3K1Ywfv8L_vzovjly2vZYPxUWUOK9FLblOkz-0000

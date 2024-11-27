Financeiro:

Algoritmo "Financeiro"

Var
// Seção de Declarações das variáveis 
receita, despesas, saldo, opcao, estoqueqtd: inteiro

Inicio
// Seção de Comandos, procedimento, funções, operadores, etc... 
despesas <- 0
saldo <- 0
receita <- 0
estoqueqtd <- 0

repita

escreval("")
escreval("[1] Para registrar a receita:")
escreval("[2] Para registrar as despesas:")
escreval("[3] Para registrar o estoque:")
escreval("[4] Para ver o saldo:")
escreval("[5] Para ver o estoque:")
escreval("[6] Para sair:")
leia(opcao)

escolha opcao

caso 1

escreval("Digite a receita: ")
leia(receita)

Caso 2

escreval("Digite as despesas: ")
leia(despesas)

caso 3

escreva("Digite a quantidade de estoque.")
leia(estoqueqtd)

caso 4

saldo <- receita - despesas

escreval("O saldo é de: ", saldo)

caso 5

escreval("O estoque é de: ", estoqueqtd)

caso 6

escreval("Sistema encerrando...")
fimescolha
ate opcao = 6

fimescolha

Fimalgoritmo

------------------------------------------------------------------------------


Marketing
Controle de Publicidade

algoritmo "Gerenciamento_Marketing"
var
   Campanhas: vetor[1..10] de caractere
   Mercado: vetor[1..10] de caractere
   Estrategias: vetor[1..10] de caractere
   TotalCampanhas, TotalMercado, TotalEstrategias, Opcao, i: inteiro
   Descricao: caractere
inicio
   TotalCampanhas <- 0
   TotalMercado <- 0
   TotalEstrategias <- 0
   repita
      // Menu Principal
      escreval("")
      escreval("========== ÁREA DE MARKETING ==========")
      escreval("1 - Desenvolver Campanha de produto")
      escreval("2 - Adicionar analise do Mercado de consruções")
      escreval("3 - Criar Estratégia para o setor de infraestrutura")
      escreval("4 - Relatórios")
      escreval("5 - Sair")
      escreval("=======================================")
      escreval("")
      escreva("Escolha uma opção: ")
      leia(Opcao)
      escolha opcao
         caso 1
            escreva("Descreva a campanha do produto Amanco: ")
            leia(Descricao)
            TotalCampanhas <- TotalCampanhas + 1
            Campanhas[TotalCampanhas] <- Descricao
            escreval("Campanha adicionada com sucesso!")
         caso 2
            escreva("Insira os detalhes da análise de mercado: ")
            leia(Descricao)
            TotalMercado <- TotalMercado + 1
            Mercado[TotalMercado] <- Descricao
            escreval("Análise de mercado registrada com sucesso!")
         caso 3
            escreva("Descreva a estratégia para o setor--: ")
            leia(Descricao)
            TotalEstrategias <- TotalEstrategias + 1
            Estrategias[TotalEstrategias] <- Descricao
            escreval("Estratégia criada com sucesso!")

         caso 4
            escreval("")
            escreval("========== RELATÓRIOS ==========")
            escreval("Campanhas Amanco: ")
            para i de 1 ate TotalCampanhas faca
               escreval(i, ": ", Campanhas[i])
            fimpara

            escreval("Análises de Mercado: ")
            para i de 1 ate TotalMercado faca
               escreval(i, ": ", Mercado[i])
            fimpara
            escreval("Estratégias: ")
            para i de 1 ate TotalEstrategias faca
               escreval(i, ": ", Estrategias[i])
            fimpara
            escreval("================================")
            escreval("")
       caso 5
            escreval("Encerrando o sistema...")
         outrocaso
            escreval("Opção inválida! Tente novamente.")
      fimescolha
   ate Opcao = 5
fimalgoritmo

Rh:

Cadastro dos Candidatos

Algoritmo "RH"

Var
   // Seção de Declarações das variáveis
   nome_candidato: vetor [1 .. 10]  de inteiro
   cargo_candidato: vetor [1 .. 10] de inteiro
   idade_candidato: vetor [1 .. 10] de inteiro
   num_candidatos, i, idade: inteiro
Inicio
   // Seção de Comandos, procedimento, funções, operadores, etc...
   escreval("Digite o número de candidatos a serem cadastrados: ")
   leia(num_candidatos)

   para i de 1 ate num_candidatos faca
      escreval("Digite o nome do candidato ", i, ": ")
      leia(nome_candidato[i])
      escreval("Digite a idade do candidato ", i, ": ")
      leia(idade_candidato[i])
      escreval("Digite o cargo pretendido por ", nome_candidato[i], ": ")
      leia(cargo_candidato[i])
   fimpara


   escreva("Lista de candidatos cadastrados:")
   para i de 1 ate num_candidatos faca
      escreval("Candidato: ", nome_candidato[i])
      escreval("Idade: ", idade_candidato[i], " anos")
      escreval("Cargo pretendido: ", cargo_candidato[i],)
      escreval("Cadastro foi concluido com sucesso!")
   fimpara


Fimalgoritmo

infraestrutura:

TipoEquipamento: Caractere
    TipoRecurso: Caractere
    DataUltimaManutencao: inteiro
    DataAtual: inteiro
    NecessitaManutencao: logico
    QuantidadeRecursoDisponivel: Inteiro
    QuantidadeRecursoAlocado: Inteiro
    QuantidadeRecursoRestabelecido: Inteiro
    NomeProcesso: Caractere
    StatusProcesso: Caractere
    RecursosAlocados: Inteiro

Inicio
// Seção de Comandos, procedimento, funções, operadores, etc... 
se (DataAtual - DataUltimaManutencao) >= 30 Então
NecessitaManutencao <- Verdadeiro
escreva("O equipamento ", TipoEquipamento, " necessita de manutenção.")
senao
escreva("O equipamento ", TipoEquipamento, " não necessita de manutenção.")
fimSe
se NecessitaManutencao Então
DataUltimaManutencao <- DataAtual
escreva("Manutenção realizada no equipamento ", TipoEquipamento, " em ", DataAtual)
fimSe
 se QuantidadeRecursoAlocado <= QuantidadeRecursoDisponivel Então
 QuantidadeRecursoDisponivel <- QuantidadeRecursoDisponivel - QuantidadeRecursoAlocado
 Escreva(QuantidadeRecursoAlocado, " unidades de ", TipoRecurso, " alocadas com sucesso.")
 RecursosAlocados <- QuantidadeRecursoAlocado
 senao
 escreva("Não há recursos suficientes de ", TipoRecurso, ". Disponível: ", QuantidadeRecursoDisponivel)
 fimse
 escreva("Processo: ", NomeProcesso, " - Status: ", StatusProcesso)
 escreva("Recurso ", TipoRecurso, ": ", QuantidadeRecursoDisponivel, " unidades disponíveis.")
  StatusProcesso <- "Finalizado"
  escreva("Processo ", NomeProcesso, " finalizado.")

Fimalgoritmo

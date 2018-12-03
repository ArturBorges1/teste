# Descrição
Este sistema consiste em uma página web que divulga as vagas de emprego e estágio disponibilizadas CEFET/RJ. O design da página web faz alusão a um mural com vários papéis pequenos usados no dia a dia chamados de “post-its”. Utilizando essa dinâmica, nesses papéis estão contidos, para cada vaga: o nome da empresa(resumido), o tipo de vaga e um QrCode que contém o endereço online de cada vaga e seus respectivos detalhes.
Nesta página, o tempo de exibição de vagas será determinado em função da quantidade de vagas de um curso específico, para contemplar todos os cursos do CEFET. Exemplo: o usuário configura 10 segundos para cada vaga e o curso de mecânica possui 6 vagas, logo, levará 1 minuto (60 segundos) para exibir todas as vagas deste curso. Depois que um curso exibe todas as suas vagas, a página recarrega e exibe as vagas de outro curso.
Há a rolagem automática da página caso o espaço de exibição das vagas exceda o espaço da tela.
Para acessar cada vaga, o usuário, munido de um aplicativo de leitor de QrCode do seu smartphone, acessa a página de descrição da vaga online. Esta página é responsiva, ou seja, ela adapta o seu tamanho a diferentes dispositivos como: smartphones, tablets e computadores de diferentes resoluções.

# Configuração
As vagas da página são originárias de um arquivo .json pré-formatado e
inserido no arquivo de configuração. Seguem abaixo os parâmetros e as
especificações para a configuração da página:
![arquivo de configuração](../imagens/imagem1.png)
Respeite as resoluções dadas. Há, também, a opção de inserir o relógio e a data.
Ao abrir a página no navegador, sem parâmetros na url, note que a aparece um “pop-up”. Ele permite que o usuário confgure a ordem de exibição das vagas por cursos. Há duas opções de exibição: rodízio e sem rodízio.
![setup](../imagens/imagem2.png)
Baseado no arquivo .json, são extraído todas os cursos das vagas e seus respectivos índices na url, podendo variar de acordo com cada arquivo.
![cursos](../imagens/imagem3.png)
Selecione um curso específco, depois, clique em “Continuar rodízio de vagas” ou em “Interromper rodízio de vagas” e clique em “Confirmar”. Se o usuário clicar em “Continuar rodízio de vagas”, as vagas serão exibidas na ordem descrita da caixa deseleção contando o tempo configurado. Se o usuário clicar em “Interromper rodízio de vagas”, só será exibida as vagas daquele curso sem transição. Em ambos os casos, se o usuário quiser mudar essa configuração a qualquer momento, basta clicar na imagem do logo da instituição presente no cabeçalho e aparecerá o “pop-up”. Quando o logo for clicado, o rodízio de vagas será interrompido, sendo necessário o usuário reativá – lo.
É possível configurar a exibição de vagas pela URL do navegador. Antes de configurar, é preciso conhecer os índices(números) dos cursos. Usando o exemplo da figura 3, temos o curso de mecânica com índice 0. Para confgurar a exibição das vagas de mecânica e deixar a exibição apenas nelas, siga o exemplo da figura abaixo:
![url sem modal](../imagens/imagem4.png)
Caso o usuário queira iniciar o rodízio começando por um curso específico, ele irá digitar o índice e escreverá “rodizio=continuou”. Na figura 4, só as vagas de mecânica estarão na tela. Neste exemplo, o “pop-up” aparecerá logo que a página recarregar. Caso não queira que isto aconteça, faça conforme a figura abaixo:
![url com modal](../imagens/imagem5.png)
Vale ressaltar, que se houver alguma falha na digitação desses comandos,
acarretará em algum comportamento indesejado do sistema.
© Copyright - CEFET/RJ

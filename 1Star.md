# *Juice Shop (Estrela 1)*

### Universidade Federal do Amazonas
#### Lucca Dourado Cunha - 22051490

Neste relatório será feito a primeira atividade do Juice Shop para a matéria de Segurança de Redes de Computadores ministrada pelo professor Eduardo Feitosa, que tem a finalidade de concluir todos os desafios de 1 Estrela da Aplicação Juice Shop do OWASP ([OWASP Juice Shop | OWASP Foundation](https://owasp.org/www-project-juice-shop/)).

Abaixo temos um Overview dos desafios completos no trabalho.

![Overview dos desafios](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/1Star.png?raw=true)

## Score Board

Para completar esse desafio apenas abri o DevTools do Google Chrome e procurei pelo caminho do "score-board" no arquivo main,js.

![Buscando endpoints no arquivo JS](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/scoreboard.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/scoreboardDone.png?raw=true)

## DOM XSS

Para completar esse desafio utilizamos a injeção de HTML por meio da barra de busca. Isso é possível pois após a busca ser realizada o valor buscado é retornado como elemento da página ao lado do campo "Search Results". Abaixo vemos na imagem o alerta sendo executado.

![Alerta sendo executado após a injeção](https://raw.githubusercontent.com/LuccaDC/ArtefatosSRC/main/1%20Star/DomXss.png)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/DomXssDone.png?raw=true)

## Bonus Payload

Processo deste desafio é exatamente o mesmo do anterior. A diferença agora é só o que é passado para injetarmos, que no caso é um player do SoundCloud com um jingle do Juice Shop.

![Payload sendo Executado](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/BonusPayload.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/BonusPayloadDone.png?raw=true)

## Privacy Policy

Neste simples desafio temos que apenas acessar a página de Privacy Policy, cujo caminho está mostrado na imagem abaixo.

![Caminho para a pagina de privacy policy](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/PrivacyPolicy.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/PrivacyPolicyDone.png?raw=true)

## Bully Chatbot

Neste desafio temos que conseguir um cupom de desconto do chatbot do site. Para concluir esse desafio tive apenas que "spammar" a mensagem solicitando um cupom, cujo ele me retornou após algumas tentativas.

![Chatbot retornando o cupom.](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/BullyChatbot.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/BullyChatbotDone.png?raw=true)

## Confidential Document

Este desafio foi um pouco mais complicado. É dado a dica para verificar locais onde a o site retorna arquivos diretamente, e é o que achamos na página "About Us". Por meio desse arquivo vemos que o site possui um caminho chamado de FTP, logo conclui-se que o site possui um FTP Server para distribuição de arquivos.

![Página mostrando o FTP](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ConfidentialDocument3.png?raw=true)

Seguindo o caminho do FTP vemos que as suspeitas estavam corretas e os arquivos estão expostos nesse caminho.

![Acessando o FTP do site](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ConfidentialDocument.png?raw=true)

Por fim ao acessar o arquivo acquisitions.md vemos o arquivo confidencial citado pelo desafio.

![Conteúdos do arquivo confidencial](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ConfidentialDocument2.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ConfidentialDocumentDone.png?raw=true)

## Error Handling

Para concluir este desafio apenas acessei o meu perfil e tentei colocar uma animação com a extensão "svg" como foto de perfil. Então o seguinte erro foi exibido e o desafio concluído.

![Erro exibido](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ErrorHandling.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ErrorHandlingDone.png?raw=true)

## Exposed Metrics

Para concluir esse desafio precisamos acessar as métricas geradas pela aplicação Prometheus. Verificando a documentação do Prometheus vemos que o caminho padrão para essas métricas é ".../metrics". Acessando então o endereço informado chegamos a tela abaixo e o desafio é concluído.

![Métricas apresentadas pelo site ](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ExposedMetrics.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ExposedMetricsDone.png?raw=true)

## Mass Dispel

Para concluir esse desafio basta fechar mais de uma notificação do Juice Shop ao mesmo tempo. Fazemos isso clicando no "X" da notificação como ilustrado abaixo enquanto seguramos a tecla Shift.

![Notificações](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/MassDispel.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/MassDispelDone.png?raw=true)

## Missing Enconding

Para concluir esse desafio, como informado pela dica, devemos ir na página "Photo Wall" e corrigir a imagem que não carrega corretamente. Ao inspecionar a página vemos que o caminho da imagem é : "/😼-#zatschi-#whoneedsfourlegs-1572600969477.jpg", esse caminho além de conter um Emoji possui também o símbolo "#". Logo para corrigir o erro devemos encodar esses símbolos especiais, produzindo o caminho: "/%f0%9f%98%bc-%23zatschi-%23whoneedsfourlegs-1572600969477.jpg", que no fim resolve o problema como mostrado nas imagens abaixo.

![Mostrando o endereço da imagem corrigida](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/MissingEncoding.png?raw=true)

![Página com a imagem reparada](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/MissingEncoding2.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/MissingEncodingDone.png?raw=true)

## Outdated Allowlist

Para concluir esse desafio devemos encontrar os endereços de pagamento por crypto descontinuados pelo site. Por isso novamente acessei o main.js e busquei por links de redirecionamento no código, que trouxe resultados como mostrado abaixo. Acessando esses redirecionamentos conclui esse desafio.

![Redirecionamentos encontrados](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/OutdatedAllowlist.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/OutdatedAllowlistDone.png?raw=true)

## Repetitive Registration

Para concluir esse desafio como sugerido pela dica devemos enviar os campos de "Password" e "Repeat Password" com valores diferentes de forma que seja aceito pelo site. Para isso utilizei a ferramenta Burp Suite e capturei o pacote de registro de um novo usuário, acessei o JSON contendo as informações do cadastro e alterei o valor "PasswordRepeat" para um diferente do "Password" e o enviei. O pacote foi prontamente aceito pelo site e o desafio marcado como concluído 

![Pacote de registro](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/RepetitiveRegistration.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/RepetitiveRegistrationDone.png?raw=true)

## Web3 Sandbox

Para concluir esse simples desafio seguimos os mesmos passos do primeiro desafio "Score Board". Buscamos dentro do main,js o caminho para a página requisitada e, como mostrado na imagem abaixo, a encontramos com sucesso.

![Caminho dentro do código main.js](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/Web3Sandbox.png?raw=true)

![Página solicitada no desafio](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/Web3Sandbox2.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/Web3SandboxDone.png?raw=true)

## Zero Stars

Por fim para esse último desafio utilizamos novamente o Burp Suite para capturar o pacote de feedback da loja, para que possamos alterar o valor de rating do pacote, visto que pela interface não foi possível alterar esse valor para 0. Então o site aceita o pacote com o valor alterado sem problema algum e o ultimo desafio é marcado como concluído.

![Imagem do pacote capturado e alterado pelo Burp Suite](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ZeroStars.png?raw=true)

![Desafio Feito!](https://github.com/LuccaDC/ArtefatosSRC/blob/main/1%20Star/ZeroStarsDone.png?raw=true)

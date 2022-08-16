# B-Health

## Backend
Você é o novo tech lead da squad que cuida do sistema de agendamento de exames, que está com os seguintes problemas:

1) Diariamente todos os hospitais enviam via FTP um arquivo para atualizar os exames, que são processados por um robô que faz a classificação e inclusão no banco de dados. Neste processo ocorrem diversos erros, como processamento de arquivos muito grandes, concorrência de I/O, falha no upload/download do arquivo, que deixam os exames desatualizados. Ficou definido com os hospitais que a comunicação não deverá mais ser feito por arquivos.
   
   - Qual solução você daria para essa integração? Descreva a solução e a arquitetura que você faria.


2) Existe um front-end que o cliente final pode agendar exames, realizar o pagamento e consultar os dados do hospital. Da forma que foi construída, cada consulta dos exames abre uma conexão com o banco e nosso banco permite até 100 conexões simultâneas. Com novos hospitais sendo integrados, hoje já tem mais de 1000 usuários acessando o site ao mesmo tempo, com muitas reclamações de performance e erros de consulta. 
   
   - Qual solução você daria para que suporte o aumento contínuo de usuários simultâneos, sem envolver alguma alteração de hardware (servidores e bancos)? Descreva a solução e a arquitetura que você faria.


3) Pensando nas soluções propostas dos itens anteriores, quais boas práticas você aplicaria no processo de entrega em produção, pensando nos conceitos de disponibilidade, qualidade e segurança?


## Frontend
O setor de exames clínicos do hospital conta com a participação de diversos laboratórios parceiros, que executam diversos tipos de exames necessários para a operação do hospital. Dependendo do tipo de exame executado, o layout de apresentação do laudo deverá ser diferente. Por exemplo, exames de sangue de rotina apresentam todos os resultados obtidos em formato tabular, enquanto uma biópsia de tecidos celulares apresentam os resultados em gráficos e textos descritos pelo médico responsável pela análise.

Nosso time de frontend precisa construir o sistema de geração dos laudos médicos, a partir das informações dos resultados processados pelos laboratórios. As seguintes premissas precisam ser levadas em consideração:

  - Uma mesma linha visual deverá ser utilizada para apresentar os resultados dos exames. Nosso time de UX/UI está trabalhando nas representações dos resultados.
  - Apesar de diversos layouts diferentes de apresentação dos resultados, a maioria destes exames contam com estruturas semelhantes de representação dos dados, como tabelas, gráficos, diagramas das regiões anatômicas analisadas, etc.
  - os laudos poderão ser consumidos através de interface web ou impressas, em documentoss PDF.
  - todos as informações necessárias para a geração dos diversos laudos, assim como um identificador único para cada laudo, foram processados pelo time de backend, e estão disponíveis para consumo pelo frontend.
  - estima-se que teremos aproximadamente 250 layouts diferentes.


1) Descreva uma proposta de arquitetura a ser utilizada para a criação deste sistema, levando em consideração todas as questões descritas acima. Alguns detalhes que devem ser considerados:
  
  - Como organizar todos os componentes necessários para a geração dos laudos? Leve em consideração a existência de diferentes laudos e a possibilidade de reaproveitamento de estruturas, entre eles.
  - Dada a quantidade de diferentes layouts existentes e a possibilidade de novos exames serem incluídos no painel do hospital, como garantir que o sistema possa ser expandido, para a geração desses novos layouts?
  - Na geração dos laudos em formato PDF, todas as páginas devem ter em seu rodapé informações do hospital, laboratório responsável pela análise e página do laudo. Como garantir que este laudo tenha estas informações?


2) Sua squad conta ainda com a participação de outros três desenvolvedores, que te auxiliarão na construção desta variedade de layots necessários. Descreva as abordagens que você utilizaria para:
  
  - Otimizar o trabalho do time, reduzindo impedimentos de trabalho entre os integrantes
  - Garantir a devida organização e qualidade do código produzido, considerando que teremos pessoas com mais e menos experiência integrando o time.
  - Evitar que os integrantes do time repliquem estruturas semelhantes, que poderiam ser reaproveitadas entre os layouts.


3) O sistema de geração dos laudos médidos, precisará ser incorporado ao sistema de operação do setor de medicina laboratorial do hospital. As equipes que já trabalham neste sistema vêm apresentando dificuldades de dar manutenção neste sistema, devido ao tamanho do projeto em si. Algumas das reclamações são: 
  
  - o build da aplicação demora demais durante o deploy
  - os testes têm demorado muito, inviabilizando o uso em período de desenvolvimento
  - a aplicação consome muito recurso de CPU e RAM, durante o desenvolvimento.

Precisamos projetar uma nova estrutura para este sistema, a começar pelo módulo de laudos médicos. Qual solução você nos recomendaria, para integrar esta aplicação ao sistema, levando em conta este cenário?



## Mobile
Você é o novo tech lead da squad que cuida do sistema de agendamento de exames, que está com os seguintes problemas:

1) Nosso time de desenvolvimento cresce a cada dia e a quantidade de funcionalidades também, com isso o tempo de build está cada vez maior impactando na performance de desenvolvimento.
Decidimos que será necessário modularizar o app para que possamos reduzir o tempo de build no dia a dia dos times. Temos 4 times principais (Agendamentos, Pagamentos, Campanhas e Segurança), qual solução você daria para essa modularização, visando:
  
  - Reduzir o tempo de build
  - Reduzir dependencias entre os times
  - Reaproveitamento de layouts
Desenhe a solução mostrando como cada modulo se comunica se necessário. Como serão feitas as chamadas de API de cada modulo? Como geramos as versões de testes e produção? Você considera que este é um bom caminho, cite os ganhos e perdas com essa estrategia.


2) Semanalmente alguns hospitais fazem campanhas de consentização de alguns exames. Ex: Outubro Rosa, Novembro Azul.
Mas por causa do tempo de publicação na loja, nunca conseguimos iniciar e finalizar a campanha na data certa.
Qual solução você daria para esse problema? Descreva a solução e a arquitetura que você faria.


3) Pensando em um time de desenvolvimento onde os membros possuem autonomia no código e trazem diferentes visões de práticas e soluções para pequenos e grandes problemas.
Como você atuaria para manter a qualidade do código e uma sinergia de padrões para facilitar na manutenção desde projeto.
Cite as boas práticas, processos e ferramentas que você poderia utilizar para resolver esse problema.


## Algumas informações extras:

- Para os desenhos de solução, você pode utilizar ferramentas como draw.io ou lucidchart ou até o Paint.
- A documentação pode ser entregue em um arquivo texto ou Word.
- Não é necessário codificar as soluções, mas caso tenha interesse, podem ser desenvolvidas em qualquer linguagem ou framework.
- Para entrega das suas respostas, mande um email para luis.ramos@bancobmg.com.br com o titulo "Processo Seletivo | Especialista Tech Lead | Entrega Desafio", as documentações em anexo e o link do repositorio, caso tenha.

Boa sorte.

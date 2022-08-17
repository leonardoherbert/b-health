# B-Health

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


## Algumas informações extras:

- Para os desenhos de solução, você pode utilizar ferramentas como draw.io ou lucidchart ou até o Paint.
- A documentação pode ser entregue em um arquivo texto ou Word.
- Não é necessário codificar as soluções, mas caso tenha interesse, podem ser desenvolvidas em qualquer linguagem ou framework.
- Para entrega das suas respostas, mande um email para luis.ramos@bancobmg.com.br com o titulo "Processo Seletivo | Especialista Tech Lead | Entrega Desafio", as documentações em anexo e o link do repositorio, caso tenha.

Boa sorte.

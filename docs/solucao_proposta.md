# 2. Solução Proposta


## 2.1 Objetivo Geral do Produto 


O objetivo geral do produto é tornar mais eficiente o acompanhamento individual do uso do tempo e da constância do usuário em atividades de estudo, trabalho, lazer e projetos pessoais, por meio de uma aplicação web de uso pessoal, executada no navegador do computador, capaz de centralizar o registro de sessões, o histórico, as estatísticas e os elementos de motivação em um ambiente de escritório virtual gamificado.

A solução busca reduzir a dispersão das informações utilizadas no acompanhamento da rotina, que hoje dependem de anotações soltas e da memória do usuário, facilitando o acesso aos dados relevantes e permitindo que o usuário visualize de forma organizada quanto tempo dedica a cada atividade e a cada categoria.

Como recurso complementar ao registro de tempo, a solução também contará com um ambiente visual em formato de escritório, composto por salas temáticas, estações associadas a cada atividade e um personagem controlado pelo usuário. Esse ambiente é acompanhado por mecanismos de gamificação, como moedas, sequência de dias, metas e conquistas, que recompensam a dedicação registrada. Esse recurso não tem como objetivo substituir o planejamento nem a disciplina do usuário, mas complementar o acompanhamento realizado por meio do registro de sessões, tornando a rotina mais motivadora.

Dessa forma, o produto pretende oferecer um ambiente único para registro, acompanhamento e motivação, mantendo os dados sob controle do próprio usuário, armazenados localmente e com possibilidade de backup, e respeitando as particularidades de sua rotina.


## 2.2 Objetivos Especifícos (OE) do Produto 


- *OE1* - Registrar de forma simples o tempo dedicado a estudo, trabalho, lazer e projetos sociais.

- *OE2* - Aumentar a constância e a motivação por meio de elementos de jogo (moedas, sequência, metas, conquistas).

- *OE3* - Dar visibilidade de como o tempo é distribuído entre atividades e categorias.

- *OE4* - Oferecer um ambiente visual agradável e personalizável, em formato de escritório.

- *OE5* - Manter os dados sob controle do usuário, locais e com backup.


## 2.3 Características do Produto 


| OE principal | ID | Contribuição secundária | Característica do Produto | Descrição resumida | Valor de negócio principal |
|---|---|---|---|---|---|
| OE1 | CP1 | OE4 | Gestão de atividades e estações | Permitir o cadastro, a edição e o arquivamento de atividades, cada uma associada a uma categoria e representada por uma estação no escritório virtual. | Organizar as atividades da rotina em categorias, de forma simples e visual. |
| OE1 | CP2 | OE3 | Registro de sessões | Permitir o registro do tempo dedicado a cada atividade por meio de timer ou de lançamento manual, com nota opcional e possibilidade de correção. | Reduzir o esforço de registrar o tempo e evitar a perda de informações da rotina. |
| OE2 | CP3 | OE1 | Moedas e sequência de dias | Conceder moedas proporcionais ao tempo registrado e contabilizar os dias consecutivos com atividade. | Reforçar o hábito de registrar e estimular a constância no dia a dia. |
| OE2 | CP4 | OE3 | Metas e conquistas | Permitir a definição de metas diárias e semanais e conceder conquistas por marcos atingidos. | Dar direção ao uso do tempo e reconhecer o progresso ao longo da jornada. |
| OE3 | CP5 | OE1 | Histórico de sessões | Reunir as sessões registradas em um histórico filtrável por dia, semana, atividade e categoria. | Facilitar a consulta e a revisão do que foi feito em cada período. |
| OE3 | CP6 | OE2 | Estatísticas de tempo | Apresentar o tempo dedicado por atividade e categoria, por dia e por semana, na tela "Meu dia". | Apoiar a percepção de como o tempo está distribuído e onde ajustar a rotina. |
| OE4 | CP7 | OE2 | Escritório virtual e navegação | Apresentar um escritório 2D em pixel art com quatro salas temáticas ligadas por um corredor, navegável pelo usuário e com ciclo de dia e noite. | Tornar o acompanhamento da rotina mais agradável e motivador. |
| OE4 | CP8 | OE2 | Personagem e personalização do ambiente | Oferecer um personagem com poucas opções de aparência e estados visuais, além da decoração das estações e salas com as moedas conquistadas. | Dar identidade ao ambiente e uma recompensa visual para a dedicação registrada. |
| OE5 | CP9 | OE1 | Armazenamento local e persistência | Salvar automaticamente os dados no próprio computador e preservar o timer em andamento caso a aba seja fechada ou recarregada. | Garantir que os registros não se percam e que o usuário mantenha o controle dos seus dados. |
| OE5 | CP10 | OE1 | Backup de dados | Permitir exportar e importar todos os dados em um arquivo, para guardar cópias e restaurar o histórico. | Proteger o histórico contra perdas e permitir a migração entre computadores. |
 

## 2.4 Tecnologias a Serem Utilizadas


O desenvolvimento do produto será realizado com tecnologias voltadas para aplicações web, executadas diretamente no navegador do computador do usuário, sem a necessidade de servidor ou de conexão contínua com a internet. A escolha considerou o caráter pessoal da solução, a necessidade de renderizar um ambiente visual 2D em pixel art e a possibilidade de evoluir o produto de forma gradual.

| Tecnologia | Categoria | Finalidade no projeto |
|---|---|---|
| TypeScript | Linguagem | Desenvolvimento de toda a lógica da aplicação, com tipagem estática para reduzir erros e facilitar a manutenção e a evolução do código. |
| Phaser | Framework de jogos 2D | Renderização do escritório virtual, dos sprites e das animações do personagem, da movimentação pelo ambiente e do ciclo de dia e noite. |
| Vite | Ferramenta de build | Servidor de desenvolvimento e empacotamento da aplicação para execução no navegador. |
| HTML5 e CSS3 | Interface | Construção dos painéis sobrepostos ao ambiente, como o timer, o cadastro de atividades, o histórico e as estatísticas. |
| Web Storage API (localStorage) | Armazenamento local | Persistência dos dados no próprio computador, incluindo atividades, sessões, moedas e o timer em andamento, com possibilidade de evolução para IndexedDB caso o volume de dados exija. |
| JSON | Formato de dados | Estrutura dos dados armazenados e dos arquivos de exportação e importação utilizados no backup. |
| Node.js e npm | Ambiente de desenvolvimento | Execução das ferramentas de desenvolvimento e gerenciamento das dependências do projeto. |
| Git e GitHub | Versionamento | Controle de versões do código e registro do histórico de evolução do projeto. |
| Visual Studio Code | Editor de código | Ambiente de edição e depuração durante o desenvolvimento. |
| Aseprite ou Piskel e Tiled | Arte e mapas (opcionais) | Edição de sprites em pixel art e montagem de mapas de salas, caso seja necessário adaptar ou criar elementos visuais próprios. |

Os elementos visuais (tilesets e sprites) poderão ser obtidos de bibliotecas de assets gratuitas, como o itch.io e o OpenGameArt, respeitando as licenças de uso e registrando os créditos correspondentes.

A solução não utilizará servidor, banco de dados externo nem mecanismos de autenticação, uma vez que se destina ao uso individual e mantém todos os dados no computador do usuário. A aplicação será executada nas versões atuais dos navegadores Chrome, Firefox e Edge.


## 2.5 Viabilidade da Proposta


A análise de viabilidade avalia se o produto proposto pode ser construído e mantido com os recursos disponíveis, considerando os aspectos técnico, operacional, de prazo e escopo e legal. Por se tratar de um projeto de uso pessoal, desenvolvido de forma individual, a análise considera a realidade de um único desenvolvedor, que também é o usuário final.

### 2.5.1 Viabilidade técnica

A proposta é tecnicamente viável. Todas as tecnologias previstas na Seção 2.4 (TypeScript, Phaser, Vite, HTML5, CSS3 e Web Storage API) são amplamente documentadas, possuem comunidade ativa e são executadas diretamente no navegador, sem exigir infraestrutura de servidor. O Phaser oferece de forma nativa os recursos centrais do produto, como renderização de sprites, animações, tilemaps, câmera e entrada do teclado, o que dispensa o desenvolvimento de um motor gráfico próprio.

O armazenamento local atende ao volume de dados esperado, composto por atividades, sessões, moedas e configurações de um único usuário, e o backup em arquivo JSON mitiga o risco de perda de dados por limpeza do navegador. O principal ponto de atenção técnico é a curva de aprendizado do Phaser e do desenvolvimento 2D, reduzida pela construção incremental do produto, que começa por uma sala e um personagem e evolui por etapas.

### 2.5.2 Viabilidade operacional

O produto é operacionalmente viável, pois será executado no navegador do computador do próprio usuário, sem instalação complexa, sem necessidade de cadastro ou login e sem dependência de conexão contínua com a internet. Não há equipe a treinar nem processo organizacional a adaptar. A rotina de uso (cadastrar atividades, iniciar o timer na estação, encerrar a sessão e consultar as estatísticas) é simples e foi pensada para exigir poucos passos. A manutenção se resume à evolução do código pelo próprio desenvolvedor e à realização periódica de backups pelo usuário.

### 2.5.3 Viabilidade de prazo e escopo

O escopo será dividido em etapas para garantir a entrega. A primeira etapa concentra as funcionalidades essenciais: escritório com quatro salas, personagem, cadastro de atividades, timer e registro manual, histórico, estatísticas, moedas, sequência de dias e backup. Metas, conquistas e decoração das salas ficam para uma etapa posterior. Essa divisão permite obter um produto funcional e utilizável antes de investir nos recursos de maior custo de desenvolvimento, e evita que o crescimento do escopo comprometa a conclusão. O prazo dependerá da disponibilidade de tempo do desenvolvedor, e a construção em etapas curtas permite ajustar o ritmo sem perder o que já foi entregue.

### 2.5.4 Viabilidade legal

Não há impedimentos legais. O produto não coleta nem compartilha dados pessoais de terceiros, pois todas as informações pertencem ao próprio usuário e ficam armazenadas no seu computador. As bibliotecas utilizadas possuem licenças que permitem o uso previsto. Os assets gráficos de terceiros deverão ter a licença verificada antes do uso, com registro dos créditos quando exigido, e o projeto não deve reproduzir material protegido de outros jogos ou produtos.

### 2.5.5 Riscos e mitigações

| Risco | Impacto | Mitigação |
|---|---|---|
| Crescimento do escopo (muitas ideias de gamificação) | Atraso ou abandono do projeto | Priorização por etapas e definição clara do escopo inicial. |
| Curva de aprendizado do Phaser | Atraso nas etapas iniciais | Desenvolvimento incremental, começando por uma sala e um personagem. |
| Falta de assets gráficos adequados | Visual inconsistente ou atraso | Uso de bibliotecas gratuitas, com opção de criar elementos próprios. |
| Licenças de assets incompatíveis | Impedimento de uso ou publicação | Verificação e registro das licenças antes da inclusão no projeto. |
| Perda de dados por limpeza do navegador | Perda do histórico do usuário | Salvamento automático e backup por exportação em JSON. |
| Falta de tempo do desenvolvedor | Atraso na entrega | Entregas curtas e funcionais ao final de cada etapa. |

### 2.5.6 Conclusão

Com base na análise, a proposta é considerada viável nos aspectos técnico, operacional, de prazo e escopo e legal. A simplicidade da infraestrutura e a divisão do escopo em etapas reduzem os riscos do projeto, e os principais pontos de atenção (escopo, aprendizado das tecnologias e licenças dos assets) possuem mitigações previstas.

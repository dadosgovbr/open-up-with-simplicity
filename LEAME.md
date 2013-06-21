Abra com simplicidade - desmistificando os dados abertos
===========================================================


> "A simplicidade é o último grau de sofisticação."
> Leonardo da Vinci

Antes de mergulhar nas ferramentas e metodologias mais aclamadas para a publicação de dados abertos, é importante voltarmos aos objetivos desse modelo de publicação: por que publicar dados abertos?
  
Publicar dados abertos é, antes de tudo, um esforço para tornar os dados mais fáceis de se utilizar e cruzar, de forma a tornar possível o uso por desenvolvedores. Nós não sabemos quem vai utilizar, nem sabemos com quais outros dados os nossos serão cruzados; daí a exigência de que os tornemos simples e bem documentados.
   
Nessa parte do curso o aluno será orientado a buscar a simplicidade para agilizar a publicação de dados e conhecer ferramentas que facilitam esse trabalho.

## Das Planilhas locais para dados na web ##

### Formatos ###

![Brinquedo de formas de crianças](http://4.bp.blogspot.com/-QmNc--UT8NM/UJGHobnbzDI/AAAAAAAAAXY/6_lVMxtrx-c/s1600/wooden_toy_shape_sorter_block_box.jpg)

Dentre as formas de se publicar dados abertos, a que consideramos mais simples é utilizar formatos de planilha. Abaixo, segue lista de formatos abertos para esta finalidade (exeção para xls e xlsx, que são fechados):
* [.csv](http://en.wikipedia.org/wiki/Comma-separated_values)
* [.tsv](http://en.wikipedia.org/wiki/Tab-separated_values)
* .txt (com tsv ou csv dentro)
* [.ods](http://en.wikipedia.org/wiki/OpenDocument)
* [.xls](http://en.wikipedia.org/wiki/Microsoft_Excel#Binary)
* [.xlsx](http://en.wikipedia.org/wiki/Office_Open_XML)

Como estamos falando de dados abertos, aconselhamos enfaticamente a publicação desses dados em formatos abertos (formatos que não impõem restrição tecnológica - [mais informações](http://opendefinition.org/)). Para exemplificar uma restrição tecnológica, pode-se imaginar uma situação em que um usuário do Corel Draw, por exemplo, (programa de criação/edição gráfica de imagens baseadas em vetores) tenta abrir um arquivo criado por esse programa, de extensão de arquivo do tipo "CDR", em um outro programa de vetores que não reconhece o formato Corel Draw.

Por fim, se queremos publicar dados em formatos simples e tamanhos pequenos, façamos como o <http://datos.gub.uy/> : csv compactado!

### Onde e porque ###

Como é de conhecimento de todos, o canal mais democrático e de maior permeabilidade da atualidade é a web! É na web que qualquer pessoa do mundo pode ter acesso aos dados que disponibilizamos com qualquer navegador.

![Tim Berners Lee](http://www.scientificamerican.com/media/inline/the-mind-behind-the-web_1.jpg)
&nbsp;
![WEB](http://www.pr-vantage.com/wp-content/uploads/2010/12/Web-Connection-300x232.jpg)

Considerando que queremos facilitar o trabalho dos nossos consumidores e que para isso selecionamos a web, é fundamental seguir [a sua arquitetura](http://www.w3.org/TR/webarch/) e algumas considerações do seu criador ([Sir Tim Berners Lee](https://en.wikipedia.org/wiki/Tim_Berners-Lee)) e de pesquisadores como [Roy Fielding](https://en.wikipedia.org/wiki/Roy_Fielding), que defendem sua utilização de forma simples e direta, ou seja:
* Disponibilizar arquivos em uma URL fixa, para que qualquer pessoa possa encontrá-los e compartilhá-los com terceiros;
* Não utilizar abstrações adicionais de outros protocolos, de modo a permitir que qualquer aplicação possa chegar ao arquivo sem maiores complicações.

Atualmente qualquer web service que siga o [estilo arquitetural REST](https://en.wikipedia.org/wiki/Representational_State_Transfer) ou ferramenta pronta de catalogação permite que se compartilhe dados em URLs que apontem diretamente para o dado.

Por último, pode ser vantajoso padronizar URLs de acesso aos arquivos de dados, uma vez que essa abordagem facilita o trabalho de crawlers, desenvolvedores, de mecanismos de busca e de muitas outras pessoas, quando procuram nossos dados.

Um grande exemplo de organização da informação nas URLs é o caso do governo do Reino Unido:

1. Página inicial do governo eletrônico do Reio Unido: <https://www.gov.uk/>
2. Página inicial para serviços de direção, transporte e viagens: <https://www.gov.uk/browse/driving>
3. Página inicial para serviços de trabalho e pensão: <https://www.gov.uk/browse/working>
4. Página inicial da parceria Reino Unido e Brasil: <https://www.gov.uk/government/world/brazil>

Esse exemplo não demonstra a organização nas URLs de conjuntos de dados, mas mostra que nas páginas do governo britânico existe na nomenclatura das páginas de serviços, uma padronização. Ainda mostra, além dessa padronização, a tentativa de agregar significado às URLs, para que elas sejam intuitivas para quem for utilizar.

## Catálogos de dados abertos e o CKAN ##

Para facilitar o processo de busca dos dados publicados em formatos abertos, utilizamos catálogos de dados abertos. 

A única descrição encontrada sobre o que é um catálogo de dados está aqui: <http://www.w3.org/TR/vocab-dcat/#class-catalog>

> "A data catalog is a curated collection of metadata about datasets."
> W3C

Considerando que essa foi a única definição encontrada, vamos criar a nossa:

Um catálogo de dados abertos é um mecanismo, ferramenta ou serviço que faz a gestão e publicação na web de dados abertos e seus metadados, ou ainda somente esses metadados (em casos nos quais os dados estão hospedados em outro lugar).

A funcionalidade básica de um catálogo de dados é então permitir: a busca, inclusão, alteração e exclusão desses metadados. 
As soluções de catálogo mais conhecidas, no entanto, têm incorporado cada vez mais funcionalidades:
* Integração com [sistemas de gestão de conteúdo](http://en.wikipedia.org/wiki/Content_management_system) (CMS como [wordpress](http://en.wikipedia.org/wiki/WordPress), [joomla](http://en.wikipedia.org/wiki/Joomla), [drupal](http://en.wikipedia.org/wiki/Drupal), [plone](http://en.wikipedia.org/wiki/Plone_(software)), etc.) ou ter seus próprios sistemas de gestão de conteúdo
* Possibilidade de visualização dos dados catalogados
* Controle de acesso a partes dos conjuntos de dados disponibilizados (acesso)
* Controle de acesso descentralizado para inclusão e edição de metadados, permitindo delegação por organizações e usuários
* Hospedagem de arquivos
* Transformação de arquivos
* APIs de acesso automatizado
* Harvesting de metadados e federação de catálogos

### Soluções conhecidas: ###

* Socrata ([Socrata](http://en.wikipedia.org/wiki/Socrata))
* Junar Open Data Platform ([Junar](http://www.junar.com/))
* [CKAN](http://ckan.org) ([Open Knowledge Foundation](http://okfn.org))

__Observações:__ 
* Essas são as soluções de mercado de maior destaque atualmente. Na verdade, devo esclarecer que são as únicas que conheço. Caso haja alguma outra que seja importante e eu não tenha colocado, por favor me avise!
* Não tive a oportunidade de testar as soluções Socrata e Junar como publicador, só como usuário.

### Socrata ###

![Socrata Home Page](https://photos-3.dropbox.com/t/0/AABQm3gFtyqC_n4b0ItX6PsjnJyMd4xvgjw5kUVaN_wFPQ/12/18364240/jpeg/32x32/3/_/1/2/Socrata.jpg/EzWsMsnxRmWMvrnTfhzXD2fGj-Xla1oQL9rpQ9-TbGs?size=1024x768)

#### Principais características ####
* Sotware como serviço
* API para acesso automático
* Pré visualização de dados tabulares
* Construção de visualizações mais elaboradas (formatação condicional, gráficos e mapas)


#### Quem usa? ###
* [Kenya](https://opendata.go.ke/)
* [Programa de Desenvolvimento das Nações Unidas](http://www.undp.org/content/undp/en/home.html) <https://data.undp.org/>
* [Banco Mundial](https://finances.worldbank.org/)
* [Estados Unidos (até 2013)](http://www.data.gov/)
* [Dezenas de cidades e estados nos Estados Unidos e no Mundo](http://www.socrata.com/customer-spotlight/)

### Junar Open Data Platform ###

![Junar Home Page](https://photos-4.dropbox.com/t/0/AAD48ncEMfORhlltWE0fqrBgQMbK54mev3gF30gXqihWxQ/12/18364240/jpeg/32x32/3/_/1/2/junar.jpg/--5i3Cu53p3w4OtSY-uFZhUP0dT--67C7GqiPDpQOr0?size=1024x768)

#### Principais características ####
* Software como serviço
* API para acesso automático
* Pré visualização de dados tabulares
* Visualização de dashboards pré elaborados

#### Quem usa? ###
* [Chile](http://datos.gob.cl/)
* [Costa Rica](http://datosabiertos.gob.go.cr/)
* [6 municípios nos Estados Unidos e no Mundo](http://www.junar.com/plans)
* [La nación (Jornal da Argentina)](http://data.lanacion.com.ar/)

### CKAN ###

![CKAN Home Page](https://photos-6.dropbox.com/t/0/AABEWPFfd_5ML1NYOCqQR0JroGtLRr5X5fztfRICwBq9wQ/12/18364240/jpeg/32x32/3/_/1/2/ckan.jpg/knz_ahNH1kXW0wU4EC2W267_aw_pczSlevS9wbwyOr0?size=1024x768)

#### Principais características ####
* Sotware Open Source - <https://github.com/okfn/ckan>
* Software como serviço
* API para acesso automático
* Pré visualização de dados tabulares
* Construção de visualizações (gráficos e mapas)
* Busca de datasets geolocalizada

#### Quem usa? ###
* [Reino Unido](http://data.gov.uk/)
* [Estados Unidos](http://www.data.gov/)
* [Alemanha](https://www.govdata.de/)
* [public.data.eu](http://publicdata.eu/)
* [Brasil](http://dados.gov.br/)
* [Dezenas de países, estados e cidades no mundo](http://ckan.org/instances/)


## APIs - por que e como? ##

O que é uma API ?

API quer dizer Application Programming Interface (Interface de Programação de Aplicação).
> "Generally speaking, an application programming interface specifies how some software components should interact with each other."
> [Wikipedia](https://en.wikipedia.org/wiki/Application_programming_interface)

Ou seja, é um componente de interoperabilidade. Na prática uma API é uma biblioteca, em alguma linguagem de programação, que encapsula ou abstrai a uma rotina, interagimos com a API enviando a ela a operação que queremos fazer.

O que chamamos de APIs quando falamos de dados abertos, na verdade, são Web APIs. As web APIs funcionam sobre a mesma filosofia: é declarado um conjunto de operações que a API realiza e o desenvolvedor a chama utilizando HTTP, ou SOAP, mas recomendamos nos ater ao HTTP pela simplicidade que isso traz aos desenvolvedores.

Embora uma API seja uma maneira mais rica de publicar dados, recomendamos também considerar algumas questões antes de entrar de cabeça nessa moda ou durante seu processo de adoção.
> Fonte: [Publishing Open Data – Do you really need an API?](http://www.peterkrantz.com/2012/publishing-open-data-api-design/)

__Você realmente precisa de uma API ?__
* Você quer disponibilizar uma planilha ou uma base inteira ?
* Qual o tamanho da base ? Não seria mais fácil convertê-la para um grande arquivo ?
* Você pode arcar com os custos de manutenção de uma API?
* Sua infraestrutura aguentaria um grande aumento de carga ?

__Isole a base de produção da base aberta__
Essa afirmação pode parecer óbvia, mas nunca é demais lembrar coisas importantes. A parte de segurança não é tão arriscada, o principal problema é a concorrência das buscas com as atividades normais do sistema que está em produção.

__Lembre-se das URLs__
API boa é RESTful, é API padronizada, criar uma API que não siga as melhores práticas na web pode ser uma dor de cabeça para você e não atender as necessidades dos desenvolvedores.

### Como Fazer uma API ###

Infelizmente não existem maneiras fáceis e nem tempo hábil para colocar isso dentro de uma postagem.
O que pode e vai fazer muito mais diferença é incluir aqui agumas coisas que devem ser levadas em consideração ao se desenvolver (ou terceirzar o desenvolvimento de) uma API:
* [Arquitetura da Web](http://www.w3.org/TR/webarch/)
* [Estilo de arquitetura REST](http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)

Além disso, estamos pesquisando no Brasil, soluções de software livre que transformem bases em APIs com um conjunto de definições, já encontramos (e desenvolvemos) algumas, mas ainda não encontramos nenhuma com interface gráfica e de fácil configuração.


### Protocolo de interoperabilidade de catálogo de dados ###

Como já falamos de catálogos de dados e de APIs, trazemos essa novidade interessante: a Open Knowledge Foundation iniciou o desenvolvimento de um "Protocolo de Interoperabilidade para catálogo de dados":

[Data Catalog Interoperability Protocol](http://spec.datacatalogs.org/)
![OKFN's DCIP](https://photos-4.dropbox.com/t/0/AAANtsg7lmKJfZtd5Y0Z0JiR07oQVJ4huCRxrqvLivNS2Q/12/18364240/jpeg/32x32/3/_/1/2/DCIP.jpg/6XHdLEkNdUi5KZ0-07i5v4l7dlMQXx6J1CEWK8qbVTI?size=1024x768)

O protocolo propõe:
* A definição de representações comuns em JSON e RDF para entidades centrais de catálogos de dados; e
* Um protocolo somente de leitura para realizar a interoperabilidade básica entre catálogos;

Dessa forma, um catálogo central mundial poderia reunir todos datasets dos catálogos que seguissem esses padrões !

### Canais da comunidade e de aprendizagem ###

Há vários meios por onde entrar em contato com pessoas interessadas em dados
abertos, ficar por dentro do que está acontecendo e aprender mais sobre o
assunto.

Para os que dominam o idioma inglês, sugerimos a utilizar o sistema
de perguntas e respostas da "Escola de Dados" ou
"[_School of Data_](http://schoolofdata.org/)" da _Open Knowledge Foundation_:
<http://ask.schoolofdata.org/>, uma iniciativa nova onde já podem ser
encontradas muitas perguntas relevantes sobre dados abertos, dados e assuntos
correlatos. A Fundação também possui listas de discussão relacionadas à
[escola de dados](http://lists.okfn.org/mailman/listinfo/school-of-data) e a
[dados governamentais abertos](http://lists.okfn.org/mailman/listinfo/open-government).

Em idioma português, temos no Brasil a [lista do GT de Dados Abertos do
W3C](https://mail.nic.br/mailman/listinfo/gt-dadosabertos) e
as [listas de discussão da
INDA](http://wiki.gtinda.ibge.gov.br/Como-Participar-da-INDA.ashx), que são 5
listas. Uma para assuntos gerais e quatro assuntos específicos. Há ainda a
[lista de discussões da _Open Knowledge Foundation_ no
Brasil](http://lists.okfn.org/mailman/listinfo/okfn-br).

Em espanhol, a OKF mantém uma [lista sobre dados abertos para a América
Latina](http://lists.okfn.org/mailman/listinfo/okfn-latin-america) e
também listas focadas nos seguintes países:
[Argentina](http://lists.okfn.org/mailman/listinfo/okfn-ar),
[Equador](http://lists.okfn.org/mailman/listinfo/okfn-ec),
[Uruguai](http://lists.okfn.org/mailman/listinfo/okfn-uy) e
[México](http://lists.okfn.org/mailman/listinfo/okfn-mx).

## Licença ##

Todo o conteúdo deste repositório e deste curso está disponível sobre licença [Creative Commons Atribuição (by)](http://creativecommons.org/licenses/by/3.0/br/)

![CC-BY](http://creativecommons.org.br/wp-content/uploads/2012/08/by.large_.png)



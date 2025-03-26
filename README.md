# Azure AI Search

É uma solução de busca inteligente e escalável para aplicativos, sites e plataformas. Utiliza a inteligência artificial para melhorar a experiência de busca, tornando-a mais relevante e eficiente.

Para exemplificar esta solução, segue o passo a passo de como o serviço pode ser implementado na prática

Acessar o link https://portal.azure.com/
Após logado, selecionar a opção criar um recurso.
![image](https://github.com/user-attachments/assets/22d8f29b-208f-4ea9-bf47-d5a9c0c3e7e2)

Selecionar a opção Azure AI Search e clicar em Criar.

![image](https://github.com/user-attachments/assets/871a89e8-fb32-437c-bc57-f115515df9c1)

Na próxima tela, na opção de grupo de recursos, se não existir, clicar em Criar novo.
![image](https://github.com/user-attachments/assets/8462b69a-0e0f-490a-867c-3435385e6214)

![image](https://github.com/user-attachments/assets/eb2cfb32-c264-4d53-9814-ba3b7fe9a11a)

Na opção de tipo de preço, selecionar básico e clicar em select.
![image](https://github.com/user-attachments/assets/6d9aaabc-b3dc-4e87-b9ff-643d4dcd13c1)

Ao retornar para a tela anterior, selecionar Revisar + Criar.

![image](https://github.com/user-attachments/assets/5a1220d7-a9a6-4810-b084-6778327ce409)

Na próxima tela, selecionar Criar.

![image](https://github.com/user-attachments/assets/fd11a4d2-950c-4f8b-8a8b-d18c29319aab)

Após a implantação, aparecerá a janela abaixo. 
![image](https://github.com/user-attachments/assets/dc95ba28-349b-4e21-aaac-11a3f04f20e6)

Retornar para a página inicial para criação de recurso de serviço do AI Search. Selecionar a opção Azure AI Services e clicar em criar.
![image](https://github.com/user-attachments/assets/5aa589c0-8d96-4243-9f97-354d2f8b3d89)

Na opção grupo de recursos, escolher o que foi configurado anteriormente, e em Instance Details criar um nome exclusivo, e em pricing tier escolher a opção Standard S0. Clicar em Examinar + criar.

![image](https://github.com/user-attachments/assets/3c6afe09-3a31-4923-b95a-c0061f0eb042)

Depois de ver a resposta Validação aprovada, selecione Criar.

![image](https://github.com/user-attachments/assets/549bc9b2-f90a-4740-9640-d934bd5c2513)

Retornar a página inicial do portal do Azure e selecionar a opção + Criar um recurso. Pesquisar a conta de armazenamento e criar um recurso de conta de armazenamento
![image](https://github.com/user-attachments/assets/4666bd6b-e651-487e-983a-b43456271c65)

Na opção grupo de recursos, selecionar a opção criada anteriormente. Em detalhes da instância, escrever um nome exclusivo para armazenamento, em serviço primário escolher a opção "Armazenamento de Blobs do Azure",  e em redundância selecionar a opção LRS. Após as configurações, selecionar Examinar + criar.

![image](https://github.com/user-attachments/assets/595569e1-fde8-4d56-ad22-271ff16dab58)

Na próxima tela, selecionar criar.

![image](https://github.com/user-attachments/assets/2015e886-4cbf-451d-8c1f-c1366d3c55a1)

Aguardar a conclusão da implantação e ir para o recurso implantado.

![image](https://github.com/user-attachments/assets/680f1201-ac77-4333-81b6-6f6a44d6e7af)

Na opção Configurações, selecionar a opção Configuração. Alterar a opção Permitir acesso anônimo ao Blob de desabilitado para habilitado, e clicar em salvar.

![image](https://github.com/user-attachments/assets/1bb801a4-48e6-4adc-b36b-3bec62e1910b)

Para carregar documentos no Azure, selecionar a opção Contêineres em Armazenamento de Dados e clicar em + Contêiner. Inserir o nome coffee-reviews e selecionar criar.
![image](https://github.com/user-attachments/assets/26a88209-3197-4353-b62e-d96a985b40fb)
![image](https://github.com/user-attachments/assets/5058169f-a949-449f-baf8-7a7bd8edf2df)

Acessar a pasta de avaliações https://aka.ms/mslearn-coffee-reviews e baixar as avaliações de café compactadas, e extrair os arquivos para a pasta de avaliações.
No portal do Azure, selecionar contêiner coffee-reviews. No contêiner, selecionar Carregar.

![image](https://github.com/user-attachments/assets/5a1b83e3-3945-4b26-a924-f371a30df949)

Selecionar os arquivos descompactados,e clicar em carregar.

![image](https://github.com/user-attachments/assets/fd184421-22f3-4224-a38e-e52b4d1bfebc)

![image](https://github.com/user-attachments/assets/b1c88ca4-a032-4d2c-b606-4b31bccf5c9a)

Após a concluir o carregamento, fechar o painel Carregar blob. Os documentos agora estarão no contêiner de armazenamento de avaliações de café.
Após o armazenamento, é possível utilizar o Azure AI Search para extrair insights dos documentos. O portal do Azure fornece um assistente de importação de dados. Com esse assistente, é possível criar automaticamente um índice e um indexador para fontes de dados com suporte. O assistente será usado para criar um índice e importar os documentos de pesquisa do armazenamento para o índice do Azure AI Search.
Retornar a página inicial e selecionar o recurso do Azure AI Search. Na página Visão geral, selecione Importar dados.

![image](https://github.com/user-attachments/assets/314247c0-5d14-4bb0-b954-81c5e8424fe1)

Na opção, Fonte de dados, selecionar Armazenamento de Blobs do Azure e preencher conforme mostrado na figura. 
![image](https://github.com/user-attachments/assets/aa36ba0d-cff1-4060-84b9-0bd0e3dacf93)

Na opção, Cadeia de conexão, selecionar: Escolher uma conexão existente. E selecionar a conta de armazenamento configurada.
![image](https://github.com/user-attachments/assets/19eaa6a6-0366-456e-b0c1-cb06dc1b262a)

Na próxima janela, marcar coffee-reviews e clicar em selecionar.
![image](https://github.com/user-attachments/assets/ed838a8c-9faa-445b-8d29-b1217e30bd25)

Para as próximas opções, escrever no item Descrição: Comentários sobre Fourth Coffee shops. E clicar em adicionar habilidades cognitivas. 

![image](https://github.com/user-attachments/assets/3e66a851-828c-4b30-abf9-df03d6f9d25c)
Na seção Adicionar enriquecimentos:
Alterar o nome do conjunto de habilidades para coffee-skillset e marcar a caixa de seleção Ativar OCR. O campo Dados de origem deverá estar definido como merged_content.
Alterar o nível de granularidade de enriquecimento para Páginas (partes de 5000 caracteres) e não selecionar Habilitar enriquecimento incremental.

![image](https://github.com/user-attachments/assets/6811c6e7-5dad-4f67-94d4-b98ee758f672)

Selecionar os campos enriquecidos conforme mostrado na figura.
![image](https://github.com/user-attachments/assets/be5a05f1-9e10-46c3-ac9d-6a1d5acacbfe)

Em salvar os enriquecimentos em um repositório de conhecimento, na opção Cadeia de conexão da conta de armazenamento. Selecionar escolher uma conexão existente.

![image](https://github.com/user-attachments/assets/048dd058-dddd-4270-b2dd-3d92a952ba3b)

Escolher a conta de armazenamento criada anteriormente.

![image](https://github.com/user-attachments/assets/af8b826b-822d-442c-ab2f-2f3814113de8)

Clicar em + Contêiner para criar um novo contêiner chamado knowledge-store com o nível de privacidade definido como Privado e selecionar Criar.

![image](https://github.com/user-attachments/assets/a62c7246-936c-4fba-aa4c-8913bef624f2)

![image](https://github.com/user-attachments/assets/27973c3b-bfb9-4ca4-ac7d-998e3e696205)

Selecionar o contêiner de armazenamento de conhecimento e clique em Selecionar na parte inferior da tela.

![image](https://github.com/user-attachments/assets/1a7d5065-d56d-4d75-b3a4-788e339695e0)

Selecionar Projeções de blob do Azure: Documento. Uma configuração para Nome do contêiner com o contêiner de armazenamento de conhecimento preenchido automaticamente é exibida. 
![image](https://github.com/user-attachments/assets/df81c522-873b-4564-b4c0-da90c9eb0eaf)

Selecionar Avançar: Personalizar índice de destino. Alterar o nome do índice para coffee-index. A chave deve estar definida como metadata_storage_path e o nome do Suggester deve ficar em branco. Selecionar filtrável para todos os campos já selecionados por padrão. Selecionar Avançar: Criar um indexador.
![image](https://github.com/user-attachments/assets/93790223-acd6-43d4-aeb9-020974d353a7)

Alterar o nome do indexador para coffee-indexer e deixar o Agendamento definido como Uma vez. Em opções avançadas, certificar que a opção Chaves de Codificação de Base 64 esteja selecionada, pois as chaves de codificação podem tornar o índice mais eficiente. Selecionar Enviar para criar a fonte de dados, o conjunto de habilidades, o índice e o indexador. 
Na página de recursos do Azure AI Search. No painel esquerdo, em Gerenciamento de Pesquisa, selecionar Indexadores. 
![image](https://github.com/user-attachments/assets/8111a257-6601-4af4-9575-d63b9073a7e0)

Selecionar o indexador de café recém-criado. 

![image](https://github.com/user-attachments/assets/0a14791c-d7e4-4655-95d8-4787d1cafbd4)

Atualizar até que o Status indique sucesso.

![image](https://github.com/user-attachments/assets/729c4b80-46c8-4af9-85d5-dcf3e1487f19)

Na página Visão geral do serviço de Pesquisa, selecionar Gerenciador de pesquisa na parte superior da tela.

![image](https://github.com/user-attachments/assets/92403615-d6ef-432d-904e-3b6953e824db)

O índice selecionado é o índice de café criado anteriormente. Abaixo do índice selecionado, alterar a exibição para JSON.

![image](https://github.com/user-attachments/assets/169681c6-582b-45ab-82dc-c26c1ff9bfa5)

No campo Editor de consultas JSON, copiar e colar o código mostrado na figura e clicar em pesquisar.

![image](https://github.com/user-attachments/assets/c35c745c-4421-4574-8dc2-74a7e969d3d8)

O índice de pesquisa deve retornar um documento JSON contendo os resultados da pesquisa.
![image](https://github.com/user-attachments/assets/f44a2416-ab0c-4841-86a5-9e83a059a2b5)

Realizar um novo filtro para localização.
![image](https://github.com/user-attachments/assets/e5e62663-e7cc-458b-a2fa-de4f9192661a)

A consulta pesquisa todos os documentos no índice e filtra as revisões com um local de Chicago.

![image](https://github.com/user-attachments/assets/d2134eae-ebb0-4386-9401-9326ac0031b3)

Realizar um novo filtro para sentimento.
![image](https://github.com/user-attachments/assets/9d01d82f-5c48-4f05-8b72-be50b49ba7ec)

A consulta pesquisa todos os documentos no índice e filtra as revisões com um sentimento negativo. Ao verificar as palavras chaves, pode-se deduzir o sentimento negativo devido a palavra chave "experiência terrível".

![image](https://github.com/user-attachments/assets/f79ffba3-0074-4810-bda7-66e96136fb65)


# Análise do repositório de conhecimento

No repositório de conhecimento, os dados enriquecidos extraídos pelas habilidades de IA são mostrados na forma de projeções e tabelas.

![image](https://github.com/user-attachments/assets/af4b6730-ead1-4744-9b05-9e163c705e50)

Na página iniciual, selecionar a conta de armazenamento e no paínel de menu à esquerda, selecionar Contêineres. Selecionar o contêiner de armazenamento de conhecimento.
![image](https://github.com/user-attachments/assets/bad8779e-5149-4715-8e4a-a72829291b3b)

Será exibida uma lista de pastas para todos os metadados de cada documento de revisão. Selecionar qualquer uma das pastas. Na pasta, clicar no arquivo objectprojection.json.

![image](https://github.com/user-attachments/assets/2f59de61-eabb-4313-8732-74f34948b440)

Selecione Editar para ver o JSON produzido para um dos documentos do armazenamento de dados do Azure.
![image](https://github.com/user-attachments/assets/b622e0b0-6f71-4d03-81e4-80dbcd1386f2)

Retornar aos Contêineres da conta de armazenamento. Selecionar o contêiner coffee-skillset-image-projection e selecionar qualquer um dos itens.

![image](https://github.com/user-attachments/assets/b41ea36b-b270-436c-a10e-63218fff6add)

Selecionar qualquer um dos .jpg arquivos e clicar em Editar para ver a imagem armazenada do documento. E observar como as imagens são armazenadas.
![image](https://github.com/user-attachments/assets/c266544a-68f4-473a-b206-ffcea63f3174)

No Navegador de armazenamento no painel esquerdo, selecionar Tabelas.Verificar que existe uma tabela para cada entidade no índice. As tabelas podem ser vinculdas como um banco de dados relacional. 

  ![image](https://github.com/user-attachments/assets/14450b5f-9803-45bf-bf2a-88132b2521a3)

  Observação: Nessa última parte é solicitado selecionar a tabela coffeeSkillsetKeyPhrases, para verificar as frases-chave que o repositório de conhecimento conseguiu capturar do conteúdo nas avaliações. Mas, a url dá um erro.
              Nãso esquecer de deletar as configurações para evitar cobranças.




























































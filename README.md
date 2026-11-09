Sistema Musical

Sistema Musical é uma aplicação web para organizar uma coleção de músicas. A ideia é simples: o usuário entra no sistema, cadastra artistas, cadastra as músicas de cada artista com o link do vídeo no YouTube e depois consulta tudo em uma biblioteca com busca e filtros.

Esta versão contém apenas a camada visual do sistema, construída com HTML e CSS puros. Ela serve como base para a futura ligação com um servidor e um banco de dados. Por isso, os formulários ainda não enviam dados para lugar nenhum e as tabelas mostram exemplos fixos.

O que o sistema oferece

Quem acessa o sistema passa primeiro pela tela de login e chega a um menu com três caminhos. O primeiro é o gerenciamento de artistas, onde se informa nome, gênero musical, país e uma foto. O segundo é o cadastro de músicas, onde se escolhe o artista e se informa título, álbum, gênero, link do YouTube, capa e letra. O terceiro é a biblioteca musical, que lista todas as músicas e permite procurar por título, álbum ou artista, além de filtrar por artista e por gênero.

Em todas as listas existem botões para editar e excluir cada registro. Na lista de artistas há ainda um botão que leva direto ao cadastro de músicas, e nas listas de músicas há um botão que abre o vídeo no YouTube em outra aba.

Arquivos

Todos os arquivos ficam juntos na mesma pasta.

login.html: tela de entrada com usuário e senha.
index.html: menu principal, com o botão de sair.
cadastro_artista.html: formulário de artista e tabela de artistas cadastrados.
cadastro_musica.html: formulário de música e tabela de músicas cadastradas.
listagem_musicas.html: biblioteca musical com filtros.
styles.css: folha de estilos usada por todas as páginas.
Como usar

Não há nada para instalar. Basta abrir o arquivo login.html em qualquer navegador moderno. Se preferir, é possível servir a pasta com uma extensão como o Live Server do VS Code ou com um servidor estático qualquer.

As credenciais de teste exibidas na tela de login são o usuário admin e a senha 123. Por enquanto o login não valida nada: qualquer preenchimento envia o formulário, que apenas recarrega a página. Para navegar pelo sistema, abra o index.html diretamente ou use os links das páginas.

Campos obrigatórios

No cadastro de artista, apenas o nome é obrigatório. No cadastro de música, são obrigatórios o artista, o título e o link do YouTube, que deve ser o endereço de um vídeo e não de um canal ou playlist. As imagens de foto e de capa são opcionais e devem ser JPG ou PNG com até 5 MB. Esse limite está indicado na interface, mas ainda não é verificado, pois não há servidor.

Sobre o visual

O estilo está todo no styles.css. Cores, sombras, arredondamento e fonte são definidos como variáveis no início do arquivo, então trocar o tema do sistema exige alterar poucas linhas. A interface se adapta a telas pequenas: abaixo de 768 pixels os formulários passam para uma coluna, as tabelas ganham rolagem horizontal e os botões ficam menores.

O arquivo também já inclui estilos para recursos que serão usados quando houver dados reais, como mensagens de sucesso e erro, miniaturas de imagem nas tabelas, pré-visualização da imagem atual na edição e o aviso de tabela vazia.

O que falta para ficar completo

O trabalho que resta é a parte de servidor. Será preciso escolher uma linguagem de back-end e um banco de dados, guardar usuários, artistas e músicas (cada música pertence a um artista), fazer o login funcionar de verdade com sessão e senha protegida e remover as credenciais de teste da tela de entrada. Também falta receber e armazenar as imagens enviadas, validar o link do YouTube, criar as telas de edição, pedir confirmação antes de excluir, carregar as listas de artistas e gêneros a partir do banco e fazer os filtros da biblioteca funcionarem.

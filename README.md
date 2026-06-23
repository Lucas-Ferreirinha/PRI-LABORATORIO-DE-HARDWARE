Laboratório VR Educativo

Este projeto é um ambiente de realidade virtual desenvolvido com A-Frame, com foco em ensino interativo sobre componentes de hardware de computadores.

O usuário explora um laboratório 3D, interage com objetos e responde quizzes para ganhar pontos.

Estrutura do sistema

O sistema é baseado em uma lista de componentes definida em JavaScript.

Cada componente possui as seguintes propriedades:

Nome
Descrição
Tipo (usado para imagem/identificação)
Link do quiz correspondente
Cor temática

Esses dados são armazenados em um array chamado COMPONENTES.

Estrutura dos componentes

Cada item segue o padrão:

name: nome do componente
desc: descrição educativa
type: identificador da imagem
link: página do quiz
color: cor do botão/interação
Geração automática

O sistema utiliza um loop:

COMPONENTES.forEach(...)

Esse loop cria automaticamente no cenário:

Base do objeto
Imagem do componente
Texto (nome e descrição dinâmica)
Botão de interação
Evento de clique para iniciar quiz

Esse modelo permite fácil expansão sem duplicação de código.

Interação no ambiente VR

A interação é baseada em olhar do usuário (gaze interaction):

O cursor utiliza fuse
O usuário olha para o objeto por 2 segundos
A ação é executada automaticamente

Isso permite uso sem teclado ou mouse.

Sistema de pontuação

A pontuação do usuário é armazenada usando localStorage.

Isso garante:

Persistência de pontos mesmo após recarregar a página
Continuidade da experiência
Possibilidade de evolução do usuário
Como adicionar novos componentes

Para adicionar um novo item ao laboratório, basta incluir um novo objeto no array COMPONENTES.

Exemplo:

name: Fonte de Energia
desc: Distribui energia para todos os componentes do computador
type: fonte
link: quiz_fonte.html
color: cor desejada
Requisitos para novos componentes

Ao adicionar um novo item, também é necessário:

Adicionar a imagem correspondente em a-assets
Criar o arquivo do quiz correspondente
Manter o padrão de nomenclatura consistente
Sistema de posicionamento

Os componentes são distribuídos automaticamente no cenário usando um array de posições:

POSICOES = [-7.5, -4.5, -1.5, 1.5, 4.5, 7.5]

Cada valor representa uma estação no laboratório.

Expansão do sistema

O sistema pode ser expandido facilmente:

Adicionando mais posições no array
Inserindo novos componentes no vetor
Criando novos quizzes associados

Não é necessário alterar a lógica principal.

Possíveis melhorias futuras
Sons interativos ao clicar
Animações nos objetos
NPCs educativos
Sistema de ranking
Partículas e efeitos visuais
Transições entre fases
Resumo

O projeto apresenta:

Ambiente VR educativo
Interação por olhar (gaze)
Sistema de quizzes integrado
Pontuação persistente
Estrutura modular e expansível
Interface 3D interativa
Observação

Projeto desenvolvido com fins educacionais utilizando tecnologias web como A-Frame e JavaScript, voltado para ensino de hardware de computadores em ambiente imersivo.
# 🧠 Laboratório VR Futurista IF

## 📌 Sobre o projeto

Este projeto é um **laboratório virtual em 3D (VR)** desenvolvido com **A-Frame (WebVR)** com o objetivo de ensinar de forma interativa os principais componentes de um computador.

O usuário pode explorar o ambiente, interagir com objetos olhando por 2 segundos e responder quizzes educativos sobre hardware.

---

# 🚀 Funcionalidades

- 🧑‍💻 Ambiente VR em 3D
- 🖥️ Componentes de computador interativos
- 👁️ Interação por olhar (cursor com fuse de 2 segundos)
- 🧪 Sistema de quizzes por componente
- 🏆 Sistema de pontuação salvo no navegador
- 🎨 Interface neon futurista

---

# ⚙️ Tecnologias usadas

- HTML5
- CSS3
- JavaScript
- A-Frame (WebVR)

---

# 🧱 Estrutura do projeto

index.html → Laboratório VR principal  
tutorial.html → Página inicial com instruções  
quiz_cpu.html → Quiz do processador  
quiz_gpu.html → Quiz da GPU  
quiz_ram.html → Quiz da memória RAM  
quiz_hd.html → Quiz do armazenamento  
images/ → Imagens dos componentes  

---

# 🧠 Como o código funciona

## 🌍 1. Cena VR

O ambiente é criado com:

<a-scene>

Dentro dele estão:
- luzes
- chão
- paredes
- componentes
- câmera

---

## 💡 2. Iluminação

O projeto usa:
- luz ambiente
- luz direcional
- luzes pontuais neon

Isso cria o efeito futurista do laboratório.

---

## 🖥️ 3. Componentes

Os componentes são definidos em um array JavaScript:

const COMPONENTES = [
  {
    name: "Processador",
    desc: "Executa instruções do computador.",
    type: "cpu",
    link: "quiz_cpu.html",
    color: "#38bdf8"
  }
];

Cada componente possui:
- nome
- descrição
- imagem
- link do quiz
- cor do tema

---

## 🔁 4. Criação automática

O código usa:

COMPONENTES.forEach((comp, i) => {

Isso cria automaticamente:
- mesa
- imagem 3D
- texto
- botão de quiz
- interação por hover (mostrar descrição)
- clique para abrir quiz

---

## 👁️ 5. Interação VR

O usuário interage com:

<a-cursor fuse="true" fuse-timeout="2000">

Isso significa:
- olhar para o objeto
- esperar 2 segundos
- ação é ativada automaticamente

---

## 🏆 6. Sistema de pontuação

A pontuação é salva usando:

localStorage

Isso permite:
- manter pontos mesmo recarregando a página
- experiência contínua

---

# ➕ Como adicionar novos componentes

Basta editar o array:

{
  name: "Fonte de Energia",
  desc: "Distribui energia para o computador.",
  type: "fonte",
  link: "quiz_fonte.html",
  color: "#f97316"
}

---

## ⚠️ IMPORTANTE

### 1. Adicionar imagem

<img id="fonte" src="images/fonte.png">

---

### 2. Criar quiz

quiz_fonte.html

---

## 📍 Posicionamento automático

const POSICOES = [-7.5, -4.5, -1.5, 1.5, 4.5, 7.5];

Cada posição representa uma estação no laboratório.

---

## ➕ Como adicionar mais de 6 itens

const POSICOES = [-10, -7, -4, -1, 2, 5, 8, 11];

O sistema se adapta automaticamente.

---

# 🎨 Melhorias futuras

- 🔊 Sons ao interagir
- ✨ Animações nos monitores
- 🧑‍🏫 NPCs educativos
- 🧪 mais quizzes
- 📊 ranking de jogadores
- 🌌 partículas e efeitos VR

---

# 🧠 Resumo

✔ Projeto VR educativo  
✔ Componentes interativos  
✔ Quizzes com pontuação  
✔ Interface futurista  
✔ Fácil de expandir  

---

# 📌 Autor

Projeto desenvolvido para fins educacionais utilizando tecnologias web (A-Frame + JavaScript).

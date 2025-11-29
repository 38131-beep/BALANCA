⚖️ Balança de Dois Lados – Simulador Interativo (HTML + CSS + JavaScript)

Este projeto é um simulador visual de uma balança de dois braços, construída inteiramente em HTML, CSS e JavaScript, com suporte completo a arrastar e soltar, manipulação física simples (cálculo de torque) e movimentação suave da viga conforme os pesos são adicionados.

O objetivo é permitir ao usuário experimentar torque, massa e distância do pivô de um modo intuitivo, visual e educativo, funcionando diretamente no navegador — sem bibliotecas externas.

🚀 Funcionalidades

🔧 Simulação realista de torque
A balança calcula torques com base na fórmula:
torque = peso × distância ao pivô, convertendo automaticamente as posições dos pesos.

🧲 Sistema de arrastar & soltar (drag & drop)
Arraste pesos da paleta e solte em qualquer ponto das bandejas — a distância influencia o equilíbrio.

📦 Pesos customizáveis
Crie novos pesos digitando o valor ou usando o botão “Adicionar peso”.

⬆ Arraste pesos já colocados para alterar sua distância.
🗑 Clique sobre um peso para removê-lo.

🎚 Viga com movimento dinâmico
A barra central inclina para esquerda ou direita proporcionalmente à diferença de torque, com suavidade visual.

📊 Painel de detalhes físicos
Mostra ao vivo:

Torque esquerdo

Torque direito

Massa total em cada lado

📱 Compatível com dispositivos móveis
Clique em uma bandeja para adicionar um novo peso rapidamente.

🔄 Botão de Reset
Remove todos os pesos e volta a balança ao equilíbrio inicial.

🎨 Interface moderna
Visual limpo com sombra suave, estilo madeira/metal e animações discretas.

🛠️ Tecnologias Utilizadas
HTML5

Estrutura da balança (base, pilar, viga, bandejas)

Bandejas com data-side e data-distance

Elementos dinâmicos para pesos

CSS3

Design responsivo com media queries

Estética madeira + metal

Sombras suaves, gradientes e bordas realistas

Animação na inclinação da viga

Layout flexível estilo aplicativo

JavaScript (Vanilla JS)

Sistema de arrastar e soltar via:

dragstart

dragover

drop

pointerdown

pointermove

pointerup

Cálculo completo de torque e posição relativa ao pivô

Reposicionamento suave da viga com transform: rotate()

Geração dinâmica de novos pesos

Remoção e atualização automática da física

Ajustes de física ao redimensionar a janela

📂 Estrutura do Projeto
/seu-projeto
│── index.html    # Arquivo único contendo HTML + CSS + JS


Todo o projeto é auto-contido, ideal para testar rapidamente em ambiente local, VSCode ou navegador.

⚙️ Como Funciona a Física

A balança calcula a distância horizontal entre cada peso e o centro do pivô.

Cada peso armazena internamente seu valor (g)

A distância é medida automaticamente ao soltar ou arrastar

A física usa uma unidade simples: 1 pixel = 1 mm

O torque de cada lado é calculado assim:

torque = peso_em_gramas × distância_em_mm


A diferença entre os torques gera um ângulo proporcional:

ângulo = clamp((torqueDireito − torqueEsquerdo) × sensibilidade)


A viga nunca passa do limite de ±18° para manter o visual estável.

▶️ Como Usar

Arraste um peso da paleta para a bandeja esquerda ou direita.

Solte em qualquer posição dentro da bandeja para alterar a distância.

Observe a viga inclinar automaticamente.

Clique em um peso para removê-lo.

Use “Criar” ou “Adicionar peso” para novos valores.

Use “Limpar” para resetar tudo.

💡 Dicas

Pesos mais pesados próximos do pivô produzem menos torque.

Pesos leves colocados nas extremidades podem levantar a viga inteira.

Arraste lentamente dentro da bandeja para sentir como pequenas mudanças alteram o equilíbrio.

📜 Licença

Este projeto é livre para estudo, modificação e melhorias.
Perfeito para aulas de física, demonstrações, experiências ou protótipos.

Se quiser, posso também:
🎨 Criar um novo design (neon, futurista, madeira realista, dark mode)
📘 Criar um README.md automatizado
🧪 Adicionar física mais precisa
🔧 Adicionar limites, animações, sons e haptics
📊 Criar uma versão com gráficos e histórico de torque
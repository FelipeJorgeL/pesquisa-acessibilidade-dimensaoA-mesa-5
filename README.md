## Sobre esta pesquisa
Essa pesquisa tem como objetivo responder a seguinte pergunta: como os desenvolvedores descobrem e medem falhas de acessibilidade?

## O que descobrimos (Principais Achados)
1. Existe um checklist oficial do governo para que os desenvolvedor possam garantir que um site seja inclusivo (https://www.gov.br/governodigital/pt-br/acessibilidade-e-usuario/acessibilidade-digital/material-de-apoio/emag-checklist-acessibilidade-desenvolvedores.pdf)
2. A responsividade de um site é um tipo de acessibilidade
3. Os conteúdos dos componentes precisam ser acessíveis pelo teclado para qualquer ação que seria realizada com o mouse, para pessoas com baixa mobilidade
4. O próprio chrome já tem o lighthouse, que é uma ferramenta que avalia a acessibilidade e traz os erros e pontos a melhorar de um site, já integrado ao navegador (https://developer.chrome.com/docs/lighthouse/overview?hl=pt-br)

## Ferramentas
Durante o desenvolvimento da pesquisa, testamos as seguintes ferramentas que medem e avaliam a acessibilidade de uma página: 

- Axe;
- WAVE;
- Lighthouse.

Todas essas ferramentas funcionam como extensão do navegador e seguem os critérios para avaliar o site. Para testar as ferramentas, usamos os sites da PicPay e Banco Original como exemplos. Os prints das evidências estão dentro da pasta evidencias do repositório.

### PicPay

- Notas
	1. Lighthouse: 75/100
	2. WAVE: 6.4/10
	3. Axe: Versão gratuita apresenta apenas os erros
- Principais erros:
	- Botões sem nomes acessíveis; 
	- Elementos sem atributo alt; 
	- Links com nomes não descritivos;
	- Baixo contraste;
	- Hierarquia de headings errada;
	- Conteúdo rolável sem acesso por teclado.
### Banco Original

- Notas
	1. Lighthouse: 86/100
	2. WAVE: 1.9/10
	3. Axe: Versão gratuita apresenta apenas os erros
- Principais erros:
	- Elementos sem atributo alt;
	- Dialog sem descrição;
	- Baixo constraste;
	- Hierarquia de headings errada.

### Análise
Ambos os sites apresentam problemas relevantes de acessibilidade, principalmente no que diz respeito ao uso com leitores de tela.

O Banco Original, por exemplo, possui diversas imagens sem texto alternativo (`alt`), o que impede que usuários com deficiência visual compreendam o conteúdo. Além disso, há diálogos sem descrição acessível, dificultando a navegação.

Outro problema recorrente está na nomenclatura de botões e links, que muitas vezes não é descritiva, causando confusão para usuários que dependem de tecnologias assistivas.

### Solução
De forma geral, os erros identificados são relativamente simples de corrigir. A maioria das soluções envolve o uso adequado de atributos HTML, como:

- `alt` em imagens
- `aria-label` e `aria-labelledby` em botões e componentes interativos
- Estrutura correta de headings
- Ajustes de contraste conforme diretrizes de acessibilidade


## Como isso afeta o nosso trabalho como desenvolvedores
A acessibilidade impacta diretamente a forma como desenvolvemos, pois ela não é algo opcional mas sim uma parte essencial da qualidade do produto. Como desenvolvedores, precisamos considerar desde o início se nosso sistema pode ser utilizado por todas as pessoas, incluindo aquelas com diferentes necessidades e limitações.
Primeiramente, isso muda a maneira como escrevemos código e estruturamos interfaces. É necessário utilizar corretamente elementos semânticos, organizar o conteúdo de forma clara, garantir navegação por teclado e audiodescrição e oferecer descrições adequadas para imagens e outros elementos visuais. Esses cuidados ajudam a tornar a aplicação mais compreensível e acessível.
O segundo ponto importante é que a acessibilidade faz parte do fluxo de desenvolvimento. Isso inclui realizar testes frequentes, seja com ferramentas automatizadas ou manualmente, para identificar e corrigir problemas ao longo do processo. Apesar de exigir mais atenção, essa prática evita retrabalho e melhora a qualidade do sistema.
Por último, pensar em acessibilidade melhora a experiência para todos os usuários, não apenas para pessoas com deficiência. Interfaces mais simples, organizadas e intuitivas facilitam o uso em diferentes contextos, como dispositivos móveis ou conexões lentas.

## Referências
https://www.gov.br/governodigital/pt-br/acessibilidade-e-usuario/acessibilidade-digital/material-de-apoio/emag-checklist-acessibilidade-desenvolvedores.pdf

https://web.dev/articles/a11y-tips-for-web-dev?hl=pt-br

https://developer.mozilla.org/pt-BR/docs/Web/Accessibility

https://developer.chrome.com/docs/lighthouse/overview?hl=pt-br
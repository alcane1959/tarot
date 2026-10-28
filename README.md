# Análise Profunda das 12 Cartas de Tarot

Aplicação web em arquivo único para realizar uma leitura temporal de Tarot com **12 cartas sorteadas de um baralho completo de 78 cartas**. O sistema combina dados da pessoa, período escolhido, posições da abertura, orientação normal ou invertida, elementos e padrões simbólicos para produzir uma análise extensa.

O projeto funciona inteiramente no navegador, sem servidor, banco de dados, bibliotecas externas ou instalação de dependências.

## Visão geral

A aplicação permite:

- informar o nome da pessoa;
- informar a data de nascimento;
- calcular e exibir o signo solar de forma simbólica;
- escolher o período da leitura;
- sortear 12 cartas sem repetição;
- habilitar ou desabilitar cartas invertidas;
- gerar uma síntese aprofundada;
- imprimir ou salvar o resultado em PDF;
- usar a página em computador, tablet ou celular.

## Estrutura do baralho

O baralho possui 78 cartas:

- 22 Arcanos Maiores;
- 56 Arcanos Menores.

Os Arcanos Menores são divididos em quatro naipes:

- Paus, associado ao elemento Fogo;
- Copas, associado ao elemento Água;
- Espadas, associado ao elemento Ar;
- Ouros, associado ao elemento Terra.

Cada naipe contém:

- Ás;
- Dois;
- Três;
- Quatro;
- Cinco;
- Seis;
- Sete;
- Oito;
- Nove;
- Dez;
- Valete;
- Cavaleiro;
- Rainha;
- Rei.

As 56 cartas menores são construídas pelo JavaScript combinando os dados dos quatro naipes com os 14 valores de cada naipe.

## Abertura de 12 cartas

A tiragem utiliza as seguintes posições:

1. **Situação atual**: núcleo da dinâmica e energia mais evidente no presente.
2. **Força que atravessa**: obstáculo, contraponto ou impulso que tensiona a situação.
3. **Raiz profunda**: base inconsciente, emocional ou histórica.
4. **Passado atuante**: ciclo anterior que ainda influencia o período.
5. **Consciência e aspiração**: percepção, desejo ou possibilidade consciente.
6. **Caminho próximo**: tendência imediata caso o movimento atual seja mantido.
7. **Postura pessoal**: forma como a pessoa participa e reage.
8. **Ambiente externo**: circunstâncias e influências fora do controle direto.
9. **Esperanças e receios**: desejos e medos que podem influenciar decisões.
10. **Integração e direção**: síntese do processo e direção simbólica.
11. **Aprendizado oculto**: ensinamento ainda não plenamente reconhecido.
12. **Conselho superior e desdobramento**: integração ampliada e orientação para escolhas futuras.

## Períodos disponíveis

A página oferece cinco modalidades:

- **Hoje**: da data atual até a própria data atual;
- **Esta semana**: de segunda-feira até domingo;
- **Este mês**: do primeiro ao último dia do mês atual;
- **Este ano**: de 1º de janeiro a 31 de dezembro do ano atual;
- **Data personalizada**: intervalo definido pelo usuário.

No período personalizado, a aplicação valida se as duas datas foram informadas e impede que a data final seja anterior à inicial.

## Dados utilizados

A leitura é estruturada a partir de dados separados, não de uma pergunta textual:

- nome da pessoa;
- data de nascimento;
- signo solar calculado;
- modalidade temporal;
- data inicial;
- data final;
- cartas sorteadas;
- posição de cada carta;
- orientação normal ou invertida;
- elemento de cada carta;
- tipo de arcano e, quando aplicável, naipe.

O nome serve para identificar a leitura. A data de nascimento é utilizada para calcular o signo solar exibido. O intervalo define o horizonte temporal da análise.

## Conteúdo de cada carta

Cada carta pode fornecer:

- nome;
- número ou valor;
- tipo de arcano;
- naipe, quando aplicável;
- elemento;
- palavras-chave;
- significado em posição normal;
- significado em posição invertida;
- orientação prática;
- visão geral;
- amor e relacionamentos;
- trabalho e projetos;
- vida financeira;
- desenvolvimento pessoal.

## Análise gerada

A síntese pode apresentar:

- clima geral da tiragem;
- elemento predominante;
- elementos ausentes;
- quantidade de cartas normais e invertidas;
- número simbólico calculado;
- temas recorrentes;
- origem e formação da dinâmica;
- relação entre conteúdo profundo e aspiração consciente;
- tendência do caminho próximo;
- comparação entre postura pessoal e ambiente externo;
- esperanças, medos e ambivalências;
- integração da décima carta;
- leitura dos eixos da abertura;
- análise conjunta das cinco dimensões da vida;
- mapa de profundidade;
- linha temporal interpretativa;
- coerências, tensões e conteúdos de sombra;
- plano de ação em cinco movimentos;
- aprendizado oculto da décima primeira carta;
- conselho superior da décima segunda carta;
- síntese conclusiva ampliada.

## Cartas invertidas

Quando a opção **Permitir cartas invertidas** está marcada, cada carta sorteada possui 35% de probabilidade de aparecer invertida.

A orientação invertida não é tratada automaticamente como negativa. Ela pode representar:

- interiorização;
- bloqueio;
- excesso;
- revisão;
- resistência;
- manifestação indireta do arquétipo.

Quando a opção é desmarcada, todas as cartas aparecem em posição normal.

## Funcionamento do sorteio

O sorteio segue esta lógica:

1. cria uma cópia do baralho;
2. embaralha as cartas com o algoritmo Fisher-Yates;
3. seleciona as 12 primeiras cartas do baralho embaralhado;
4. atribui uma posição da abertura a cada carta;
5. define a orientação de cada carta;
6. produz os cartões individuais;
7. gera a análise integrada.

Como a seleção é feita após o embaralhamento de uma lista de cartas únicas, uma carta não se repete na mesma tiragem.

## Signo solar

O signo é calculado apenas com o dia e o mês da data de nascimento. Os signos exibidos são:

- Capricórnio;
- Aquário;
- Peixes;
- Áries;
- Touro;
- Gêmeos;
- Câncer;
- Leão;
- Virgem;
- Libra;
- Escorpião;
- Sagitário.

Se a data não for informada, o resultado mostra o signo como não informado.

## Como executar

1. Baixe ou copie o arquivo `index.html`.
2. Abra o arquivo em um navegador moderno.
3. Informe o nome da pessoa.
4. Opcionalmente, informe a data de nascimento.
5. Escolha o período da leitura.
6. Se selecionar data personalizada, informe o início e o término.
7. Defina se deseja permitir cartas invertidas.
8. Defina se deseja utilizar a síntese aprofundada.
9. Clique em **Sortear 12 cartas**.

Não é necessário executar servidor local. O arquivo pode ser aberto diretamente no navegador.

## Como imprimir ou salvar em PDF

Depois de realizar o sorteio:

1. clique em **Imprimir / salvar em PDF**;
2. selecione uma impressora ou a opção de salvar em PDF;
3. confirme as configurações desejadas;
4. conclua a impressão.

O CSS de impressão utiliza zoom de 73%. O formulário e os botões de ação não são exibidos no documento impresso.

## Estrutura técnica

Todo o projeto está contido em um único arquivo:

```text
index.html
```

O arquivo contém:

- **HTML** para estrutura e controles;
- **CSS** para layout, responsividade e impressão;
- **JavaScript** para baralho, sorteio, datas, signo e análise.

Não há dependências externas.

## Principais estruturas JavaScript

### `positions`

Lista das 12 posições da abertura e da função interpretativa de cada posição.

### `cards`

Lista inicial dos 22 Arcanos Maiores. Após a criação dos Arcanos Menores, passa a conter as 78 cartas.

### `minorSuitData`

Define significado, elemento e aplicações de cada naipe.

### `minorRankData`

Define os 14 valores dos Arcanos Menores e suas etapas simbólicas.

### `buildMinorArcana()`

Combina os quatro naipes com os 14 valores para gerar as 56 cartas menores.

### `shuffle()`

Embaralha uma cópia do baralho.

### `zodiac()`

Calcula o signo solar com base na data de nascimento.

### `periodData()`

Calcula as datas inicial e final do período selecionado e valida intervalos personalizados.

### `draw()`

Valida os dados, embaralha o baralho, sorteia as 12 cartas, atribui posições e exibe os resultados.

### `buildReport()`

Analisa as cartas sorteadas e monta a síntese aprofundada.

### `clearAll()`

Limpa os dados e retorna a interface ao estado inicial.

## Personalização

### Alterar cores

Edite as variáveis no início do CSS:

```css
:root {
  --bg: #0d0916;
  --panel: #191126;
  --gold: #e8bd68;
  --text: #f8f2ff;
}
```

### Alterar o zoom de impressão

Localize a regra:

```css
@media print {
  html {
    zoom: 73% !important;
  }
}
```

### Alterar a probabilidade de inversão

Localize esta expressão na função de sorteio:

```javascript
Math.random() < 0.35
```

O valor `0.35` representa 35% de probabilidade.

### Alterar o número de cartas

A aplicação foi planejada para 12 posições. Para alterar essa quantidade, é necessário ajustar conjuntamente:

- a lista `positions`;
- a seleção `.slice(0, 12)`;
- a desestruturação das cartas em `buildReport()`;
- as seções da análise que dependem de posições específicas;
- os textos da interface.

## Compatibilidade

A aplicação utiliza recursos nativos de HTML, CSS e JavaScript, incluindo:

- `const` e `let`;
- template strings;
- spread operator;
- `Intl.DateTimeFormat`;
- `Object.entries()`;
- `Array.from()` e métodos modernos de arrays;
- campos de data HTML.

Recomenda-se utilizar uma versão atual de Edge, Chrome, Firefox ou Safari.

## Privacidade

Os dados são processados localmente no navegador. O código não contém chamadas de rede, armazenamento em nuvem, banco de dados, cookies ou envio automático de informações.

Se o arquivo for alterado para incluir serviços externos, essa condição deverá ser reavaliada.

## Observações importantes

A aplicação apresenta interpretações simbólicas para reflexão e entretenimento. Ela não garante acontecimentos futuros e não substitui aconselhamento:

- médico;
- psicológico;
- jurídico;
- financeiro;
- profissional.

## Limitações

- O signo calculado é somente o signo solar simplificado por dia e mês.
- A aplicação não calcula mapa astral.
- A leitura é gerada por regras e textos definidos no próprio JavaScript.
- Não existe inteligência artificial externa conectada ao arquivo.
- O resultado não é salvo automaticamente após fechar ou atualizar a página.
- O zoom CSS de impressão pode ser interpretado de forma diferente dependendo do navegador.

## Licença

Nenhuma licença foi definida no código original. Antes de distribuir publicamente, escolha e inclua uma licença adequada ao uso pretendido.

## Arquivos recomendados para publicação

Uma estrutura mínima pode ser:

```text
projeto-tarot/
├── index.html
└── README.md
```

## Resumo

Este projeto oferece uma leitura temporal de Tarot em um único arquivo HTML, com baralho completo de 78 cartas, abertura de 12 posições, cartas invertidas, seleção de período, cálculo simbólico do signo solar, análise multidimensional e impressão em PDF.

---

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

---

## Autor

**Alberto de Campos Neto**

---

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.

Your site is live at https://alcane1959.github.io/tarot/

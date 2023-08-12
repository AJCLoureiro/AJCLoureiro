https://loureiro.neocities.org/


<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="utf-8"/>
    <title>ADS/Trainee - Loureiro</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11.0.18/dist/sweetalert2.all.min.js"></script> 
</head>

<body>
    <div class="site-background"></div>
    <!-- Resto do seu conteúdo -->
<div class="background-container">
	
    <!-- Cabeçalho -->
    
	<header id="cabecalho"> 
		<div class="site-container"><!-- Nova div adicionada para englobar todo o conteúdo do site -->
			<div class="header-content">
				<!-- Atualizamos para exibir a data/hora no formato anterior -->
                <span id="hora-atual"></span><!-- Adicionar o elemento <span> com id="hora-atual" para exibir a mensagem de hora -->
					<div class="logo-container">
						<img src="imagens/Loureiro.jpg" alt="Logo" class="logo">
					</div>
            </div>
						<h1>Meu Site</h1>
						<div id="interface">
							<hgroup>
								<h1>Bom dia, boa tarde, boa noite, para o Mundo!</h1>
								<h2>Para haver Desenvolvimento, tem que haver AMOR!</h2>
								<h3>Análise e Desenvolvimento de Sistemas - ADS</h3>
							</hgroup>
							<nav id="menu"><!-- Seu menu de navegação pode ser adicionado aqui -->
								<h1>Menu Principal</h1>
									<ul type="disc">
										<li onmouseover="mudaFoto('imagens/home.png')" onmouseout="mudaFoto('imagens/home.png')"><a href="index.html">Home</a></li>
										<li onmouseover="mudaFoto('imagens/multimidia.png')" onmouseout="mudaFoto('imagens/multimidia.png')"><a href="multimidia.html">Multimídia</a></li>
										<li onmouseover="mudaFoto('imagens/contato.png')" onmouseout="mudaFoto('imagens/contato.png')"><a href="contato.html">Contato</a></li>
									</ul>
							</nav>
						</div>
		</div>
	</header>
    
    <!-- Corpo do site -->
    <div class="site-container"> <!-- Nova div adicionada para englobar todo o conteúdo do site -->
        <div class="card-container front-blue">
		            <!-- Card 1 -->
            <div class="card" onclick="virarCard(this)">
                <div class="card-inner">
                    <div class="card-front card-front-blue"> <!-- Adicione a classe "card-front-blue" para a frente do card 1 -->
                        <h2>CLIQUE AQUI - Cursos</h2>
                       	<p>IA e o Novo conceito da cultura digital</p>
						<p>Web Analytics</p>
						<p>Excel Avançado</p>
						<p>C#</p>
						<p>HTML Avançado</p>
						<p>HTML5</p>
						<p>CSS</p>
						<p>JavaScript</p>
						<p>Java avançado</p>
						<p>Implementação BD SQL</p>
						<p>SQL Server</p>
						<p>Modelagem B.D</p>
                    </div>
                    <div class="card-back card-back-#ffff33">
                        <h2>CLIQUE AQUI - Instituições</h2>
                        <p>UNISUAM</p>
						<p>CURSOS EM VÍDEOS</p>
						<p>FUNDAÇÃO BRADESCO</p>
                    </div>
                </div>
            </div>

            <!-- Card 2 -->
            <div class="card" onclick="virarCard(this)">
                <div class="card-inner">
                    <div class="card-front card-front-blue"><!-- Adicione a classe "card-front-blue" para a frente do card 1 -->
                        <h2>CLIQUE AQUI - Acadêmico</h2>
						<p>2° período ADS</p>
                        <p>Bachalelado em Geografia</p>
						<p>Licenciatura Plena em Geografia</p>
						<p>Especialização Docência E.Superior</p>
                    </div>
                    <div class="card-back card-back-#ffff33">
                        <h2>CLIQUE AQUI - Universidades</h2>
                        <p>UNISUAM</p>
						<p>UFRJ</p>
						<p>UCB</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
	
    <!-- Rodapé -->
    <footer class="footer">
        <!-- Conteúdo do rodapé -->
        <P><p align=center><font size="4" color="#ff0000"><i>Lembre-se: quanto mais se ensina, mais se aprende.</i></font size></P>
        <p>Todos os direitos reservados © 2023 Antonio Loureiro</p>
        <p><a href="https://www.linkedin.com/in/antonio-loureiro-78b359263/" target="_blank">Linkedin</a></p>
		<p class="indented-paragraph">
			Agradecimentos: 
			<a href="link-da-madalena">Madalena Loureiro</a>. 
			<a href="https://gbloureiro.neocities.org/">Gabriel Loureiro</a>. 
			<a href="link-do-rafael">Rafael Loureiro</a>. 
			<a href="https://www.scapesaude.com/">Leonília Lemos</a>. 
			<a href="https://www.cursoemvideo.com/">Curso em Vídeos - Guanabara</a>. 
			<a href="https://www.ev.org.br/">Fundação Bradesco</a>. 
			<a href="https://hs.unisuam.edu.br/">Unisuam</a>.
			<a href="https://www.youtube.com/">YouTube</a>.
		</p>
    </footer>

    <script src="script.js"></script>
</div>
</body>
</html>

--------------------------------------------------------------------------------------
// script.js
function exibirMensagem() {
    var nome = window.prompt('Qual o seu nome?');
    if (nome !== null && nome.trim() !== "") {
        window.alert('Olá, ' + nome + '! É um prazer!');
    } else {
        window.alert('ok!');
    }
}

// Chamando a função exibirMensagem() automaticamente ao carregar a página
exibirMensagem();

function atualizarHora() {
    var agora = new Date();
    var diaSemana = obterDiaSemana(agora.getDay());
    var diaMes = agora.getDate().toString().padStart(2, '0');
    var mes = obterNomeMes(agora.getMonth());
    var ano = agora.getFullYear();
    var hora = agora.getHours().toString().padStart(2, '0');
    var minutos = agora.getMinutes().toString().padStart(2, '0');
    var segundos = agora.getSeconds().toString().padStart(2, '0');

    var mensagemHora;
    if (hora < 12) {
        mensagemHora = 'Bom Dia!';
    } else if (hora < 18) {
        mensagemHora = 'Boa Tarde!';
    } else {
        mensagemHora = 'Boa Noite!';
    }

    var spanHora = document.getElementById("hora-atual");
    spanHora.textContent = `Olá! Hoje é ${diaSemana}, ${diaMes} de ${mes} de ${ano}, ${hora}:${minutos}:${segundos} h. ${mensagemHora}`;
}

function obterDiaSemana(numeroDia) {
    var diasSemana = ['Domingo', 'Segunda-feira', 'Terça-feira', 'Quarta-feira', 'Quinta-feira', 'Sexta-feira', 'Sábado'];
    return diasSemana[numeroDia];
}

function obterNomeMes(numeroMes) {
    var meses = ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho', 'Julho', 'Agosto', 'Setembro', 'Outubro', 'Novembro', 'Dezembro'];
    return meses[numeroMes];
}

// Chamando a função atualizarHora() automaticamente ao carregar a página
atualizarHora();

function virarCard(card) {
  card.classList.toggle("virado");
}

function verificar(){
	var date=new Date()
	var ano=date.getFullYear()
	var fano=document.getElementById('txtano')
	var res=document.querySelector('div#res')
	if (fano.value.length == 0 || Number(fano.value) > ano) {
		window.alert('[ERRO] Verifique os dados e tente novamente!')
	} else {
		var fsex = document.getElementByName('radsex')
		var idade = ano - Number(fano.value)
		var gênero = ''
		var img = document.createElement('img')
		res.innerHTML = `Detectamos ${gênero} com ${idade} anos.`
	}
}
----------------------------------------------------------------------------------------------------------------------------------



@charset "utf-8";
h1 {
	font-size: 16px; /* Tamanho da fonte */
    color: black; /* Cor do texto */
    /*margin-bottom: 10px;  Margem inferior */
	text-align: center;
}

h2 {
	font-size: 14px; /* Tamanho da fonte */
    color: black; /* Cor do texto */
    /*margin-bottom: 10px;  Margem inferior */
	text-align: center;
}

h3 {
	font-size: 12px; /* Tamanho da fonte */
    color: black /* Cor do texto */
	text-align: center;
	text-align: center;
}

h4 {
	font-size: 10px; /* Tamanho da fonte */
    color: black; /* Cor do texto */
    /*margin-bottom: 10px;  Margem inferior */
	text-align: center;
}

/* Estilos para o container do site, mas só altera o body? */
.site-container {
    background-color: #f0f5f5; /* Cor cinza mais escura */
    padding: 0px;
    display: flex;
    position: relative;
    flex-direction: column;
	margin-left: 200px;
	margin-right: 200px;
}

/* Estilos para o cabeçalho */
header#cabecalho {
    background-color: #f0f5f5;
	margin: 200px;
	margin-bottom: 0;
	margin-top: 0;
    max-width: 768px;
    position: relative;
	/*margin: 0;  Centraliza horizontalmente */
    display: flex;
    flex-direction: column;
    /*justify-content: flex-start; Alinha os itens à esquerda */
}

/* Estilo para a data/hora no cabeçalho */
#hora-atual {
    font-size: 14px;
    color: #585960;
    margin: 5px 0px 0px; /* Adiciona margem superior para posicionar a data/hora no topo e margem inferior para espaçamento */
}

/* Estilo para a imagem no cabeçalho */
.logo {
    width: 100px;
    height: auto;
    margin: 5px 0px; /* Adiciona margem superior e inferior para separar a logo */
}

/* Estilos para o elemento que cobre a área fora das margens */
.site-background {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgb(200, 200, 200);; /* Cor cinza escuro desejada */
    z-index: -1; /* Coloca o elemento atrás de todo o conteúdo */
}

nav#menu {
    position: relative;
    top: 45px;
    right: 0px; /* Ajuste conforme necessário */
    display: flex; /* Para alinhar os itens na mesma linha */
}

nav#menu ul {
    display: flex;
    list-style: none; /* Remove os marcadores da lista */
    padding: 0;
    margin: 0;
}

nav#menu li {
	display: inline-block;
	background-color: #dcdcdc;
	padding: 4px;
	margin: 6px;
	margin-right: 0px;
	text-transform: uppercase;
	transition: background-color 1s;
	-ms-transition: background-color 1s;
}

nav#menu li:hover {
	background-color: #708090;
}

nav#menu li:hover {
	background-color: #708090;
}

nav#menu h1 {
	display: none;
}

nav#menu a {
	color: #556B2F;
	text-decoration: underline;
}

nav#menu a:hover {
	color: red;
	text-decoration: underline;
}

/* Estilos para o container do site */
body.site-container {
    background-color: rgb(255, 255, 255); /* Cor cinza mais escura */
    padding: 0px; /* Adicione um espaçamento interno para criar uma margem entre o conteúdo e a cor de fundo */
    min-height: 100vh; /* Define a altura mínima da div para ocupar pelo menos toda a altura da janela do navegador */
    display: flex; /* Para garantir que a cor de fundo se estenda por toda a altura do site mesmo que o conteúdo seja menor */
	position: absolute; /* Adiciona posicionamento relativo para permitir posicionamento do pseudo-elemento */
    flex-direction: column; /* Para organizar o conteúdo em coluna */
	margin: 0;
	margin-left: 200px;
	margin-right: 200px;
}

/* Estilos para a div que engloba todo o conteúdo do site */
.background-container {
    /*background-color: #f0f5f5;  Cor cinza mais escura */
    padding: 0px; /* Adicione um espaçamento interno para criar uma margem entre o conteúdo e a cor de fundo */
    min-height: 100vh; /* Define a altura mínima da div para ocupar pelo menos toda a altura da janela do navegador */
    display: flex; /* Para garantir que a cor de fundo se estenda por toda a altura do site mesmo que o conteúdo seja menor */
    flex-direction: column; /* Para organizar o conteúdo em coluna */
}

/* Estilo para o container dos cards */
.card-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    max-width: 768px;
    margin: 0 auto;
	padding: 0px;
    background-color: #f0f5f5; /* Mesma cor de fundo para o container dos cards */
}

/* Estilos para os cards */
.card {
    width: 280px;
    height: 350px;
    background-color: #a9a9a9;
    padding: 2px;
    cursor: pointer;
    transition: transform 0.5s ease;
    perspective: 1000px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    position: relative;
}

.card-inner {
    width: 100%;
    height: 100%;
    transition: transform 0.5s ease;
    transform-style: preserve-3d;
}

.card-front, .card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
}

.card-back {
    transform: rotateY(180deg);
}

.card.virado .card-inner {
    transform: rotateY(180deg);
}

/* Estilos para a frente do card em azul */
.card-front-blue {
    background-color: #E6E6FA; /* Cor de fundo azul */
    color: #fff; /* Cor do texto em branco para contrastar */
}

/* Estilos para o verso do card em amarelo */
.card-back-yellow {
    background-color: #a9a9a9; /* Cor de fundo amarela */
    color: #000; /* Cor do texto em preto para contrastar */
}

.card h2 {
    margin: 0;
    font-size: 20px;
    color: black;
}

.card p {
    margin: 10px;
	font-size: 14px;
    color: blue;
}
 
/* Estilos para o rodapé */
.footer {
    max-width: 768px;
    margin-left: 200px;
	margin-right: 200px;
	margin-bottom: 0;
    padding: 0px;
	text-align: center;
	background-color: #f0f5f5; /* Mesma cor de fundo para o rodapé */
    color: black;
}
--------------------------------------------


<!DOCTYPE html>
<html lang="pt-br">
<head>
	<meta charset="utf-8"/>
	<title>Multimídia</title>
	<link rel="stylesheet" href="css/estilo.css"/>
	<link rel="stylesheet" href="css/media.css"/>
</head>

<script language="javascript" src="javaScript/funcoes.js"></script>

<body>

<div id="interface">
	<header id="cabecalho">
<hgroup>
	<h1>Para relaxar um pouco.</h1>
	<h2>A revolução, é uma construção, sempre esteve 'chegando'.</h2>
</hgroup>
	
<img id="icone"src="imagens/multimidia.png"/>
<nav id="menu">
	<h1>Menu Principal</h1>
	<ul type="disc">
		<li onmouseover="mudaFoto('imagens/home.png')" onmouseout="mudaFoto('imagens/home.png')"><a href="index.html">Home</a></li>
		<li onmouseover="mudaFoto('imagens/multimidia.png')" onmouseout="mudaFoto('imagens/multimidia.png')"><a href="multimidia.html">Multimídia</a></li>
		<li onmouseover="mudaFoto('imagens/contato.png')" onmouseout="mudaFoto('imagens/contato.png')"><a href="contato.html">Contato</a></li>
	</ul>
</nav>
	</header>

<section id="corpo-full">
	<article id="noticia-principal">
		<header id="cabeçalho-artigo">
			<hgroup>
				<h3>Multimídia</h3>
				<h1>Sons e vídeos</h1>
				<h2>por Loureiro</h2>
				<h3 class="direita">Atualizado em 09/Agosto/2023</h3>
			</hgroup>
		</header>
				<p class="indented-paragraph">Veja que este espaço está constantemente sendo aprimorado. Desfrute as mídias.</p>
								
		<div id="tv-radio">
			<audio id="musica" controls="controls">
				<source src="media/2009-lovers-carvings-bibio.mp3" type="audio/mpeg"/><!--a tag type não tem fechamento então usa a />-->
				<source src="media/2009-lovers-carvings-bibio.m4a" type="audio/x-aac"/><!--a tag type não tem fechamento então usa a />-->
				<source src="media/2009-lovers-carvings-bibio.ogg" type="audio/ogg"/><!--a tag type não tem fechamento então usa a />-->
				Lamentamos, mas não foi possível carregar o arquivo.
			</audio>
			<h5><p class="indented-paragraph">Fonte: <a href="https://youtube/vRI2u1v4uCM">https://youtube/vRI2u1v4uCM</a>, em 09/Agosto/2023, às 19:04h.</p></h5>
		</div>
		
			<div class="video-container">
				<iframe width="640" height="360" src="https://www.youtube.com/embed/SWm1uvCRfvA" title="Lenine - Paciência (Lenine In Cité)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
				
			</div>
	</article>
</section>

	<!-- Rodapé -->
	<footer id="rodape">
		<footer class="footer">
        <!-- Conteúdo do rodapé -->
        <P><p align=center><font size="4" color="#ff0000"><i>Lembre-se: quanto mais se ensina, mais se aprende.</i></font size></P>
        <p>Todos os direitos reservados © 2023 Antonio Loureiro</p>
        <p><a href="https://www.linkedin.com/in/antonio-loureiro-78b359263/" target="_blank">Linkedin</a></p>
    </footer>
</div>
</body>
</html>

----------------------------------------------------------


<!DOCTYPE html>
<html lang="pt-br">
<head>
	<meta charset="utf-8"/>
	<title>Fale Conosco.</title>
	<link rel="stylesheet" href="css/estilo.css"/>
	<link rel="stylesheet" href="css/form.css"/>
	<link rel="stylesheet" href="css/estilo15.css"/>
	
</head>

<script language="javascript" src="javascript/funcoes.js"></script><!--NÃO ESTÁ FUNCIONANDOMCOM A FUNÇÃO FORA DO HTML-->

<body>
<div id="interface">
	<header id="cabecalho">
		<hgroup>
			<h1>Comunicação.</h1>
			<h2>&nbsp;&nbsp;&nbsp;&nbsp;Ela faz muita diferença.</h2>
			<style>
				.destaque {
				color: red;
				font-size: 18px;
				font-weight: bold;
			}
			</style>
			<p>&nbsp;&nbsp;&nbsp;&nbsp;<h3 class="destaque">LAMENTO!&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;PÁGINA EM MANUTENÇÃO.</h3></p>
		</hgroup>
			
		<img id="icone" src="imagens/contato.png">
		<nav id="menu">
			<h1>Menu Principal</h1>
			<ul type="disc">
				<li onmouseover="mudaFoto('imagens/home.png')" onmouseout="mudaFoto('imagens/home.png')"><a href="index.html">Home</a></li>
				<li onmouseover="mudaFoto('imagens/multimidia.png')" onmouseout="mudaFoto('imagens/multimidia.png')"><a href="multimidia.html">Multimídia</a></li>
				<li onmouseover="mudaFoto('imagens/contato.png')" onmouseout="mudaFoto('imagens/contato.png')"><a href="contato.html">Contato</a></li>
			</ul>
		</nav>
	</header
	
	<section id="corpo">	
	<article id="noticia-principal">
		<header id="cabecalho-artigo">
			<hgroup>
				<p>&nbsp;&nbsp;&nbsp;&nbsp;<h3 class="destaque"> SITE COM OBJETIVO DE ESTUDO. NÃO TEM USO COMERCIAL.</h3></p>
				<h1>Formulário de Contato</h1>
				<h2>por Loureiro</h2>
				<h3 class="direita">Atualizado em 09/Agosto/2023</h3>
			</hgroup>
		</header>
	</article>
	</section>

<form>

<fieldset id="usuario"><legend>Identificação do Usuário</legend>
    <p>Nome:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtnome" id="txtnome" min="0"></p>
    <p>Sobre  nome:&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtsnome" id="txtsnome" min="0"></p>
    <p>E  -  mail:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtemail" id="txtemail" min="0"></p>
	<p>Telefone(DDD):<input type="number" name="txttel" id="txttel" min="0"></p>
	<p>C P F:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="number" name="txtcpf" id="txtcpf" min="0"></p>
	<p>C N P J :&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="number" name="txtcep" id="txtcep" min="0"></p>
</fieldset>

	<section>
		<div>
			<p>Ano de nascimento: 
				<input type="number" name="txtano" id="txtano" min="0">
			</p>
			<p>Sexo:
				<input type="radio" name="radsex" id="masc" checked>
				<label for="masc">Masculino</label>
				<input type="radio" name="radsex" id="fem">
				<label for="fem">Feminino</label>
			</p>
		</div>
	</section>
	

<fieldset id="endereco"><legend>Endereço do Usuário</legend>
    <p>Logradouro:<input type="text" name="txtlograd" id="txtlograd" min="0"></p>
    <p>Número :&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="number" name="txtnr" id="txtnr" min="0"></p>
    <p>Bairro :&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtbairro" id="txtbairro" min="0"></p>
    <p>Cidade :&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtcid" id="txtcid" min="0"></p>
	<p>Estado :&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtest" id="txtest" min="0"></p>
	<p>C E P :&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="txtcep" id="txtcep" min="0"></p>
</fieldset>

<fieldset id="mensagem"><legend>Mensagem do Usuário</legend>
    <p><label for="cUrg">Grau de Urgência: Mín.   </label><input type="range" name="tUrg" id="cUrg" min="0" max="10" step="5"/>  Máx.</p>
    <p><label for="cMsg">Mensagem:</label><Textarea name="tMsg" id="cMsg" cols="35" rows="5" placeholder="Digite sua mensagem."></textarea></p>
</fieldset>

<fieldset id="pedir"><legend>Quero um software também!</legend>
    <p>Gostaria de adquirir um software padronizado.</p>
    <p><label for="cMsg">Finalidade:</label><Textarea name="tMsg" id="cMsg" cols="35" rows="5" placeholder="Digite sua mensagem."></textarea></p>
    <p>Pessoa:
				<input type="radio" name="radsex" id="masc" checked>
				<label for="masc">Física</label>
				<input type="radio" name="radsex" id="fem">
				<label for="fem">Jurídica</label>
	</p>
</fieldset>
</form>
	<div id="botton">
		<p><input type="button" value="ENVIAR" onclick="enviar()"></p>
	</div>
	<!-- Rodapé -->
	<footer id="rodape">
	<footer class="footer">
        <P><p align=center><font size="4" color="#ff0000"><i>Lembre-se: quanto mais se ensina, mais se aprende.</i></font size></P>
        <p>Todos os direitos reservados © 2023 Antonio Loureiro</p>
        <p><a href="https://www.linkedin.com/in/antonio-loureiro-78b359263/" target="_blank">Linkedin</a></p>
    </footer>
	<script src="script15.js"></script>
</div>
</body>
</html>

-------------------------------------------

@ charset="utf-8";
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web&display=swap');
@font-face {
		font-family: 'FonteLogo';
		src: url("C:\Users\Thamyres\Desktop\Site\font/bubblegum-sans-regular.otf");
}

body {
	
	font-family: Arial, sans-serif;
	background-color: #dddddd;/*hsl(165,81%,93%,0.5);*/
	color: rgba(0,0,0,1);
}

div#interface {
	width: 900px;
	background-color: #ffffff;
	margin: 0px auto 0px auto;
	box-shadow: 0px 0px 10px black;
	padding: 10px;
}

		h1 {
			font-family: Arial;
			font-size: 30pt;
			color: blue;
			text-shadow: 2px 5px 2px black;
		}
			
		p {
			text-align:justify;
			text-indent:50px;
		}
		
		a {
			color: #616259;
		}
		
		a:hover {
			text-decoration: underline;
		}
		
header#cabecalho img#icone {
	position: absolute;
	left: 850px;
	top: 80px;
}

header#cabecalho {
	border-bottom: 1px #585960 solid;
	height: 150px;
	background: url("../imagens/contato.jpg") no-repeat 0px 100px;
}

header#cabecalho h1 {
	font-family: 'FonteLogo', sans-serif;
	font-size: 30px;
	color: #596061;
	text-shadow: 0px 1px 2px rgba(1,1,1,.5);
	padding: 0px;
	margin-bottom: 0px; 
}

header#cabecalho h2 {
	font-family: 'Titillium Web', sans-serif;
	color: #888888;
	font-size: 15px;
	margin-top: 0px;
}
			
/*Formatação de imagens com legenda.*/

figure.foto-legenda {
	position: relative;
	border: 8px solid white;
	box-shadow: 1px 1px 4px black;
}

figure.foto-legenda img {
		width: 100%;
		height: 100%;
}

figure.foto-legenda figcaption {
		opacity: 1;
		position: absolute;
		top: 0px;
		background-color: rgba(0,0,0,.4);
		color: white;
		width: 100%;
		height: 100%;
		padding: 10px;
		box-sizing: border-box;
		transition: opacity 1s;
}
		
figure.foto-legenda: hover figcaption {
	opacity: 1;
}

/*Formatação do menu*/
nav#menu {
    position: absolute;
    top: 45px;
    right: 225px; /* Ajuste conforme necessário */
    display: flex; /* Para alinhar os itens na mesma linha */
}

nav#menu ul {
    display: flex;
    list-style: none; /* Remove os marcadores da lista */
    padding: 0;
    margin: 0;
}

nav#menu li {
	display: inline-block;
	background-color: #dcdcdc;
	padding: 4px;
	margin: 6px;
	margin-right: 0px;
	text-transform: uppercase;
	transition: background-color 1s;
	-ms-transition: background-color 1s;
}

nav#menu li:hover {
	background-color: #708090;
}

nav#menu h1 {
	display: none;
}

nav#menu a {
	color: #556B2F;
	text-decoration: underline;
}

nav#menu a:hover {
	color: red;
	text-decoration: underline;
}

section#corpo { /* corpo divide lateralmente*/
	display: block;
	width: 500px;
	float: left;
	border-right: 1px solid green;
	padding-right: 20px;
}

article#noticia-principal h2 {
	font-size: 16px;
	color: #606059;
	background-color: #dddddd;
	padding: 5px 0px 5px 10px;
	margin: 10px 0px 10px 0px;
}

header#cabecalho-artigo h1 {
	font-family: 'FonteLogo', sans-serif;
	font-size: 20pt;
	color: #585960;
	text-shadow: 0px 1px 2px rgba(1,1,1,.5);
}

.direita {
	text-align: right;
}

header#cabecalho-artigo h2 {
	font-size: 16pt;
	color: #585960;
	background-color: #dddddd;
}

header#cabecalho-artigo h3 {
	font-size: 16pt;
	color: #585960;
	
}

table#tabelaspec {
	border: 1px solid #585960;
	border-spacing: 0px; /*para acabar com distância entre margens da célula*/
	margin-left: auto;
	margin-right: auto;
}

table#tabelaspec td {
	border: 1px dashed #585960;
	padding: 5px;
	/*text-align: center;/right/left
	vertical-align: bottom;/top/
	vertical-align: middle;(para centralizar)*/
}

table#tabelaspec td.ce {
	color: #ffffff;
	background-color: #585960;
	vertical-align: top;
	font-weight: bold;
}

table#tabelaspec td.CD {
	background-color: #cecece;
}

table#tabelaspec caption {
	color: #888888;
	font-size: 12pt;
	font-weight: bolder;
}

table#tabelaspec span {
	display: block;
	float: right;
	color: #000000;
	font-size: 8px;
	margin-top: 10px;
}

aside#lateral {
	display: block;
	width: 350px;
	float: right;
	background-color: #dddddd;
	padding: 10px;
	margin-top: 10px;
	box-shadow: 2px 2px 2px rgb(0,0,0,0,.5);
	margin-top: 0px;
}

aside#lateral h1 {
	font-family: 'FonteLogo' sans-serif;
	font-size: 20pt;
	color: #585960;
}

aside#lateral h2 {
	background-color: #585960;
	font-size: 20pt;
	color: #ffffff;
	padding: 5px;
}

footer#rodape {
	clear: both; /*limpa configuração dos 2 lados*/
	border-top: 1px solid #585960;
}

footer#rodape p {
	text-align: center;
}

-----------------------------------------------
@charset "utf-8";

audio#musica {
	display: block;
	position: relative;
	left: 275px;
	top: 50px;
	width: 300px;
}

video#filme {
	display: block;
	position: relative;
	left: 220px;
	top: 10px;
	width: 440px;
}
.video-container {
    display: flex;
    justify-content: center; /* Centraliza horizontalmente */
	padding-bottom: 20px;
	padding-top: 50px;
}

/* Estilo para o parágrafo com margem à esquerda */
.indented-paragraph {
    margin-left: 160px; /* Ajuste este valor conforme necessário */
	padding-top: 50px;
}

--------------------------------------------------

@charset "UTF-8";

form {
	width: 500px;
	margin: auto;
}

input, textarea {
	font-family: sans-serif;
	font-weight: normal;
	font-size: 13pt;
	background-color: rgba(255,255,255,.5);
}

input:hover, textarea:hover {
	background-color: #dddddd;
}

legend {
	color: #888888;
	font-weight: bold;
	font-size: 13pt;
	font-family: sans-serif;
}

fieldset {
	border-color: #cecece;
	margin: 20px;
	box-shadow: 5px 10px 10px black;
}

fieldset#sexo {
	width: 350px;
}

div#botton {
	margin-left: 360px;
}

-------------------------------------------------------------


* PICT GLOTALES 2020

- renovacion: https://r020.com.ar/lab/caicyt/nivacle/proyectos-pict
	PICT-2020-SERIEA-03903, (Aceptado, febrero 2022).
	Temas Abiertos (I), Grupo de Reciente Formación, 3 años. “Representaciones, procesos y trayectorias de las glotales y dorsales en el nivaĉle y su comparación con otras lenguas mataguayas.” Investigadora Responsable: Dra. Analía Gutiérrez. Fondo para la Investigación Científica y Tecnológica, Agencia Nacional de Promoción Científica y Tecnológica, MINCYT

## julio

- ya está lista planilla de palabras en común para recortar audios para GG
https://docs.google.com/spreadsheets/d/1GtliM_yutOBnWaferOmQjVNLt_xOxz56rst6ZR9MkXc/edit#gid=1308046217
- ya están los csv de las transcripciones con metadata más completa
DILA/PICT-20161038/lexico
- también hice un csv global de glotales detectadas en transcripciones y en fuentes bibiográficas
- todo generado con `2022-julio.ipynb`

## septiembre

- copié Excel de transcripciones en https://drive.google.com/drive/u/2/folders/1Cn6StmzsKSysBb8aMlp0w7fYgMe7bN4S
- generado con PICT-20161038/2022-julio.ipynb
- DataTable para resultados.md y corpus-interno.md 

- reunión con AG en Caicyt
	- Sitio PICT
		- palabras comunes a las 4 lenguas: retomar transcripción del archivo spreadsheet de palabras 
		- geolocalizar audios
		- glotales por fuente
			AG hace seleccion de palabras y corrige transcripcion en columna nueva "Palabra AFI"
			AG hace un archivo con datos de audio en Nivaclé
			- agregar nuevas columnas: Hablante y Coordenadas
		- Comparación de fuentes textuales
			- NH cambiar código por Cita
			- NH agregr referencias bibliográficas abajo del cuadro
		- cuadro de comparación de fuentes de audio: agregar audios recortados por GG y AG con ícono de bocinita

## octubre

let data =[
{
    audio:new Audio("https://github.com/Alaixs/ChantSupporter/raw/beta/Audio2.mp3"), 
    id:'#ppb1'
},
{
    audio:new Audio("https://commons.wikimedia.org/wiki/File:Musical_Sound_1_(Gravity_Sound).wav"), 
    id:'#ppb2'
}
];

data.forEach((d)=>{
    // Get the element
    $(d.id).on("click",function(){
    // Play and change the DOM
       d.audio.play();
  });
  
});



{% for row in site.data.mataguayas-comparadas-audio %}
  <tr>
    <td>{{ row.espanol }}</td>
    <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="{{row.fuente_wichi}}">{{ row.wichi }}</button></td>
    <td><audio id="{{row.audio_wichi}}"><source src="{{ site.baseurl }}/assets/audio/{{row.audio_wichi}}.wav" type="audio/wav"></audio><button onclick="playAudio()" type="button">{{row.has_audio_wichi}}</button></td>
    <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="{{row.fuente_chorote}}">{{ row.chorote }}</button></td>
    <td><audio id="{{row.audio_chorote}}"><source src="{{ site.baseurl }}/assets/audio/{{row.audio_chorote}}.wav" type="audio/wav"></audio><button onclick="playAudio()" type="button">{{row.has_audio_chorote}}</button></td>
    <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="{{row.fuente_nivacle}}">{{ row.nivacle }}</button></td>
    <td><audio id="{{row.audio_nivacle}}"><source src="{{ site.baseurl }}/assets/audio/{{row.audio_nivacle}}.wav" type="audio/wav"></audio><button onclick="playAudio()" type="button">{{row.has_audio_nivacle}}</button></td>
    <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="{{row.fuente_maka}}">{{ row.maka }}</button></td>
    <td><audio id="{{row.audio_maka}}"><source src="{{ site.baseurl }}/assets/audio/{{row.audio_maka}}.wav" type="audio/wav"></audio><button onclick="playAudio()" type="button">{{row.has_audio_maka}}</button></td>
  </tr>

<script>
var x = document.getElementById("{{row.audio_wichi}}"); 
function playAudio() { 
  x.play(); 
}
</script>
{% endfor %}






<button id="{{row.audio_wichi}}" data-src="{{ site.baseurl }}/assets/audio/{{row.audio_wichi}}.wav" type="audio/wav" onclick="playAudio()" type="button">{{row.has_audio_wichi}}</button>



<table class="table py-2 mb-4">
  <thead>
    <tr>
      <th>Español</th>
      <th>Wichi</th>
      <th>Chorote</th>
      <th>Nivaĉle</th>
      <th>Maka</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>flor</td>
      <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="Bucca, 1969">ɬawoʔ</button><button onclick="playAudio()" type="button">🔉</button></td>
      <td>ɬokʲe</td>
      <td>ɬawa</td>
      <td>ɬop'om</td>
    </tr>
    <tr><td>fruta</td>
      <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="Bucca, 1969">ɬaj</button><button onclick="playAudio()" type="button">🔉</button></td>
      <td>chorote</td><td>nivacle</td><td></td></tr>
    <tr><td>su hija</td>
      <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="Bucca, 1969">ɬɑse</button><button onclick="playAudio()" type="button">🔉</button></td>
      <td>chorote</td><td>nivacle</td><td></td></tr>
    <tr><td>su hija</td>
      <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="Bucca, 1969">ɬɑse</button><button onclick="playAudio()" type="button">🔉</button></td>
      <td>chorote</td><td>nivacle</td><td></td></tr>
    <tr><td>mi hija</td>
      <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="Bucca, 1969"></button><button onclick="playAudio()" type="button">🔉</button></td>
      <td>chorote</td><td>nivacle</td><td></td></tr>
    <tr><td>piojo</td>
      <td><button class="balloon" data-balloon-pos="up" data-balloon-length="small" data-balloon="Bucca, 1969">ɬaʔ</button><button onclick="playAudio()" type="button">🔉</button></td>
      <td>chorote</td><td>nivacle</td><td></td></tr>
  </tbody>
</table>
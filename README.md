Följ instruktionerna steg för steg och ha en porfolio på nolltid!

1. LADDA NER JQUERY 
Ladda ner jQuery HÄR, inkludera filen i <head> i din html-fil.

2. LADDA NER SITESHOW FRÅN GITHUB 
Ladda ner SiteShow från GitHub HÄR, inkludera filen siteshow-github.js samt siteshow-github.css i <head>. 
Din <head> ska nu se ut ungefär såhär; 

<head>
	<link rel="stylesheet" type="text/css" href="siteshow-github.css">	
	<script src="jquery.js"></script>
	<script src="siteshow-github.js"></script>
</head>

3. HTML 
För att SiteShow ska fungera krävs en del HTML-element. Se nedan. 

<body>
 <div id="bkg"></div>
 <div id="nav-menu"> 
  <!-- Byt ut "logotyp.png" mot sökvägen till din logotyp. --> 
  <div id="logo"><img src="logotyp.png"></div> 
 </div>
</body>

4. LÄGG TILL SLIDES 
Koden nedan definierar EN slide. Ju fler slides du vill ha, ju fler sådana kodklumpar lägger du in i <body>. För varje slide ändrar du id-numret, slide 1 har id slide-1, slide 2 id slide-2 osv. 

<!-- Varje slide ska ha ett unikt id, syntax: slide-1, slide-2 osv -->
<!-- Byt ut "bakgrundsbildkälla.jpg" mot sökvägen till din bakgrundsbild. Lämna tom om du inte vill ha någon. -->
<div id="slide-1" class="slide" data-src="bakgrundsbildkälla.jpg">
 <div class='heading'>
  <div class="title">
   <!-- Byt ut "rubrik" mot din rubrik -->
   <h1>Rubrik</h1>
   <div class="clearfix"></div>
   <!-- Byt ut "underrubrik" mot din underrubrik -->
   <p>Underrubrik</p>
  </div>
  <img class="open" src="img/open.png">
 </div>
 <div class="content">
  <!-- Byt ut "introtext" mot din introtext -->
  <p id="intro">Introtext</p>
  <!-- Byt ut "text" mot din text -->
  <p>Text</p>
  <!-- Ta bort hela table-elementet om du inte vill ha något bildgalleri i sliden -->
  <table>
   <tr>
    <!-- Byt ut "bildkälla1.jpg" mot sökvägen till din bild -->
    <!-- Fler bilder = fler kodsnuttar som nedan. Kräver unika id, syntax image-slideID-bildID, ex: image-1-1, image-1-2 osv -->
    <td><div id='image-1-1' class='image' data-src='bildkälla1.jpg'></div></td>
   <tr>
  </table>
 </div>
</div>

5. LÄGG TILL BAKGRUNDSMUSIK 
Om du vill ha bakgrundsmusik lägger du in koden nedan i <body>. 

<div id="music-control"> 
 <div class="left"><img src="img/volume-on.png"></div> 
 <!-- Byt ut "låttitel" mot titeln på din låt --> 
 <div class="right">Låttitel</div> 
</div> 

<audio autoplay loop id="music"> 
 <!-- Byt ut "låtkälla" mot sökvägen till din låt -->
 <source src="låtkälla.mp3"> 
</audio>

6. ÄNDRA FÄRGERNA 
Vill du skräddarsy din layout? Lägg in koden nedan i <head>, mellan jquery.js och siteshow-github.js. 
"Färg" ska ersättas med valfri färg. Grön kan exempelvis skrivas som "green", "#00ff00" eller "rgba(0,255,0,0.5);". Sistnämnda används för att ge färgen opacitet, där 0.5 bestämmer hur transparent denna ska vara på en skala 0-1. 

<script> 
 $(document).ready(function() { $('#nav-menu').SiteShow({ 
 <!-- Byt ut "färg" mot valfri färg --> 
 'menu_background_color' : 'färg', 
 'menu_font_color' : 'färg', 
 'menu_current_color' : 'färg', 
 'logo_background_color' : 'färg', 
 'content_background_color' : 'färg', 
 'content_font_color' : 'färg', 
 'slide_background_color' : 'färg' 

 }); }); 
</script>

7. KLART! 
På GitHub kan du hitta ett exempel på hur din färdiga kod skulle kunna se ut. Bra att titta på om något känns otydligt! Lycka till :-)
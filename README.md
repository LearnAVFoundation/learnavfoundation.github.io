


<!DOCTYPE html>
<html lang="en"> 
<head>
    <meta charset="utf-8"/>
    <title>LearnOpenGL - Introduction</title>	<!--<title>Learn OpenGL, extensive tutorial resource for learning Modern OpenGL</title>-->
    <link rel="shortcut icon" type="image/ico" href="/favicon.ico"  />
    <meta name="description" content="Learn OpenGL . com provides good and clear modern 3.3+ OpenGL tutorials with clear examples. A great resource to learn modern OpenGL aimed at beginners.">
	<meta name="fragment" content="!">
    <script>
      (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
      (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
      m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
      })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

      ga('create', 'UA-51879160-1', 'learnopengl.com');
      ga('send', 'pageview');

    </script>
    <!--<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>-->
    <script>
         (adsbygoogle = window.adsbygoogle || []).push({
              google_ad_client: "ca-pub-7855791439695850",
              enable_page_level_ads: true
         });
    </script>
	<script async='async' src='https://www.googletagservices.com/tag/js/gpt.js'></script>
	<script>
	  var googletag = googletag || {};
	  googletag.cmd = googletag.cmd || [];
	</script>
	<script>
	  googletag.cmd.push(function() {
		googletag.defineSlot('/8491498/learnopengl_video', [300, 225], 'div-gpt-ad-1540574378241-0').addService(googletag.pubads());
		googletag.pubads().enableSingleRequest();
		googletag.pubads().collapseEmptyDivs();
		googletag.enableServices();
	  });
	</script>
    <script type="text/javascript" src="https://d31vxm9ubutrmw.cloudfront.net/static/js/1681.js"></script>
	<script src="/js/jquery-1.11.0.min.js"></script>
	<script src="/js/hoverintent.js"></script>
	<link rel="stylesheet" type="text/css" href="/layout.css">
    <link rel="stylesheet" type="text/css" href="/js/styles/obsidian.css">
    <script src="/js/highlight.pack.js"></script>    
    <script src="/js/functions.js"></script>
    <script type="text/javascript" src="/js/mathjax/MathJax.js?config=TeX-AMS_HTML"></script>
    <script>
    // Has to be loaded last due to content bug 
    MathJax.Hub.Config({
        TeX: { equationNumbers: { autoNumber: "AMS" } }
    });
    </script>
    <script>hljs.initHighlightingOnLoad();</script>
    <script>  
        $(document).ready(function() {
            // check if user visited from the old # based urls, re-direct to ?p= form
            if(window.location.hash)
            {
                var name = window.location.hash.substring(2);
                // name = name.replace(/-/g," ");
                var index = name.indexOf('#'); // Remove any hash fragments from the url (Disquss adds hash fragments for comments, but results in 404 pages)
                if(index >= 0)
                    name = name.substring(0, index);
                
                window.location.href = "https://learnopengl.com/" + name;
            } else {
                    // Check if data has been succesfully loaded, if so: change title bar as ajax hash fragment
                    var title = $('#content-url').text();
                  
                    // Refresh syntax highlighting
                    // $('pre').each(function(i, e) {hljs.highlightBlock(e)});
                  
                    // Reset DISQUS
                    // if(title == '/dev/')
                        // title = '';
                    // alert('hoi');
                    
                    // Adjust ads for correct bottom positioning based on content size
                    window.setTimeout(function() {  
                        AdPositioning();
                     }, 3000);
                  
                  
                    // set API resets after time-out (once content is properly loaded)
                    window.setTimeout(function() {  
                        MathJax.Hub.Queue(["Typeset",MathJax.Hub]);       
                        MathJax.Hub.Queue(["resetEquationNumbers", MathJax.InputJax.TeX]);
                        
                        var page_url = title == "" ? "http://www.learnopengl.com/" : "http://www.learnopengl.com/" + title;
                        if(typeof DISQUS !== 'undefined') {                                              
                            DISQUS.reset({
                              reload: true,
                              config: function () {  
                                this.page.identifier = title;  
                                this.page.url = page_url;
                              }
                            });
                            $('#disqus_thread').show();
                        }
                           // Refresh callbacks on <function> tags
                        SetFunctionTagCallbacks();        
                    }, 1000);
                                        
                    // Zet ook de juiste button op 'selected'
                    $('#nav li span, #nav li a').removeClass('selected');                
                    if(title != '')
                    {                    
                        $('#nav li[id=\'' + title + '\']').children('span, a').addClass('selected');
                    }
                    // En open menu waar nodig
                    var parents = $('#nav span.selected, #nav a.selected').parents('li').children('span.closed, a.closed');
                    var index = 0;
                    for(index = parents.length - 1; index >= 0; index--)
                    {             
                        
                        var id = $(parents[index]).attr("id").replace( /^\D+/g, '');
                        MenuClick(id, false);
                    }                          
                
            }
        });
		// var initialized = false;
        // window.onpopstate = function() {
            // if(initialized)
                // LoadPage();
			// else
				// initialized = true;
        // };
        
        // Set up DISQUS
        // $(document).ready(function() {
            var disqus_shortname = 'learnopengl';
            (function() {
                var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
                dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
                (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
            })();           
        // });
    </script>
</head>
<body>
<a href="https://learnopengl.com">
<div id="header">
</div>
</a>

<div id="supercontainer">
    <!-- 728x90/320x50 -->
    <div id="header_ad">
        <div id="waldo-tag-6194"></div>
    </div>
    <div id="rightad_container">
        <div id="rightad">
            <!-- /8491498/learnopengl_video -->
            <!--<div id='div-gpt-ad-1540574378241-0' style='height:225px; width:300px;'>
			<script>
			googletag.cmd.push(function() { googletag.display('div-gpt-ad-1540574378241-0'); });
			</script>
			</div>            
            <br/>-->
           
            <div id="waldo-tag-1715"></div>
        </div>

        <div id="admessage">
            If you're running AdBlock, please consider whitelisting this site if you'd like to support LearnOpenGL; and no worries, I won't be mad if you don't :)
            <!--<br/><br/>
            Also, check out this little local multiplayer-only game I've made: <a href="https://store.steampowered.com/app/983590/Tank_Blazers/" target="_blank">Tank Blazers</a>.
            <br/>
            <a href="https://store.steampowered.com/app/983590/Tank_Blazers" target="_blank"><img src="/img/tank_blazers.jpg"  style="width:278px; margin-top: 9px; margin-left: -3px;"/></a>-->
        </div>
        
        <div id="rightonethirdad">
            <div id="waldo-tag-2246"></div>
        </div>
        
        <div id="rightbottomad">            
			<div id="waldo-tag-2247"></div>								
        </div>
    </div>
    <div id="container">
        <div id="loading"></div>
<script> 
$(document).ready(function() {
$('#menu-item4').mousedown(function() { MenuClick(4, true) });
$('#menu-item48').mousedown(function() { MenuClick(48, true) });
$('#menu-item56').mousedown(function() { MenuClick(56, true) });
$('#menu-item63').mousedown(function() { MenuClick(63, true) });
$('#menu-item100').mousedown(function() { MenuClick(100, true) });
$('#menu-item102').mousedown(function() { MenuClick(102, true) });
$('#menu-item113').mousedown(function() { MenuClick(113, true) });
$('#menu-item116').mousedown(function() { MenuClick(116, true) });
$('#menu-item78').mousedown(function() { MenuClick(78, true) });
$('#menu-item81').mousedown(function() { MenuClick(81, true) });
$('#menu-item85').mousedown(function() { MenuClick(85, true) });
}); 
</script>   
    <div id="nav">
         <div id="social">
            <a href="https://github.com/JoeyDeVries/LearnOpenGL" target="_blank">
                    <img src="/img/github.png" class="social_ico">
            </a>
             <!-- <a href="https://www.facebook.com/Learnopengl-2199631333595544/" target="_blank">
                <img src="/img/facebook.png" class="social_ico">
            </a>-->
            <a href="https://twitter.com/JoeyDeVriez" target="_blank">
                <img src="/img/twitter.png" class="social_ico">
            </a>
          
        </div>
    <img src='img/nav-button_bottom-arrow.png' style='display: none'><ol><li id='Introduction'><a id="menu-item1" href="https://learnopengl.com/Introduction">Introduction </a></li><li id='Getting-started'><span id="menu-item4" class="closed">Getting started </span><ol id="menu-items-of4" style="display:none;"><li id='Getting-started/OpenGL'><a id="menu-item49" href="https://learnopengl.com/Getting-started/OpenGL">OpenGL </a></li><li id='Getting-started/Creating-a-window'><a id="menu-item5" href="https://learnopengl.com/Getting-started/Creating-a-window">Creating a window </a></li><li id='Getting-started/Hello-Window'><a id="menu-item6" href="https://learnopengl.com/Getting-started/Hello-Window">Hello Window </a></li><li id='Getting-started/Hello-Triangle'><a id="menu-item38" href="https://learnopengl.com/Getting-started/Hello-Triangle">Hello Triangle </a></li><li id='Getting-started/Shaders'><a id="menu-item39" href="https://learnopengl.com/Getting-started/Shaders">Shaders </a></li><li id='Getting-started/Textures'><a id="menu-item40" href="https://learnopengl.com/Getting-started/Textures">Textures </a></li><li id='Getting-started/Transformations'><a id="menu-item43" href="https://learnopengl.com/Getting-started/Transformations">Transformations </a></li><li id='Getting-started/Coordinate-Systems'><a id="menu-item44" href="https://learnopengl.com/Getting-started/Coordinate-Systems">Coordinate Systems </a></li><li id='Getting-started/Camera'><a id="menu-item47" href="https://learnopengl.com/Getting-started/Camera">Camera </a></li><li id='Getting-started/Review'><a id="menu-item50" href="https://learnopengl.com/Getting-started/Review">Review </a></li></ol></li><li id='Lighting'><span id="menu-item48" class="closed">Lighting </span><ol id="menu-items-of48" style="display:none;"><li id='Lighting/Colors'><a id="menu-item51" href="https://learnopengl.com/Lighting/Colors">Colors </a></li><li id='Lighting/Basic-Lighting'><a id="menu-item52" href="https://learnopengl.com/Lighting/Basic-Lighting">Basic Lighting </a></li><li id='Lighting/Materials'><a id="menu-item53" href="https://learnopengl.com/Lighting/Materials">Materials </a></li><li id='Lighting/Lighting-maps'><a id="menu-item54" href="https://learnopengl.com/Lighting/Lighting-maps">Lighting maps </a></li><li id='Lighting/Light-casters'><a id="menu-item55" href="https://learnopengl.com/Lighting/Light-casters">Light casters </a></li><li id='Lighting/Multiple-lights'><a id="menu-item58" href="https://learnopengl.com/Lighting/Multiple-lights">Multiple lights </a></li><li id='Lighting/Review'><a id="menu-item57" href="https://learnopengl.com/Lighting/Review">Review </a></li></ol></li><li id='Model-Loading'><span id="menu-item56" class="closed">Model Loading </span><ol id="menu-items-of56" style="display:none;"><li id='Model-Loading/Assimp'><a id="menu-item59" href="https://learnopengl.com/Model-Loading/Assimp">Assimp </a></li><li id='Model-Loading/Mesh'><a id="menu-item60" href="https://learnopengl.com/Model-Loading/Mesh">Mesh </a></li><li id='Model-Loading/Model'><a id="menu-item61" href="https://learnopengl.com/Model-Loading/Model">Model </a></li></ol></li><li id='Advanced-OpenGL'><span id="menu-item63" class="closed">Advanced OpenGL </span><ol id="menu-items-of63" style="display:none;"><li id='Advanced-OpenGL/Depth-testing'><a id="menu-item72" href="https://learnopengl.com/Advanced-OpenGL/Depth-testing">Depth testing </a></li><li id='Advanced-OpenGL/Stencil-testing'><a id="menu-item73" href="https://learnopengl.com/Advanced-OpenGL/Stencil-testing">Stencil testing </a></li><li id='Advanced-OpenGL/Blending'><a id="menu-item74" href="https://learnopengl.com/Advanced-OpenGL/Blending">Blending </a></li><li id='Advanced-OpenGL/Face-culling'><a id="menu-item77" href="https://learnopengl.com/Advanced-OpenGL/Face-culling">Face culling </a></li><li id='Advanced-OpenGL/Framebuffers'><a id="menu-item65" href="https://learnopengl.com/Advanced-OpenGL/Framebuffers">Framebuffers </a></li><li id='Advanced-OpenGL/Cubemaps'><a id="menu-item66" href="https://learnopengl.com/Advanced-OpenGL/Cubemaps">Cubemaps </a></li><li id='Advanced-OpenGL/Advanced-Data'><a id="menu-item69" href="https://learnopengl.com/Advanced-OpenGL/Advanced-Data">Advanced Data </a></li><li id='Advanced-OpenGL/Advanced-GLSL'><a id="menu-item67" href="https://learnopengl.com/Advanced-OpenGL/Advanced-GLSL">Advanced GLSL </a></li><li id='Advanced-OpenGL/Geometry-Shader'><a id="menu-item68" href="https://learnopengl.com/Advanced-OpenGL/Geometry-Shader">Geometry Shader </a></li><li id='Advanced-OpenGL/Instancing'><a id="menu-item70" href="https://learnopengl.com/Advanced-OpenGL/Instancing">Instancing </a></li><li id='Advanced-OpenGL/Anti-Aliasing'><a id="menu-item75" href="https://learnopengl.com/Advanced-OpenGL/Anti-Aliasing">Anti Aliasing </a></li></ol></li><li id='Advanced-Lighting'><span id="menu-item100" class="closed">Advanced Lighting </span><ol id="menu-items-of100" style="display:none;"><li id='Advanced-Lighting/Advanced-Lighting'><a id="menu-item101" href="https://learnopengl.com/Advanced-Lighting/Advanced-Lighting">Advanced Lighting </a></li><li id='Advanced-Lighting/Gamma-Correction'><a id="menu-item110" href="https://learnopengl.com/Advanced-Lighting/Gamma-Correction">Gamma Correction </a></li><li id='Advanced-Lighting/Shadows'><span id="menu-item102" class="closed">Shadows </span><ol id="menu-items-of102" style="display:none;"><li id='Advanced-Lighting/Shadows/Shadow-Mapping'><a id="menu-item103" href="https://learnopengl.com/Advanced-Lighting/Shadows/Shadow-Mapping">Shadow Mapping </a></li><li id='Advanced-Lighting/Shadows/Point-Shadows'><a id="menu-item104" href="https://learnopengl.com/Advanced-Lighting/Shadows/Point-Shadows">Point Shadows </a></li></ol></li><li id='Advanced-Lighting/Normal-Mapping'><a id="menu-item106" href="https://learnopengl.com/Advanced-Lighting/Normal-Mapping">Normal Mapping </a></li><li id='Advanced-Lighting/Parallax-Mapping'><a id="menu-item107" href="https://learnopengl.com/Advanced-Lighting/Parallax-Mapping">Parallax Mapping </a></li><li id='Advanced-Lighting/HDR'><a id="menu-item111" href="https://learnopengl.com/Advanced-Lighting/HDR">HDR </a></li><li id='Advanced-Lighting/Bloom'><a id="menu-item112" href="https://learnopengl.com/Advanced-Lighting/Bloom">Bloom </a></li><li id='Advanced-Lighting/Deferred-Shading'><a id="menu-item108" href="https://learnopengl.com/Advanced-Lighting/Deferred-Shading">Deferred Shading </a></li><li id='Advanced-Lighting/SSAO'><a id="menu-item109" href="https://learnopengl.com/Advanced-Lighting/SSAO">SSAO </a></li></ol></li><li id='PBR'><span id="menu-item113" class="closed">PBR </span><ol id="menu-items-of113" style="display:none;"><li id='PBR/Theory'><a id="menu-item114" href="https://learnopengl.com/PBR/Theory">Theory </a></li><li id='PBR/Lighting'><a id="menu-item115" href="https://learnopengl.com/PBR/Lighting">Lighting </a></li><li id='PBR/IBL'><span id="menu-item116" class="closed">IBL </span><ol id="menu-items-of116" style="display:none;"><li id='PBR/IBL/Diffuse-irradiance'><a id="menu-item117" href="https://learnopengl.com/PBR/IBL/Diffuse-irradiance">Diffuse irradiance </a></li><li id='PBR/IBL/Specular-IBL'><a id="menu-item118" href="https://learnopengl.com/PBR/IBL/Specular-IBL">Specular IBL </a></li></ol></li></ol></li><li id='In-Practice'><span id="menu-item78" class="closed">In Practice </span><ol id="menu-items-of78" style="display:none;"><li id='In-Practice/Debugging'><a id="menu-item79" href="https://learnopengl.com/In-Practice/Debugging">Debugging </a></li><li id='In-Practice/Text-Rendering'><a id="menu-item80" href="https://learnopengl.com/In-Practice/Text-Rendering">Text Rendering </a></li><li id='In-Practice/2D-Game'><span id="menu-item81" class="closed">2D Game </span><ol id="menu-items-of81" style="display:none;"><li id='In-Practice/2D-Game/Breakout'><a id="menu-item82" href="https://learnopengl.com/In-Practice/2D-Game/Breakout">Breakout </a></li><li id='In-Practice/2D-Game/Setting-up'><a id="menu-item88" href="https://learnopengl.com/In-Practice/2D-Game/Setting-up">Setting up </a></li><li id='In-Practice/2D-Game/Rendering-Sprites'><a id="menu-item83" href="https://learnopengl.com/In-Practice/2D-Game/Rendering-Sprites">Rendering Sprites </a></li><li id='In-Practice/2D-Game/Levels'><a id="menu-item84" href="https://learnopengl.com/In-Practice/2D-Game/Levels">Levels </a></li><li id='In-Practice/2D-Game/Collisions'><span id="menu-item85" class="closed">Collisions </span><ol id="menu-items-of85" style="display:none;"><li id='In-Practice/2D-Game/Collisions/Ball'><a id="menu-item95" href="https://learnopengl.com/In-Practice/2D-Game/Collisions/Ball">Ball </a></li><li id='In-Practice/2D-Game/Collisions/Collision-detection'><a id="menu-item96" href="https://learnopengl.com/In-Practice/2D-Game/Collisions/Collision-detection">Collision detection </a></li><li id='In-Practice/2D-Game/Collisions/Collision-resolution'><a id="menu-item97" href="https://learnopengl.com/In-Practice/2D-Game/Collisions/Collision-resolution">Collision resolution </a></li></ol></li><li id='In-Practice/2D-Game/Particles'><a id="menu-item89" href="https://learnopengl.com/In-Practice/2D-Game/Particles">Particles </a></li><li id='In-Practice/2D-Game/Postprocessing'><a id="menu-item90" href="https://learnopengl.com/In-Practice/2D-Game/Postprocessing">Postprocessing </a></li><li id='In-Practice/2D-Game/Powerups'><a id="menu-item91" href="https://learnopengl.com/In-Practice/2D-Game/Powerups">Powerups </a></li><li id='In-Practice/2D-Game/Audio'><a id="menu-item94" href="https://learnopengl.com/In-Practice/2D-Game/Audio">Audio </a></li><li id='In-Practice/2D-Game/Render-text'><a id="menu-item92" href="https://learnopengl.com/In-Practice/2D-Game/Render-text">Render text </a></li><li id='In-Practice/2D-Game/Final-thoughts'><a id="menu-item93" href="https://learnopengl.com/In-Practice/2D-Game/Final-thoughts">Final thoughts </a></li></ol></li></ol></li><li id='Code-repository'><a id="menu-item99" href="https://learnopengl.com/Code-repository">Code repository </a></li><li id='Translations'><a id="menu-item119" href="https://learnopengl.com/Translations">Translations </a></li><li id='About'><a id="menu-item2" href="https://learnopengl.com/About">About </a></li></ol>       <div id="donate">
            <a href="https://www.paypal.me/learnopengl/" target="_blank">
                <div id="donate_img"></div>
                <img style="display: none" src="/img/donate_button_hover.png"/>
                <!--<img id="donate_img" src="img/patreon.png"/>-->
            </a>
          <!--<div id="alipay">
            <img style="width: 150px;" class="clean" src="/img/alipay_logo.png"/>
            <img style="width: 150px; margin-top: 5px" src="/img/alipay.png"/>
          </div>-->
        </div> 
      <div id="menu_book">
            <a href="https://www.amazon.com/dp/9090332561/" target="_blank"><img src="/book/below_menu.png" class="clean"/></a>
        </div>
        <div id="alipay">
          
        </div>
        <div id="ad">
							<!--<div id="waldo-tag-1684"></div>-->
			        </div>
      
        <div id="lefttwothirdad">
            <div id="waldo-tag-2245"></div>
        </div>
    </div>
    
    <div id="content">
    <h1 id="content-title">Introduction</h1>
<h1 id="content-url" style='display:none;'>Introduction</h1>
<p>
	Since you came here you probably want to learn the inner workings of computer graphics and do all the stuff the cool kids do by yourself. Doing things by yourself is extremely fun and resourceful and gives you a great understanding of graphics programming. However, there are a few  items that need to be taken into consideration before starting your journey.
</p>

<h2>Prerequisites</h2>
<p>
	Since OpenGL is a graphics API and not a platform of its own, it requires a language to operate in and the language of choice is <code>C++</code>. Therefore a decent knowledge of the <code>C++</code> programming language is required for these chapters. However, I will try to explain most of the concepts used, including advanced <code>C++</code> topics where required so it is not required to be an expert in <code>C++</code>, but you should be able to write more than just a <code>'Hello World'</code> program. If you don't have much experience with <code>C++</code> I can recommend the free tutorials at <a href="http://www.learncpp.com" target="_blank">www.learncpp.com</a>.
</p>

<p>
	Also, we will be using some math (linear algebra, geometry, and trigonometry) along the way and I will try to explain all the required concepts of the math required. However, I'm not a mathematician by heart so even though my explanations may be easy to understand, they will most likely be incomplete. So where necessary I will provide pointers to good resources that explain the material in a more complete fashion. Don't be scared about the mathematical knowledge required before starting your journey into OpenGL; almost all the concepts can be understood with a basic mathematical background and I will try to keep the mathematics to a minimum where possible. Most of the functionality doesn't even require you to understand all the math as long as you know how to use it.
</p>

<h2>Structure</h2>
<p>
	LearnOpenGL is broken down into a number of general sections. Each section contains several chapters that each explain different concepts in large detail. Each of the chapters can be found at the menu to your left. The concepts are taught in a linear fashion (so it is advised to start from the top to the bottom, unless otherwise instructed) where each chapter explains the background theory and the practical aspects. 
</p>

<p>
  To make the concepts easier to follow, and give them some added structure, the book contains <em>boxes</em>, <em>code blocks</em>, <em>color hints</em> and <em>function references</em>.
</p>

<h3>Boxes</h3>
<note><strong>Green</strong> boxes encompasses some notes or useful features/hints about OpenGL or the subject at hand.</note>
<warning><strong>Red</strong> boxes will contain warnings or other features you have to be extra careful with.</warning>

<h3>Code</h3>
<p>
	You will find plenty of small pieces of code in the website that are located in dark-gray boxes with syntax-highlighted code as you can see below:
</p>

<pre><code>
// This box contains code    
</code></pre>

  <p>
    Since these provide only snippets of code, wherever necessary I will provide a link to the entire source code required for a given subject.
</p>

<h3>Color hints</h3>
<p>
  Some words are displayed with a different color to make it extra clear these words portray a special meaning:
</p>

<ul>
  <li><def>Definition</def>: green words specify a definition i.e. an important aspect/name of something you're likely to hear more often.</li>
  <li><fun>Program structure</fun>: red words specify function names or class names.</li>
  <li><var>Variables</var>: blue words specify variables including all OpenGL constants.</li>
</ul>

<h3>OpenGL Function references</h3>
<p>
	A particularly well appreciated feature of LearnOpenGL is the ability to review most of OpenGL's functions wherever they show up in the content. Whenever a function is found in the content that is documented at the website, the function will show up with a slightly noticeable underline. You can hover the mouse over the function and after a small interval, a pop-up window will show relevant information about this function including a nice overview of what the function actually does. Hover your mouse over <fun><function id='60'>glEnable</function></fun> to see it in action.
</p>

<p>
  Now that you got a bit of a feel of the structure of the site, hop over to the Getting Started section to start your journey in OpenGL!
</p>       

    </div>
    
    <div id="hover">
        HI
    </div>
   <!-- 728x90/320x50 sticky footer -->
<div id="waldo-tag-6196"></div>

   <div id="disqus_thread"></div>

    


</div> <!-- container div -->


</div> <!-- super container div -->
</body>
</html>

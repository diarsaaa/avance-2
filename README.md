<html> 
    <head>      
        <link rel="shortcut icon" type="image/x-icon" href="../IMAGENES/Logo/logo3.ico" />

        <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
        <meta charset="UTF-8">

        <title>A.T Energy</title>

        <link href="CSS/font-awesome-ie7.css" rel="stylesheet" type="text/css"/>
        <link href="CSS/font-awesome-ie7.min.css" rel="stylesheet" type="text/css"/>
        <link href="CSS/font-awesome.css" rel="stylesheet" type="text/css"/>
        <link href="CSS/font-awesome.min.css" rel="stylesheet" type="text/css"/>

        <link href="CSS/Menu.css" rel="stylesheet" type="text/css"/>
        <link href="CSS/Principal.css" rel="stylesheet" type="text/css"/>      
        <link href="CSS/Color_Box.css" rel="stylesheet" type="text/css"/>
        <link href="CSS/Formulario.css" rel="stylesheet" type="text/css"/>

        <link href="CSS/Galeria_Complemento_1.css" rel="stylesheet" type="text/css"/>
        <link href="CSS/Galeria_Complemento_2.css" rel="stylesheet" type="text/css"/> 

        <script src="JS/jquery.min.js" type="text/javascript"></script>
        <script src="JS/jquery.nivo.slider.js" type="text/javascript"></script>
        <script src="JS/jquery.colorbox.js" type="text/javascript"></script>

        <script type="text/javascript">
            $(window).on('load', function () {
                $('#slider').nivoSlider();
            });
        </script>

        <script>
            $(document).ready(function () {
                //Examples of how to assign the ColorBox event to elements
                $(".inline").colorbox({inline: true, width: "50%"});
                $(".callbacks").colorbox({
                    onOpen: function () {
                        alert('onOpen: colorbox is about to open');
                    },
                    onLoad: function () {
                        alert('onLoad: colorbox has started to load the targeted content');
                    },
                    onComplete: function () {
                        alert('onComplete: colorbox has displayed the loaded content');
                    },
                    onCleanup: function () {
                        alert('onCleanup: colorbox has begun the close process');
                    },
                    onClosed: function () {
                        alert('onClosed: colorbox has completely closed');
                    }
                });

                //Example of preserving a JavaScript event for inline calls.
                $("#click").click(function () {
                    $('#click').css({"background-color": "#f00", "color": "#fff", "cursor": "inherit"}).text("Open this window again and this message will still be here.");
                    return false;
                });
            });
        </script>

        <script>
            $(function () {
                var pull = $('#pull');
                menu = $('navegador ul');
                menuHeight = menu.height();

                $(pull).on('click', function (e) {
                    e.preventDefault();
                    menu.slideToggle();
                });
            });

            $(window).resize(function () {
                var w = $(window).width();
                if (w > 320 && menu.is(':hidden')) {
                    menu.removeAttr('style');
                }
            });
        </script>       
    </head>

    <body>
        <div id="principal">
            <header>       

                <div class="logo">                   
                    <img src="IMAGENES/Logo/Logo.png" alt="" height=100% width=10% position=left/>
                </div> 

                <div class="logo2">                  
                    <img src="IMAGENES/Logo/Nombre.png" alt="" height=100% width=50% position=left/>
                    <div id="rs"> 
                        <h5><p style="color:#045FB4">Número de contacto: 565-4052</p></h5> 
                        <h5><p style="color:#DF7401">Correo Electrónico: admin@at-energysac.com</p></h5>    
                    </div> 
                </div>                         
            </header>  
        </div>

    <navegador>
        <ul>
            <li><a href="#"><i class="icon-home"></i>Inicio</a></li>
            <li><a href="#"><i class="icon-money"></i>Productos</a></li>
            <li><a href="#"><i class="icon-paste"></i>Noticias</a></li>
            <li><a class='inline' href="#inline_content"><i class="icon-envelope-alt"></i>Contactanos</a></li>                
        </ul>
        <a id="pull" href="#">Menu</a>
    </navegador>


    <!--Formulario-->
    <div style='display:none'>
        <div id='inline_content' style='padding:10px; background:#fff;'>
            <div id="content">
                <section> 
                    <h1>Solicitud de consulta</h1>
                    <!--Formulario... los datos se mandan a la direccion del servidor e "action"-->
                    <form action="#" method="post">
                        <div>
                            <label for="name">Nombre:</label>
                            <input type="text" id="name" name="user_name" />
                        </div>
                        <div>
                            <label for="mail">E-mail:</label>
                            <input type="email" id="mail" name="user_email" />
                        </div>
                        <div>
                            <label for="msg">Mensaje:</label>
                            <textarea id="msg" name="user_message"></textarea>
                        </div>

                        <div class="button">
                            <button type="reset">Vaciar Campos</button>
                            <button type="submit">Enviar Consulta</button>                                                
                        </div>
                    </form>
                </section>     
            </div>    
        </div>


    </div>

    <!--Galeria Dinamica-->
    <div class="slider-wrapper theme-mi-slider">
        <div id="slider" class="nivoSlider">       
            <img src="IMAGENES/1.jpeg" alt="" title="#Imagen1" /> 
            <img src="IMAGENES/2.jpeg" alt="" title="#Imagen2" />   

        </div>   

        <!--Texto Sobre Imagenes, llamando al nombre de la imagen en id-->    
        <div id="Imagen1" class="nivo-html-caption">
            <h1 style="color:#000000">Imagen 1</h1>
            <div class="Centrales">                      
                <h5>Bienvenidos</h5>
            </div>  
        </div>
        <div id="Imagen2" class="nivo-html-caption">     
            <h1 style="color:#000000">Imagen 2</h1>
            <div class="Centrales">    
                <h5>Bienvenidos</h5>
            </div>
        </div>		
    </div>

</body>
</html>

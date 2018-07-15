# utl_graphics_plotting_rivers_in_brazil_using_sharpefiles
Graphics plotting rivers in brazil using shapefiles.  Keywords: sas sql join merge big data analytics macros oracle teradata mysql sas communities stackoverflow statistics artificial inteligence AI Python R Java Javascript WPS Matlab SPSS Scala Perl C C# Excel MS Access JSON graphics maps NLP natural language processing machine learning igraph DOSUBL DOW loop stackoverflow SAS community.

    Graphics plotting rivers in brazil using shapefiles

    for graphic output
    https://tinyurl.com/y8vhj3lg
    https://github.com/rogerjdeangelis/utl_graphics_plotting_rivers_in_brazil_using_sharpefiles/blob/master/utl_graphics_plotting_rivers_in_brazil_sharpefiles

    WPS Proc R ot IML/R

    * you need these shapefiles;
    https://tinyurl.com/ybqn78ua
    https://sites.google.com/site/joabelb/Home/PrincRiosBrazil.zip

    https://tinyurl.com/ybyf34hx
    ftp://geoftp.ibge.gov.br/organizacao_do_territorio/malhas_territoriais/malhas_municipais/municipio_2017/Brasil/BR/br_unidades_da_federacao.zip

    StackOverflow
    https://tinyurl.com/ya2ssc2y
    https://stackoverflow.com/questions/51333546/how-to-plot-rivers-efficiently

    Carlos Eduardo Lagosta profile
    https://stackoverflow.com/users/9817508/carlos-eduardo-lagosta



    INPUT
    =====

      * you need these shapefiles;
      * download and put individual file in "d:/shp";

      https://tinyurl.com/ybqn78ua
      https://tinyurl.com/ybyf34hx


    PROCESS (all the code)
    ======================

    %utl_submit_wps64('
    options set=R_HOME "C:/Program Files/R/R-3.3.2";
    proc r;
    submit;
    source("C:/Program Files/R/R-3.3.2/etc/Rprofile.site", echo=T);
     library(rgdal);
     library(ggplot2);
     shapeUFs <- readOGR("d:/shp", "BRUFE250GC_SIR");
     shapeHid <- readOGR("d:/shp", "PrincipaisRiosDoBrasil");
     png("d:/png/utl_graphics_plotting_rivers_in_brazil_sharpefiles.png");
     ggplot(shapeUFs, aes(long, lat, group = group)) +
       geom_polygon(fill = "gray90", color = "black") +
       geom_path(data = shapeHid, color = "steelblue2") +
       coord_map() + theme_void();
     dev.off();
     endsubmit;
     run;quit;
    ');


    OUTPUT
    ======

    https://tinyurl.com/y8vhj3lg

    *                _               _       _
     _ __ ___   __ _| | _____     __| | __ _| |_ __ _
    | '_ ` _ \ / _` | |/ / _ \   / _` |/ _` | __/ _` |
    | | | | | | (_| |   <  __/  | (_| | (_| | || (_| |
    |_| |_| |_|\__,_|_|\_\___|   \__,_|\__,_|\__\__,_|

    ;

      * you need these shapefiles;
      * download and put individual file in "d:/shp";

      https://tinyurl.com/ybqn78ua
      https://tinyurl.com/ybyf34hx

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;

    see process

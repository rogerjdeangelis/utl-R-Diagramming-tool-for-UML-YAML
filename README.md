# utl-R-Diagramming-tool-for-UML-YAML
R Diagramming tool for UML YAML.

    R Diagramming tool for UML YAML

    graphic output
    https://tinyurl.com/y7fj67ml
    https://github.com/rogerjdeangelis/utl-R-Diagramming-tool-for-UML-YAML/blob/master/svgout.png

    * other R tools;
    https://tinyurl.com/ya6r4ahn
    https://rstudio-pubs-static.s3.amazonaws.com/31795_b000d8fa834b4cbcb29b1837e5a55a95.html

    github (another example)
    https://github.com/rogerjdeangelis/utl_diagramme_a_flow_with_a_predefined_order_of_the_nodes

    more examples
    http://www.htmlwidgets.org/showcase_diagrammer.html

    https://goo.gl/K5hM
    https://www.google.com/search?q=diagrammer+graphics&rlz=1C1CHBD_enUS743US743&tbm=isch&tbo=u&source=univ&sa=X&ved=0ahUKEwjnraGIs-jVAhUj7YMKHZOUC_0QsAQITw&biw=1590&bih=857

    HJ Allen profile (capture browswer output)
    https://github.com/HJAllen

    StackOverfloW
    https://tinyurl.com/ybc9r5q7
    https://stackoverflow.com/questions/54224618/diagrammer-does-not-accept-specific-syntax-symbols


        WORKING CODE

            draph {
              layout = twopi
              node [shape = circle]
              A -> {B C D}

    HAVE
    ====

      Three four nodes that I need to network

           ___      ___      ___      ___
          /   \    /   \    /   \    /   \
         |  A  |  |  B  |  |  C  |  |  D  |
          \___/    \___/    \___/    \___/

    WANT
    ----
                  ___          ___
                 /   \       /   \
                |  B  |     |  C  |
                 \___/       \___/
                  /\          /\
                   \          /
                     \      /
                      \___ /
                      /   \
                     |  A  |
                      \___/
                        |
                        |
                        |
                       _V_
                      /   \
                     |  D  |
                      \___/

    *                _              _       _
     _ __ ___   __ _| | _____    __| | __ _| |_ __ _
    | '_ ` _ \ / _` | |/ / _ \  / _` |/ _` | __/ _` |
    | | | | | | (_| |   <  __/ | (_| | (_| | || (_| |
    |_| |_| |_|\__,_|_|\_\___|  \__,_|\__,_|\__\__,_|

    ;

    Data is internal to R program

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;

    %utlfkil(d:/png/svgout.png); * delete if exist;

    %utl_submit_r64('
    source("c:/Program Files/R/R-3.4.0/etc/Rprofile.site",echo=T);
    library(DiagrammeR);
    library(DiagrammeRsvg);
    library(rsvg);
    svgout <- grViz("
      draph {
        layout = twopi
        node [shape = circle]
        A -> {B C D}
      }");
    tmp<-capture.output(rsvg_png(charToRaw(export_svg(svgout)),"d:/png/svgout.png"));
    cat("![Need to capture browser output](svgout){#f:svgout}\n\n");
    ');








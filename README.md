# learningCSS3
# a walk through of CSS3

> Relational selectors
> Attribute selectors

> Selectors & Pseduoclasses
> Color models:
       Opactity:
              example: span{ background-color:blue; opacity: 0,5;} - sample6.html
       RGBA color
              example: div{background-color: RGBA(125,125,125,0.5);}
       HSL/HSLA:
              HSL/HSLA color model - Hue (0-359) Saturation (0-100%) Lightness(0-100% - 0% =black - 100% = white; 50% = hue ) Alpha (0-1)
              example: background-color:HSL(200,90%,50%);
                      background-color:HSLA(100,70%,20%,0.5);
 > Border radius:
           Border properties add sharpness to the html element
           border-radius (properties)
             using "/" between two values we can provide elliptical corners.
             example:   10px/20px (%/px)
        border-top-left; 
        border-top-right
        border-bottom-left; 
        border-bottom-right
        example: border-radius : 30px 15px 25px 50px;
        border-radius : 30px;
        
 > Box shadow:
        This adds shadow to the html element.
        example:
                box-shadow: 5px 10px 6px 2 px rbga(20,20,20,.5);
                //horizontal_offset blur_distance vertical_offset spread_distance shadow_color
 > Text Shadowing:
        example: 
            text-shadow: 10px 6px 2px black; 
            //Horizontal_offset vertical_offset blur_distance shadow_color
     more than one text shadow in the same property with comma
        example:
            text-shadow:  4px 4px 2px red, -4px -4px 3px green;
            
 > Glow effect: (glow effect is produced by providing high blur value in text-shadow property with horizontal and vertical offset as zero
         example:
           text-shadow: 0px 0px 10px rgba(255, 0,0,1);
 
 > Border Image
        
 
 
 >  input:focus
 

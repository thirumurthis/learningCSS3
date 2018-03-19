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
 
 > Border Image (used to specify image as a border around the html element.)
 The border-image property allows you to specify an image to be used as the border around an element.
        this is a easy property to set border-source, border-image-slice, border-width,border-outset,border-repeat
        border-image property
        border-source => locaion of the image to be used for border
        border-image-slice => specifies the value to slice image. can have 1 to 4 (top,bottom, left, right) or px 
        border-width
        border-outset => specifies the amount by which border image area extends beyond border box.
        border-repeat => specifies whether the edges of the image should be stretched, repeat, rounded or scaled.
Example:        
 the image to be added as a border will be divided into 9 section
 based on the image slice value of border-image property
 
 once the image is divided into 9 sections, the corner of the image is placed on the corners 
 of the element and so as the edges of the element is placed at the edges.
 
 The edge of the image is scalled or repeated using the border-repeat property.
 
 sample:  border-image-slice : 10% 15% 20% 25%
below is the representation:

 25%   60%     (100-60-25)%
 <--><-------><-->
   1     2     3 /\
                  | 10%
                  \/
                  /\
   4     5     6  |  70%
                  \/
                  /\
   7     8     9  |  (100-70-10)%
                  \/
> border-repeat
         stretch - (default value)
         repeat - image is tiled
         space - image is tiled, with area between the edge with space. if area cannot be filled with a whole number of tiles the extra space is distributed around the tiles. 
         round - the image is tiled, to fill the area between the edges.
         
> fonts:
        web-safe fonts to font-family property
        option of defining web font in CSS3
        
        @font-face rule allows custom fonts to be loaded on a webpage
        once added to the stylesheet file, the rule instructs the browser to download the 
        font from where it is hosted, then display it as specified.
        to create custom font, usage of tool.
        
        example:
        @font-face { font-family : name; src: url("location of custom font file");}
        
        EOT : Embedded open type (Microsoft supported IE)
        OTF/TTF : open type font and true type font in cross platform type format. expert layout features and advanced typographc control 
        SVG - vector re-creation of the font.
        WOFF - web open font format. used on web, this is faster load time.
 
 usage:
    @font-face { font-family: newfont; src: url('fontfile.ttf');}
    #classId { background-color : red; font : bold 1.2em newfont; ....}
     Note: the newfont is specifled in the font property, which is defined using @font-face
     
 Transformation in CSS3:
      the html element getting transformed, such as elements gets rotated/scaled on mouse hover.
      This is generally achieved by javascript code/ framework.
      CSS3 has introduced transformations using which we can transform html.
      Transformation is used to create dynamic web pages.
      CSS3 enables to move, tilt, scale element of web page with ease.
      CSS3 - 
             Translate
             Scale
             Rotate
             Skew
      translate() function is moved an element from one position to another position.
      
      sample: 
           translate(x,y) -> moves right by x-value (when positive) left when x-value is -ve; and y-value down from current position
           translate(20px,30px) ; 
           translate(-40px, 20px); => moved
           transalte (30px,-25px);
           
       scale () function is uses to change (increase/decreast) the size of the element
       
       scale(x,y) -> scale the element x-value of width & y value of height
       if scale(value) - x and y will be considered as same.
           scale(2,1); - doubles
           scale(0.5); - decrease half
       
       rotate() function is used to rotate and element from its origin up to an specified angle.
       rotate (x); x - +ve element rotates clockwise lese anti-clockwise.
            rotate(20deg)
            
       skew () function is used to turn/skew any element to any angle.
       skew (x,y) -> skews the element from x degrees from the x-axis and y degress from y-axis
             skew(30deg,10deg)
             skewX(15deg) - skew element 15 deg accross x axis
             skewY(45deg)
             
             
    > Transitions in CSS3
          to show gradual change in the CSS properties of an element during an interval of time.
          like changing one style to another.
          transition has two things to be specified
             CSS proeprty effect should be added 
             duration of the effect
          sample:
              transition: height 3s;
                  height is the property to be transitioned.
                  
            transition is short-hand property to specify
              transition- property (height, width, background, etc.)
              transition-duration (sec/msec) duration - if not provided no effects happens
              transition-timing-function (controls the pace or speed of the transition)
              transition-delay (delay before starting the transition)
              
          transition-timing-function:
           ease
           linear
           ease-in
           ease-out
           ease-in-out
           steps
           
           multiple transtion-time-function
                  transtion-time-function: ease,linear;
           
           custom function can also be specified using four co-ordinates to define a cubic bezier curve.
           
                  cubic-bezier(x1,y1,x2,y2);
                  x1,y2 -> start and end of the curve (0 & 1 default values)
                  y1,x2 -> specify x and y co-ordinates of cubic bezier curve function
                  
                        cubic-bezier(0,1.1,0.9,4);
                        
                        
           steps () timing function enables us to break the transtion into steps
                      steps(int, start|end);
                         int - speifies the number of intervals to which the transition should be broken, should be +ve >0
                      2 pre-defined variants of step function
                              step-start = step(1,start)
                              step-end = step(1,end)
             div{ transition: 4s steps(5); }
             
 Animation:
          transition can only provide dynamic effects to the page
          transition can start only when some events like hover, focus occurs.
          only the initial state and finale state for transition can be specified, cannot provide intermidiate state.
    animation can be used to replace animated images, scripts or flash.
    
    animation is done is using key frames:
      with each frame the start, end and smooth transition is performed.
   the change will happen using from & to keywords or value in percentage 0% to 100%.
   
   sample:
     @keyframes anim{
           from { color:white; background:black;}
           to{ color:black; background: white;}
           }
     @keyframes anim{
           0% { color:white; background:black;}
           100%{ color:black; background: white;}
           }
   properties:
         animation-name
         animation-duration
         animation-timing
         
media queries:
    where you want the webpage to look uniform in all the devices
    responsiveness 
    when the website is viwed in mobile phone the layout should adjust according to the screen size.
    
    media query helps in presenting the content tailored to a specific range of output devices without having to change the content
    media query consits of media type followed by at least one expression.
        there can be one or more media expression expressed as bollean expression
    The result of the query is true if media type specified in the media query matches the type of device the document is being displayed on and all expression in the media query are true.
    
    media queries uses @media rule to include a block of CSS properties, if the media feature condition is true
    @media rule is used to define different style rules for different media types/devices.
    
    Media quries look the capablilty of the device, and can be used for checking many things as,
        width and height of the viewport
        width and height of the device
        orientation 
        resolution and much more
        
    
        
    
    
      
      
         
 >  input:focus
 >  input:hover

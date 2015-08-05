# Print-Preview
JQuery plugin to print preview specific div,p or any other object with css applied

Consider we have div at our page with id="masterContent" we want to print only that div
-----------------
 &lt;div id="masterContent"> 
-----------------

 in head section
Include JQuery library as 

-----------------
&lt;script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"> &lt;/script>
-----------------

or include your local copy

Include printPreview library as 

-----------------
&lt;script type="text/javascript" src="js/printPreview.js">&lt;/script>
-----------------

write one more script tag without src attribute for our JQuery section to initiate our Plugin as below 

-----------------
  &lt;script type="text/javascript">
        $(function(){
        
            $("#btnPrint").printPreview({
            
                obj2print:'#masterContent',
                width:'810'
                
                /*optional properties with default values*/
                //obj2print:'body',     /*if not provided full page will be printed*/
                //style:'',             /*if you want to override or add more css assign here e.g: "<style>#masterContent:background:red;</style>"*/
                //width: '670',         /*if width is not provided it will be 670 (default print paper width)*/
                //height:screen.height, /*if not provided its height will be equal to screen height*/
                //top:0,                /*if not provided its top position will be zero*/
                //left:'center',        /*if not provided it will be at center, you can provide any number e.g. 300,120,200*/
                //resizable : 'yes',    /*yes or no default is yes, * do not work in some browsers*/
                //scrollbars:'yes',     /*yes or no default is yes, * do not work in some browsers*/
                //status:'no',          /*yes or no default is yes, * do not work in some browsers*/
                //title:'Print Preview' /*title of print preview popup window*/
                
            });
        });
 &lt;/script>
-----------------

if you have "print Preview" button residing within the target object which we are printing, that button will not be displayed in print/preview.

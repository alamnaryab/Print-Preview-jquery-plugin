;(function ( $ ) {
    $.fn.printPreview = function( options ) {
        var elem = this;
        
        var opt = $.extend({
            obj2print:'body',
            style:'',
            width:'670',
            height:screen.height-105,
            top:0,
            left:'center',
            resizable : 'yes',
            scrollbars:'yes',
            status:'no',
            title:'Print Preview'
        }, options );
        if(opt.left == 'center'){
            opt.left=(screen.width/2)-(opt.width/2);
        }
        
        return elem.bind("click.printPreview", function () {
            var btnCode = elem[0].outerHTML;
            var headString = '';
            headString = $("head").html();
            var str = "<!DOCTYPE html><html><head>"+headString+opt.style+"</head><body>";
            str+=$(opt.obj2print)[0].outerHTML.replace(btnCode,'')+"</body></html>";
            var newWindow = window.open(
                    "", 
                    "newWindow", 
                    "width="+opt.width+
                    ",top="+opt.top+
                    ",height="+opt.height+
                    ",left="+opt.left+
                    ",resizable="+opt.resizable+
                    ",scrollbars="+opt.scrollbars+
                    ",status="+opt.status
                    );
            newWindow.document.write(str);
            newWindow.document.title = opt.title;
        });
    };
}( jQuery ));

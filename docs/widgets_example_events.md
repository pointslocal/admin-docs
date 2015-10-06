# Example Widgets
> The following widgets are created utilizing jQuery and Pagu.  Neither are required, but demonstrate a simple application of the API :: Widget pipeline.



## Events This Week
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
<script>
var template = '<div class="widget"><h3>Happening This Week</h3>{{items.each}}<div class="event"><a href="">{{title}}</a><div>{{date}} - {{start_time}}</div></div>{{/items.each}}</div>';
$.getJSON('http://maine.pointslocal.com/api/v1/events?count=5&date=this%20week',function(d) {
  var p = new Pagu(d,template);
  $('#widget1').html(p.parsed);
});
</script>

```
<style type="text/css">
.widget {
  margin: auto;
  border-radius: 2px;
  background-color: #fff;
  border: 1px solid #eee;
  padding: 10px;
}
.event {
  padding-top: 20px;
  padding-bottom: 20px;
  border-bottom: 1px solid #eee;
}
.event:last-child {
  border-bottom: 1px solid rgba(255,255,255,0);
}
</style>
<div id="widget1"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
<script href="http://cdn.pointslocal.com/pagu.min.js" type="text/javascript"></script>
<script>
var Pagu=function(e,a){"use strict";var r=this;r.obj=e,r.template=a,r.parsed=a,r.grammar={tokens:[],whitespace:[" "],operations:["each","is","!is","if","!if","empty"],tags:["{{","}}","{{/"],operators:["."],ctlchr:[]},this.escapeRegexp=function(e){return new RegExp(e.replace(/[\-\[\]\/\{\}\(\)\*\+\?\.\\\^\$\|]/g,"\\$&"),"gm")},this.Pagu=function(e,a){var p=e?e:r.obj,n=a?a:r.parsed;for(var c in p)if(p.hasOwnProperty(c)){p[c]&&"[object Function]"==={}.toString.call(p[c])&&(p[c]=p[c]());for(var g=new RegExp("{{"+c+"\\.if}}(.*?){{/"+c+"\\.if}}","gm"),t=g.exec(n);null!=t;){var i=t[1],s=r.escapeRegexp(t[0]);n=p[c]?n.replace(s,i):n.replace(s,""),t=g.exec(n)}var l=new RegExp("{{"+c+"\\.(is|!is)\\((.*?)\\)}}(.*?){{/"+c+"\\.(\\1)}}","gm");console.log("pat: "+l);for(var o=l.exec(n);null!=o;){var x="!is"===o[1]?!1:!0,f=o[2],m=new RegExp(o[0].replace(/[\-\[\]\/\{\}\(\)\*\+\?\.\\\^\$\|]/g,"\\$&"),"gm"),u="";f==p[c]===x&&(u=o[3]),n=n.replace(m,u),o=l.exec(n)}var v=new RegExp("{{"+c+"}}","gi");if(n=n.replace(v,p[c]),p[c]instanceof Array){var h="{{"+c+".empty}}(.*?){{/"+c+".empty}}",w=new RegExp(h,"gim");n=p[c].length<1?n.replace(w,"$1"):n.replace(w,"");for(var R="{{"+c+".each}}(.*?){{/"+c+".each}}",E=".*?"+R+".*",$=new RegExp(R,"gim"),d=new RegExp(E,"gim"),y=n.replace(d,"$1"),P="",b=0;b<p[c].length;b++)P+=r.Pagu(p[c][b],y);n=n.replace($,P)}}var j=new RegExp("{{([A-Za-z_0-9])+..*?}}(.*?){{/\\1.*?}}","gm");n=n.replace(j,"");var A=new RegExp("{{([A-Za-z_0-9])+}}","gm");return n=n.replace(A,""),r.parsed=n,r.parsed},this.parse=function(){return r.parsed},r.Pagu()};
var template = '<div class="widget"><h3>Happening This Week</h3>{{items.each}}<div class="event"><a href="">{{title}}</a><div>{{date}} - {{start_time}}</div></div>{{/items.each}}</div>';
$.getJSON('http://maine.pointslocal.com/api/v1/events?count=5&date=this%20week',function(d) {
  var p = new Pagu(d,template);
  $('#widget1').html(p.parsed);
});
</script>
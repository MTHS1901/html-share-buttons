<style>
   @media only screen and (max-width: 992px) {
   .compartilhe {
   position: fixed;
   right: 0;
   bottom: 0;
   width: 102%;
   margin: -1px;
   height: 40px;
   text-align: center;
   z-index: 99999;
   background: #fff;
   }
   .compartilhe-desktop {
   display: none;}
   }
   .compartilhe{animation:animatebottom 0.3s}@keyframes animatebottom{from{bottom:-300px;opacity:0} to{bottom:0;opacity:1}}
   @media only screen and (min-width: 992px) {
   .compartilhe {
   position: fixed;
   left: 10px;
   bottom: 30px;
   width: 320px;
   padding: 10px;
   text-align: center;
   z-index: 99999;
   background: #fff;
   border: solid 1px;
   border-radius: 3px;
   }
   .compartilhe-desktop {
   display: block;}
   #whatsapp {display: none;}
   }
   .fa {
   padding: 14px;
   font-size: 15px!important;
   width: 20%;
   text-align: center;
   text-decoration: none;
   margin: 0px -2px;
   background: #000;
   }
   .fa:hover {
   text-decoration: none!important;
   }
   .fa-facebook {
   background: rgb(59, 89, 152);
   color: white!important;}
   .fa-whatsapp {
   background: rgb(77, 194, 71);
   color: white!important;
   }
   .fa-twitter {
   background: rgb(29, 161, 242);
   color: white!important;
   }
   .fa-telegram {
   background: rgb(0, 136, 204);
   color: white!important;
   }
   .fa-copy {
   background: black;
   color: white!important;
   }
</style>
<div class="compartilhe">
   <div class="compartilhe-desktop" >Compartilhe:</div>
   <a href="#" target="_blank" onclick="window.open('whatsapp://send?text=' + encodeURIComponent(document.URL) + '&quote=' + encodeURIComponent(document.URL)); return false;" id="whatsapp" class="fa fa-whatsapp"></a>
   <a href="#" target="_blank" onclick="window.open('https://fb.com/sharer/sharer.php?u=' + encodeURIComponent(document.URL) + '&quote=' + encodeURIComponent(document.URL)); return false;" class="fa fa-facebook"></a>
   <button onclick="CopyLink()" class="fa" style="border:none"><i class="fa-copy"></i></button>
   <a href="#" target="_blank" onclick="window.open('https://twitter.com/intent/tweet?text=' + encodeURIComponent(document.URL) + '&quote=' + encodeURIComponent(document.URL)); return false;" class="fa fa-twitter"></a>
   <a href="#" target="_blank" onclick="window.open('https://telegram.me/share/url?url=' + encodeURIComponent(document.URL) + '&quote=' + encodeURIComponent(document.URL)); return false;" class="fa fa-telegram"></a>
</div>
<script>
   function copyTextToClipboard(text) {
     var textArea = document.createElement("textarea");
     textArea.style.position = 'fixed';
     textArea.style.top = 0;
     textArea.style.left = 0;
     textArea.style.width = '2em';
     textArea.style.height = '2em';
     textArea.style.padding = 0;
     textArea.style.border = 'none';
     textArea.style.outline = 'none';
     textArea.style.boxShadow = 'none';
     textArea.value = text;
     document.body.appendChild(textArea);
     textArea.select();
     try {
       var successful = document.execCommand('copy');
    alert("Link copiado!");
     } catch (err) {
       alert("Erro ao copiar link!");
     }
   
     document.body.removeChild(textArea);
   }
   
   function CopyLink() {
     copyTextToClipboard(location.href);
   }
</script>
</div>

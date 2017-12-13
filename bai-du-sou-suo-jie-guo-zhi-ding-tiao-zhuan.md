      var ref=window.document.referrer;
      //ref=ref==""?window.opener.location:ref;
      var u=decodeURIComponent(ref);
      var q=getKey(u);
      
      
      function getKey(url){
      var K='';
      if(url.indexOf('baidu.com')!=-1){
      K = Key(url,'wd=');
      }
      else if(url.indexOf('utm_term')!=-1){
      K = Key(url,'utm_term=');
      }
          else if(url.indexOf('google.com')!=-1){
      K = Key(url,'q=');
      //K='多动症';
      }
      return K;
      }
      
      function Key(url,cs){
      var start=url.indexOf(cs);
      url=url.slice(start+cs.length);
      var end=url.indexOf('&');
      var key=url.slice(url,end);
      return key;
      }
      
      
      var reg=/(sogou.com|soso.com|gougou.com|baidu.com|google.com|youdao.com|360.com)/;
      if(reg.test(ref)){
         //if(!+[1,]){
           //window.opener.location='http://www.site.com/plus/search.php?q='+q;
      //window.open('http://www.site.com/plus/search.php?q='+q,'_parent',''); 
         //}else
         //{
      //window.opener.location.href ='http://www.site.com/plus/search.php?q='+q;
      window.opener.location.href="http://www.site.com/plus/search.php?q="+q;
      //}
      }
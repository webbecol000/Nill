

<!DOCTYPE html>

<html>
  <head>
    <meta http-equiv="X-UA-Compatible" content="IE=Edge" /><script type="text/javascript">window.NREUM||(NREUM={}),__nr_require=function(e,n,t){function r(t){if(!n[t]){var o=n[t]={exports:{}};e[t][0].call(o.exports,function(n){var o=e[t][1][n];return r(o||n)},o,o.exports)}return n[t].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<t.length;o++)r(t[o]);return r}({1:[function(e,n,t){function r(){}function o(e,n,t){return function(){return i(e,[c.now()].concat(u(arguments)),n?null:this,t),n?void 0:this}}var i=e("handle"),a=e(3),u=e(4),f=e("ee").get("tracer"),c=e("loader"),s=NREUM;"undefined"==typeof window.newrelic&&(newrelic=s);var p=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],d="api-",l=d+"ixn-";a(p,function(e,n){s[n]=o(d+n,!0,"api")}),s.addPageAction=o(d+"addPageAction",!0),s.setCurrentRouteName=o(d+"routeName",!0),n.exports=newrelic,s.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(e,n){var t={},r=this,o="function"==typeof n;return i(l+"tracer",[c.now(),e,t],r),function(){if(f.emit((o?"":"no-")+"fn-start",[c.now(),r,o],t),o)try{return n.apply(this,arguments)}catch(e){throw f.emit("fn-err",[arguments,this,e],t),e}finally{f.emit("fn-end",[c.now()],t)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(e,n){m[n]=o(l+n)}),newrelic.noticeError=function(e){"string"==typeof e&&(e=new Error(e)),i("err",[e,c.now()])}},{}],2:[function(e,n,t){function r(e,n){if(!o)return!1;if(e!==o)return!1;if(!n)return!0;if(!i)return!1;for(var t=i.split("."),r=n.split("."),a=0;a<r.length;a++)if(r[a]!==t[a])return!1;return!0}var o=null,i=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var u=navigator.userAgent,f=u.match(a);f&&u.indexOf("Chrome")===-1&&u.indexOf("Chromium")===-1&&(o="Safari",i=f[1])}n.exports={agent:o,version:i,match:r}},{}],3:[function(e,n,t){function r(e,n){var t=[],r="",i=0;for(r in e)o.call(e,r)&&(t[i]=n(r,e[r]),i+=1);return t}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],4:[function(e,n,t){function r(e,n,t){n||(n=0),"undefined"==typeof t&&(t=e?e.length:0);for(var r=-1,o=t-n||0,i=Array(o<0?0:o);++r<o;)i[r]=e[n+r];return i}n.exports=r},{}],5:[function(e,n,t){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(e,n,t){function r(){}function o(e){function n(e){return e&&e instanceof r?e:e?f(e,u,i):i()}function t(t,r,o,i){if(!d.aborted||i){e&&e(t,r,o);for(var a=n(o),u=v(t),f=u.length,c=0;c<f;c++)u[c].apply(a,r);var p=s[y[t]];return p&&p.push([b,t,r,a]),a}}function l(e,n){h[e]=v(e).concat(n)}function m(e,n){var t=h[e];if(t)for(var r=0;r<t.length;r++)t[r]===n&&t.splice(r,1)}function v(e){return h[e]||[]}function g(e){return p[e]=p[e]||o(t)}function w(e,n){c(e,function(e,t){n=n||"feature",y[t]=n,n in s||(s[n]=[])})}var h={},y={},b={on:l,addEventListener:l,removeEventListener:m,emit:t,get:g,listeners:v,context:n,buffer:w,abort:a,aborted:!1};return b}function i(){return new r}function a(){(s.api||s.feature)&&(d.aborted=!0,s=d.backlog={})}var u="nr@context",f=e("gos"),c=e(3),s={},p={},d=n.exports=o();d.backlog=s},{}],gos:[function(e,n,t){function r(e,n,t){if(o.call(e,n))return e[n];var r=t();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(e,n,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return e[n]=r,r}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(e,n,t){function r(e,n,t,r){o.buffer([e],r),o.emit(e,n,t)}var o=e("ee").get("handle");n.exports=r,r.ee=o},{}],id:[function(e,n,t){function r(e){var n=typeof e;return!e||"object"!==n&&"function"!==n?-1:e===window?0:a(e,i,function(){return o++})}var o=1,i="nr@id",a=e("gos");n.exports=r},{}],loader:[function(e,n,t){function r(){if(!E++){var e=x.info=NREUM.info,n=l.getElementsByTagName("script")[0];if(setTimeout(s.abort,3e4),!(e&&e.licenseKey&&e.applicationID&&n))return s.abort();c(y,function(n,t){e[n]||(e[n]=t)}),f("mark",["onload",a()+x.offset],null,"api");var t=l.createElement("script");t.src="https://"+e.agent,n.parentNode.insertBefore(t,n)}}function o(){"complete"===l.readyState&&i()}function i(){f("mark",["domContent",a()+x.offset],null,"api")}function a(){return O.exists&&performance.now?Math.round(performance.now()):(u=Math.max((new Date).getTime(),u))-x.offset}var u=(new Date).getTime(),f=e("handle"),c=e(3),s=e("ee"),p=e(2),d=window,l=d.document,m="addEventListener",v="attachEvent",g=d.XMLHttpRequest,w=g&&g.prototype;NREUM.o={ST:setTimeout,SI:d.setImmediate,CT:clearTimeout,XHR:g,REQ:d.Request,EV:d.Event,PR:d.Promise,MO:d.MutationObserver};var h=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1099.min.js"},b=g&&w&&w[m]&&!/CriOS/.test(navigator.userAgent),x=n.exports={offset:u,now:a,origin:h,features:{},xhrWrappable:b,userAgent:p};e(1),l[m]?(l[m]("DOMContentLoaded",i,!1),d[m]("load",r,!1)):(l[v]("onreadystatechange",o),d[v]("onload",r)),f("mark",["firstbyte",u],null,"api");var E=0,O=e(5)},{}]},{},["loader"]);</script><script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","queueTime":0,"licenseKey":"1c6ed9743c","agent":"","transactionName":"M1IHN0NYXEZWAEFRCgoYIxZfWkZcWA0aSBcLXQAARUocQ14GQktfNEUKCVRaRnFSF1RRCTJeABQfXldB","applicationID":"2845391","errorBeacon":"bam.nr-data.net","applicationTime":144}</script>
     
    <meta name="google-site-verification" content="m_3TAXDreGTFyoYnEmU9mcKB4Xtw5mw6yRkuJtXRKxM" />
    <title>Nill V.1.X.6.4 (UPDATE) on Scratch</title>
    

<meta name="description" content="Nill V.1.X.6.4 (UPDATE) on Scratch by webbecol000" />


    <link rel="stylesheet" href="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/vendor/redmond/jquery.ui.all.css" />
    
        <link href="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/css/main.css" rel="stylesheet" type="text/css" />
   
   <link rel="stylesheet" href="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//css/handheld.css" media="handheld, only screen and (max-device-width:480px)"/>

    
    
        <link href="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/css/project_base.css" rel="stylesheet" type="text/css" />
    
    <link href="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//vendor/redmond/jquery-ui.css" rel="stylesheet">
    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/swfobject.js"></script>

    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/jquery.min.js"></script>
    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/lib/underscore-min.js"></script>
    
    <script>
      window.console||(window.console={log:$.noop,error:$.noop,debug:$.noop}); // ensure console fails gracefully when missing
      // define _gaq here to log errors with GA. ga.js script gets loaded furthe down
      var sessionCookieName = 'scratchsessionsid';
      var _gaq = window._gaq || [];
      _gaq.push(['_setAccount', 'UA-30688952-1']);
      _gaq.push(['_setSampleRate', '10']);
      _gaq.push(['_trackPageview']);
      
      
      
      _gaq.push(['_setCustomVar', 2, 'status', 'logged_in', 2]);
      
      

      
    </script>
    <script type="text/javascript">
        function getCookie(name) {
            var cookieValue = null;
            if (document.cookie && document.cookie != '') {
                var cookies = document.cookie.split(';');
                for (var i = 0; i < cookies.length; i++) {
                    var cookie = jQuery.trim(cookies[i]);
                    // Does this cookie string begin with the name we want?
                    if (cookie.substring(0, name.length + 1) == (name + '=')) {
                        cookieValue = decodeURIComponent(cookie.substring(name.length + 1));
                        break;
                    }
                }
            }
            return cookieValue;
        }

        function setCookie(name, value, days) {
            var expires;

            if (days) {
                var date = new Date();
                date.setTime(date.getTime() + (days * 24 * 60 * 60 * 1000));
                expires = "; expires=" + date.toGMTString();
            } else {
                expires = "";
            }
            document.cookie = escape(name) + "=" + escape(value) + expires + "; path=/";
        }
    </script>
    
  <script>
    

var Scratch = Scratch || {};
Scratch.INIT_DATA = Scratch.INIT_DATA || {};



Scratch.INIT_DATA.ADMIN = false;
Scratch.INIT_DATA.LOGGED_IN_USER = {
  
  model: {
    username: 'webbecol000',
    username_truncated: 'webbecol000',
    has_outstanding_email_confirmation: 'false',
    
    id: 26049657,
    profile_url: '/users/webbecol000/',
    thumbnail_url: '//uploads.scratch.mit.edu/users/avatars/26049657.png'
     
  },
  
  options: {
    
      authenticated: true
     
    
,
permissions: [
    'edit-project'
]

  }
};
Scratch.INIT_DATA.comment_posting = true;

Scratch.INIT_DATA.BROWSERS_SUPPORTED = {

  chrome: 35,
  firefox: 31,
  msie: 8,
  safari: 7
};

Scratch.INIT_DATA.TEMPLATE_CUES = {

  unsupported_browser: true,
  welcome: true,
  confirmed_email: false
};
  




Scratch.INIT_DATA.PROJECT = {
  
  model: {
    id: 244087899,
    title: 'Nill V.1.X.6.4 (UPDATE)',
    notes: 'Please like and favorite this game so I will be motivated to update it more often! Keep playing Nill and have fun.\u000AWARNING: INSANE MODE IS EXTREMELY HARD BUT EXTREMELY FUN! If you can beat the highscores on ANY mode, I will follow you and tell you what inspired me to make this game.\u000A\u000ACredit to TrapMusicHDTV for: \u000AGhostBusters Theme Song Remix\u000A\u000ADubstepGutter for \u000AFur Elise Trap Remix',
    credits: 'Instructions: To play, click on the game mode you want to play on. Answer the question. And use the Arrow Keys to move the bar.\u000AOn survival mode, press 1 and 2 to switch between guns.\u000A\u000A   WARNING: INSANE MODE IS EXTREMELY HARD BUT EXTREMELY FUN! IF YOU CAN BEAT THE NILL HIGH\u002DSCORE ON EITHER MODE, I WILL FOLLOW YOU AND GIVE YOU A NILL TOUR THROUGH THE COMMENTS. \u000A________________________________________\u000AYOU MUST HAVE AN ACCOUNT TO DO SO!!!    l  ________________________________________l\u000A\u000AUpdates Coming SOON! Keep calm and Scratch on!\u000A\u000A\u002DUpdate\u002D V.4.J.9.6.3\u000AMore Power\u002DUps!\u000AMore Game Modes!\u000ASurvival WAVES\u000AMORE!\u000A_______________________________________________________',
    creator: 'webbecol000',
    modifiedDate: '2018\u002D11\u002D26 15:49:59',
    isPublished: true,
    comments_allowed: true
  },
  is_new: false,

  is_censored: false,
  is_permcensored: false,

  reportText: {
    "": "Select a reason why above",
    "0": "Please provide a link to the original project",
    "1": "Please provide links to the uncredited content",
    "2": "Please say why the project is too violent or scary",
    "3": "Please say where the inappropriate language occurs in the project (For example: Notes \u0026 Credits, sprite name, project text, etc.)",
    "4": "Please say the name of the audio file with the inappropriate music",
    "5": "Please say where the personal contact information is shared (For example: Notes \u0026 Credits, sprite name, project text, etc.)",
    "6": "Please be specific about why this project does not follow our Community Guidelines",
    "8": "Please say the name of the sprite or the backdrop with the inappropriate image"
  }

  
  ,embedUrl: 'http://scratch.mit.edu/projects/embed/244087899/'
  
  
}

Scratch.INIT_DATA.HAS_NEVER_REMIXED = false;

Scratch.INIT_DATA.TIPS = {
  HELP_URLS : {
    
      'ab': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ab/",
    
      'ar': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ar/",
    
      'an': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/an/",
    
      'ast': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ast/",
    
      'id': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/id/",
    
      'ms': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ms/",
    
      'be': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/be/",
    
      'bg': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/bg/",
    
      'ca': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ca/",
    
      'cs': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/cs/",
    
      'cy': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/cy/",
    
      'da': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/da/",
    
      'de': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/de/",
    
      'yum': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/yum/",
    
      'et': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/et/",
    
      'el': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/el/",
    
      'en': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/en/",
    
      'eo': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/eo/",
    
      'es': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/es/",
    
      'eu': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/eu/",
    
      'fa': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/fa/",
    
      'fr': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/fr/",
    
      'fur': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/fur/",
    
      'ga': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ga/",
    
      'gd': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/gd/",
    
      'gl': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/gl/",
    
      'ko': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ko/",
    
      'hy': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/hy/",
    
      'he': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/he/",
    
      'hi': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/hi/",
    
      'hr': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/hr/",
    
      'zu': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/zu/",
    
      'is': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/is/",
    
      'it': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/it/",
    
      'kn': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/kn/",
    
      'kk': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/kk/",
    
      'rw': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/rw/",
    
      'ht': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ht/",
    
      'ku': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ku/",
    
      'la': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/la/",
    
      'lv': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/lv/",
    
      'lt': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/lt/",
    
      'mk': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/mk/",
    
      'hu': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/hu/",
    
      'ml': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ml/",
    
      'mt': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/mt/",
    
      'mr': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/mr/",
    
      'cat': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/cat/",
    
      'mn': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/mn/",
    
      'my': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/my/",
    
      'nl': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/nl/",
    
      'ja': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ja/",
    
      'ja-hr': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ja-hr/",
    
      'nb': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/nb/",
    
      'nn': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/nn/",
    
      'uz': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/uz/",
    
      'th': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/th/",
    
      'pl': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/pl/",
    
      'pt': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/pt/",
    
      'pt-br': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/pt-br/",
    
      'ro': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ro/",
    
      'ru': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/ru/",
    
      'sc': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/sc/",
    
      'sq': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/sq/",
    
      'sk': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/sk/",
    
      'sl': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/sl/",
    
      'sr': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/sr/",
    
      'fi': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/fi/",
    
      'sv': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/sv/",
    
      'te': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/te/",
    
      'nai': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/nai/",
    
      'vi': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/vi/",
    
      'tr': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/tr/",
    
      'uk': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/uk/",
    
      'zh-cn': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/zh-cn/",
    
      'zh-tw': "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/help/zh-tw/",
    
  },

  CURRENT_LANGUAGE: "en",
};




Scratch.INIT_DATA.COI = {
  TARGET_DOMAIN: "http://cdn.scratch.mit.edu"
};




Scratch.INIT_DATA.IS_IP_BANNED = false;

Scratch.INIT_DATA.GLOBAL_URLS = {
  'media_url': '//uploads.scratch.mit.edu/',
  'static_url': '//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/',
  'static_path': '/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/'
}

Scratch.INIT_DATA.IS_SOCIAL = true;

Scratch.ALERT_MSGS = {
  'error': 'Oops! Something went wrong',
  'inappropriate-generic': 'Hmm...the bad word detector thinks there is a problem with your text. Please change it and remember to <a target="_blank" href="/community_guidelines/">be respectful</a>.',
  'image-invalid': 'Upload a valid image. The file you uploaded was either not an image or a corrupted image.',
  'thumbnail-missing': 'Missing file',
  'thumbnail-upload-bad': 'Bad upload',
  'thumbnail-too-large': 'Maximum file size is 1 MB.',

  'inappropriate-comment': 'Hmm...the bad word detector thinks there is a problem with your comment. Please change it and remember to <a target="_blank" href="/community_guidelines/">be respectful</a>.',
  'comment-has-chat-site': 'Uh oh! This comment contains a link to a website with unmoderated chat. For safety reasons, please do not link to these sites!',

  'empty-comment': "You can't post an empty comment!",
  'delete_comment': '<div title="Delete Comment?"><p>Are you sure you want to delete this comment? If the comment is mean or disrespectful, please click report instead, to let the Scratch Team know about it.</p></div>',
  'report_comment': '<div title="Report Comment?"></p>Are you sure you want to report this comment?</p></div>',
  'report_comment_educator': '<div title="Delete Comment?"></p>Are you sure you want to delete this comment?</p></div>',
  'followed': 'You are now following ',
  'unfollowed': 'You are no longer following ',
  'comment-spam': "Hmm, seems like you've posted the same comment a bunch of times. Please don't spam.",
  'comment-flood': "Woah, seems like you're commenting really quickly. Please wait longer between posts.",
  'comment-muted': "Hmm, the filterbot is pretty sure your recent comments weren't ok for Scratch, so your account has been muted for the rest of the day. :/",
  'comment-unconstructive': "Hmm, the filterbot thinks your comment may be mean or disrespectful. Remember, most projects on Scratch are made by people who are just learning how to program. Read the <a href='/community_guidelines'>community guidelines</a>, and be nice.",
  'comment-disallowed': "Hmm, it looks like comments have been turned off for this page. :/",
  'project-complaint-length': "That's too short. Please describe in detail what's inappropriate or disrespectful about the project.",
  'project-complaint-buglength': "That's too short! Please describe in detail what you expected the project to do, and how exactly it is broken. Thanks!",
  'editable-text-too-long': "That's too long! Please find a way to shorten your text."

  ,"notes-changed": "Changes saved",
  "added-to-studio": "Added to studio",
  "tags-changed": "Changes saved",
  "tags-limited": "Limit of 3 tags.",
  "tags-edit-error": "Server error when editing tag.  Please reload the page to see updates.",
  "inappropriate-tag": "Hmm...the bad word detector thinks there is a problem with your tag. Please change it and remember to <a target=\"_blank\" href=\"/community_guidelines/\">be respectful</a>.",
  "project-complaint-type": "Please choose a reason for reporting this project from the dropdown."


}


  </script>


    <meta property="og:type" content="website" />
    
    <meta property="og:description" content="Make games, stories and interactive art with Scratch. (scratch.mit.edu)"/>
    

    

<meta property="og:title" content="Scratch - Nill V.1.X.6.4 (UPDATE)"/>
<meta property="og:description" content="Instructions: To play, click on the game mode you want to play on. Answer the question. And use the Arrow Keys to move the bar. On survival mode, press 1 and 2 to switch between guns. WARNING: INSANE MODE IS EXTREMELY HARD BUT EXTREMELY FUN! IF YOU CAN BEAT THE ..." />



  </head>

  <body class="" >
  <!--[if lte IE 8]>
  <div class="unsupported-browser banner" data-cue="unsupported_browser">
    <div class="container">
      <span>Scratch supports Internet Explorer 9+. We suggest you upgrade to <a href="/info/faq/#requirements">a supported browser</a>, <a href="/scratch2download/">download the offline editor</a>, or <a href="https://en.scratch-wiki.info/wiki/List_of_Bug_Workarounds">read about common workarounds</a>.</span>
    </div>
  </div>
  <![endif]-->
    <div id="pagewrapper">
      
      
      <div id="topnav" >
      <div class="innerwrap">
        <div class="container">
          <a href="/" class="logo"><span class="scratch"></span></a>
          <ul class="site-nav">
            <li><a id="project-create" href="/projects/editor/?tip_bar=home">Create</a></li><li><a href="/explore/projects/all">Explore</a></li><li ><a href="/tips">Tips</a></li><li class="last"><a href="/about/">About</a></li>
          </ul>
          
          <form class="search" action="/search/projects" method="get" class="search">
            <input type="submit" class="glass" value="">
            
	          <input id="search-input" type="text" placeholder="Search" name="q" >
          </form>
          
          <ul class="account-nav"></ul>
          <script type="text/template" id="template-account-nav-logged-out">
          <ul class="account-nav" >
              <li class="join-scratch" data-control="registration"><span class=""><span>Join Scratch</span></span></li><li id="login-dropdown" class="sign-in dropdown"><span data-toggle="dropdown" class="dropdown-toggle"><span>Sign in</span></span><div class="popover bottom dropdown-menu"><div class="arrow"></div><div class="popover-content" ><form method="post" id="login" action="#"><label for="username">Username</label><input type="text" id="login_dropdown_username" name="username" maxlength="30" class="wide username" /><label for="password" class="password">Password</label><input type="password" name="password" class="wide password" /><div class="ajax-loader" style="display:none; float: left;"></div><button type="submit">Sign in</button><span class="forgot-password"><a href="/accounts/password_reset/">Need help?</a></span><div class="error"></div></form></div></div></li><li data-control="modal-login" class="sign-in mobile"><span>Sign in</span></li>
          </ul>
          </script>
          <script type="text/template" id="template-account-nav-logged-in">
          <ul class="account-nav logged-in"><li class="messages"><a title="messages - updates and notices" href="/messages" class="messages-icon"><span class="notificationsCount none">0</span></a></li><li class="my-stuff"><a title="my stuff - manage projects and studios" href="/mystuff/" class="mystuff-icon"></a></li><li class="logged-in-user dropdown"><span class="user-name dropdown-toggle" data-toggle="dropdown"><img class="user-icon" src="<%- LOGGED_IN_USER.model.thumbnail_url %>" width="24" height="24"><%- LOGGED_IN_USER.model.username_truncated %><span class="caret"></span></span><div class="dropdown-menu blue" ><ul class="user-nav"><li><a href="<%- LOGGED_IN_USER.model.profile_url %>">Profile</a></li><li><a href="/mystuff/">My Stuff</a></li><% if (LOGGED_IN_USER.model.is_educator){ %><li><a href="/educators/classes/">My Classes</a></li><% } %><% if (LOGGED_IN_USER.model.is_student){ %><li><a href="/classes/<%- LOGGED_IN_USER.model.classroom_id %>/">My Class</a></li><% } %><li><a href="/accounts/settings/">Account settings</a></li><li id="logout" class="logout divider"><form method="post" action="/accounts/logout/"><input type='hidden' name='csrfmiddlewaretoken' value='iw2oPjtonxxnujxKBQl32EAlqqlm1Vav' /><input type="submit" value="Sign out"></form></li></ul></div></li></ul>
          </script>
          <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/account-nav.js"></script>
        </div>
        <iframe class="iframeshim" frameborder="0" scrolling="no"><html><head></head><body></body></html></iframe>
      </div><!-- innerwrap -->
      </div>
        

      <div class="confirm-email banner" data-cue="confirmed_email" style="display:none;">
        <div class="container">
          
          <span><a id="confirm-email-popup" href="#">Confirm your email</a> to enable sharing. <a href="/help/faq/#accounts">Having trouble?</a></span>
          <div class="close">x</div>
        </div>
      </div>

        
        <div class="container" id="content">
        <div id="alert-view"></div>
        






<div class="showcase" id="project" data-project-id="244087899">
  <div class="box">
    <div class="box-head">
      
      <div class="header-text">
          
<div id="title" class="editable read">
  <form>
    <h2><input name="title" value="Nill V.1.X.6.4 (UPDATE)"></textarea></h2>
    <div class="loading-img s32"></div>
  </form>
</div>


        <div id="author">
           by
          
            <a href="/users/webbecol000/"><span id="owner">webbecol000</span></a>
          
          
        </div>
      </div>
      

<div id="wip" class="wip ">
  <input type="checkbox" name="wip" >
  <span>Draft</span>
</div>


      <div class="buttons">
        <div id="editor-stats">
        <div class="stat"><span class="count" id="script-count">&nbsp;</span> scripts</div>
        <div class="stat"><span class="count" id="sprite-count">&nbsp;</span> sprites</div>
        </div>
        <a href="#editor">
          <div class="button" id="see-inside">
              <span class="see-inside icon white">See inside</span>
          </div>
        </a>
      </div>
      
    </div>
    <div class="box-content">
      <div class="stage">
        <div id="player" class="player">
        
        <!-- Start template projects/public.html project-swf -->
        

<!-- Start template project/includes/flash_player_object.html -->
<div id="scratch-loader"></div>
<div id="scratch" style="text-align:center;margin-top:30px;visibility:hidden;position:relative;">
    
    <img src="//cdn2.scratch.mit.edu/get_image/project/244087899_144x108.png" width="144" height="108" class="image" />
    
    <div class="scratch_unsupported" style="display: none;">
        <p style="color:#aaa;font-size:22px;margin-top:14px;line-height:28px;">
            Oh no! We're having trouble displaying this Scratch project.<br/>
            If you are on a mobile phone or tablet, try visiting this project on a computer.<br/>
            If you're on a computer, your Flash player might be disabled, missing, or out of date. Visit <a href="https://get.adobe.com/flashplayer/">this page</a> to update Flash.<br/>
        </p>
        <a href="http://www.adobe.com/go/getflashplayer">
            <img src="//www.adobe.com/images/shared/download_buttons/get_flash_player.gif" alt="Get Adobe Flash player" target="_blank" />
        </a>
    </div>
    <div class="scratch_loading">Loading...</div>
</div>

<script type="text/javascript">
window.SWFready=$.Deferred(); // Deferred makes sure we don't call ASSetEditMode before SWF is ready.
function JSeditorReady() {
    try {
        SWFready.resolve();
        return true;
    } catch (error) {
        console.error(error.message, "\n", error.stack);
        throw error;
    }
}

function handleEmbedStatus(e) {
    $('#scratch-loader').hide();
    if(!e.success) {
        $('#scratch').css('marginTop', '10');
        $('#scratch IMG.proj_thumb').css('width', '179px');
        $('#scratch DIV.scratch_unsupported').show();
        $('#scratch DIV.scratch_loading').hide();
    }else{
        $('#scratch').css('visibility', 'visible');
    }
}

// The flashvars tell flash about the project data (and autostart=true)
var flashvars = {
    autostart: 'false',
    cdnToken: '8f96f1e236e1272ebf8be2ee9598823a',
    urlOverrides: {
        sitePrefix: window.location.protocol + '//' + window.location.host + '/',
        siteCdnPrefix: "http://cdn.scratch.mit.edu/",
        assetPrefix: "http://assets.scratch.mit.edu/",
        assetCdnPrefix: "http://cdn.assets.scratch.mit.edu/",
        projectPrefix: "http://projects.scratch.mit.edu/",
        projectCdnPrefix: "http://cdn.projects.scratch.mit.edu/",
        internalAPI: "internalapi/",
        siteAPI: "site-api/",
        staticFiles: "scratchr2/static/"
    },

    inIE: (navigator.userAgent.indexOf('MSIE') > -1)
};

$.each(flashvars, function(prop, val) {
    if($.isPlainObject(val))
        flashvars[prop] = encodeURIComponent(JSON.stringify(val));
});

$.each(Scratch.INIT_DATA.PROJECT.model, function(i, val) {
    if(val != null)
        flashvars['project_'+i] = encodeURIComponent(val);
});

if(Scratch.INIT_DATA.PROJECT.is_new)
    flashvars.project_isNew = true;

var params = {
    allowscriptaccess: 'always',
    allowfullscreen: 'true',
    wmode: 'direct',
    menu: 'false'
};

// url format flashvars for createSWF call (see
// https://github.com/LLK/scratchr2/blob/f42c289a5fa890d9c5562cc1fa54b0aea3dfa45e/static/js/swfobject.js#L673-L682)
for (var i in flashvars) {
    if (typeof params.flashvars !== 'undefined') {
        params.flashvars += '&' + i + '=' +flashvars[i];
    } else {
        params.flashvars = i + '=' + flashvars[i];
    }
}

var swfFile = (swfobject.hasFlashPlayerVersion('11.7.0') ? 'Scratch.swf' : 'ScratchFor10.2.swf');

var swfAtt = {
    data: "//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/" + swfFile,
    width: "100%",
    height: "100%"
};

swfobject.addDomLoadEvent(function() {
    // check if mobile/tablet browser user bowser
    if(bowser.mobile || (bowser.tablet && typeof bowser.msie === 'undefined')) {
        // if on mobile, show error screen
        handleEmbedStatus({success: false});
    } else {
        // if not on ie, let browser try to handle flash loading
        var swf = swfobject.createSWF(swfAtt, params, "scratch");
        handleEmbedStatus({success: true, ref: swf});
    }
    document.getElementById('scratch').style.visibility = 'visible';
});

//Dynamically add iframe for registration window
$.when(window.SWFready).done(function() {$('<iframe id="registration-iframe" class="iframeshim" style="background:#fff;z-index:-1;" frameborder="0" scrolling="no">').insertBefore('#registration')});

// enables the SWF to log errors
function JSthrowError(e) {
    if (window.onerror) window.onerror(e, 'swf', 0);
    else console.error(e);
}
</script>
<!-- End template project/includes/flash_player_object.html -->

        <!-- End template projects/public.html project-swf -->
        
        </div>
      </div>
      <div id="info" class="info">
        
        <div class="dynamic">
          

<div class="text-block"> 
	<b>Instructions</b>
  <div  id="instructions" class="editable read instructions">
	  <span data-content="prompt">Tell people how to use your project</br>(such as which keys to press).</span>
    <form>
      <textarea name="instructions">Instructions: To play, click on the game mode you want to play on. Answer the question. And use the Arrow Keys to move the bar.
On survival mode, press 1 and 2 to switch between guns.

   WARNING: INSANE MODE IS EXTREMELY HARD BUT EXTREMELY FUN! IF YOU CAN BEAT THE NILL HIGH-SCORE ON EITHER MODE, I WILL FOLLOW YOU AND GIVE YOU A NILL TOUR THROUGH THE COMMENTS. 
________________________________________
YOU MUST HAVE AN ACCOUNT TO DO SO!!!    l  ________________________________________l

Updates Coming SOON! Keep calm and Scratch on!

-Update- V.4.J.9.6.3
More Power-Ups!
More Game Modes!
Survival WAVES
MORE!
_______________________________________________________</textarea>
      <div class="loading-img s48"></div>
    </form>
  </div>
  
</div>


          


<div id="description-wrapper" class="text-block controls">
  <div class="tooltip-target">
    <b>
      Notes and Credits 
    </b>
    <div id="description" class="editable read instructions">
      <span data-content="prompt">
        How did you make the project?
        <br/>
        Did you use ideas, scripts, or artwork from other people? Thank them here.
      </span>
      <form>
        <textarea name="description">Please like and favorite this game so I will be motivated to update it more often! Keep playing Nill and have fun.
WARNING: INSANE MODE IS EXTREMELY HARD BUT EXTREMELY FUN! If you can beat the highscores on ANY mode, I will follow you and tell you what inspired me to make this game.

Credit to TrapMusicHDTV for: 
GhostBusters Theme Song Remix

DubstepGutter for 
Fur Elise Trap Remix</textarea>
        <div class="loading-img s48"></div>
      </form>
    </div>
  </div>
</div>


        </div>
        <div id="fixed" class="fixed">
          
          
          
          
<div id="project-tags" class="has-tags">
  <div class="tag-box editable read">
    <span data-content="prompt">Add project tags.</span>
    <div data-content="tag-list">
      
      
      
      <span class="tag"><a href="/search/projects?q=PongGame">PongGame</a>
      <span data-tag-name="PongGame" data-control="remove">x</span></span>
      
      <span class="tag"><a href="/search/projects?q=money">money</a>
      <span data-tag-name="money" data-control="remove">x</span></span>
      
      <span class="tag"><a href="/search/projects?q=Nill">Nill</a>
      <span data-tag-name="Nill" data-control="remove">x</span></span>
      
      
      
    </div>
    <div data-content="add-tags">
      <form>
        <input type="text" class="tag-input" name="tags">
      </form>
    </div>
  </div>
  <div class="tag-choices">
    <ul class="first-col">
      <li data-control="add-tag" data-tag="animations">Animations</li>
      <li data-control="add-tag" data-tag="art">Art</li>
      <li data-control="add-tag" data-tag="games">Games</li>
    </ul>
    <ul class="second-col">
      <li data-control="add-tag" data-tag="music">Music</li>
      <li data-control="add-tag" data-tag="simulations">Simulations</li>
      <li data-control="add-tag" data-tag="stories">Stories</li>
    </ul>
  </div>
</div>


          <div class="dates">
          
          <span class="date-shared">
            <a href="/info/faq/#remix" class="copyright"></a>
            
Shared: 3 Sep 2018

          </span>
      <span class="date-updated">Modified: 26 Nov 2018</span>
          
          </div>
        </div>
        
      </div>

      <div class="actions clearfix">
        
        <div id="stats" class="active">
            
            <div class="action tooltip bottom first" data-control="toggle-stat" data-stat="favoriters" data-add="false">
            <span class="hovertext"><span class="arrow"></span>Favorite this project</span>
            <span class="favorite icon on" data-content="fav-count">
              11
            </span>
            </div>
            

            
            <div class="action tooltip bottom" id="love-this" data-control="toggle-stat" data-stat="lovers" data-add="false">
            <span class="hovertext"><span class="arrow"></span>Love this project</span>
            <span class="love icon on" data-content="love-count">
              11</span>
          </div>
            

          


<div class="action tooltip bottom" id="add-to" data-control="add-to-open" data-username="webbecol000">
  <span class="hovertext"><span class="arrow"></span>Add project to studios</span>
  <span class="dropdown-toggle text black" data-control="open-add-to">Studios<span class="caret"></span></span>
</div>
 
<div class="action tooltip bottom" id="share-to">
  <span class="hovertext"><span class="arrow"></span> Embed project on other websites</span>
  <span class="dropdown-toggle text black" data-control="open-share-to">Embed<span class="caret"></span></span>
</div>




<div class="action tooltip bottom" style="display: none;" id="cloud-log">
    <span class="hovertext"><span class="arrow"></span>View Cloud Data activity for this project.</span>
    <span><a class="text black" href="/cloudmonitor/244087899/">Cloud Data</a></span>
</div>





           
          <div class="stats">
            <div id="total-views" class="first action tooltip bottom grey">
              <span class="hovertext"><span class="arrow"></span>Total views</span>
              <span class="icon views">177</span>
            </div>
            <div class="action last tooltip bottom grey">
              <span class="hovertext"><span class="arrow"></span>View the remix tree</span>
              <a href="/projects/244087899/remixtree/" class="remix-tree" onclick="on_click_remixtree(244087899, window.location.pathname, '/projects/244087899/remixtree/', 244087899);">
                <span class="icon remix-tree">&nbsp;4</span>
              </a>
            </div>
          </div>
        </div>
        
      </div>
    </div>
  </div>
</div>


<div class="player-box-footer-module" id="player-box-footer">
</div>

<div class="player-box-footer-module" id="bug-report-form">
</div>

<div id="add-to-menu"  class="player-box-footer-module hide page">
  <div class="section first">
      <h4>Add this project to a studio you curate (or remove it from a studio)</h4>
      Just click on the button for any of the studios from the list below
  <div class="studio-list">
    <ul>
      <div class="next-page" data-url="/site-api/galleries/curated_by_or_with_project/244087899/1/"></div>
    </ul>
  </div>
</div>
  <div class="close">x</div>
</div>

<div id="download-menu" class="player-box-footer-module hide page">
  <div class="section first" style="height: 100px;">
    <h4>Download this project file</h4>
    
    <div id="old-scratch-project2" class="hide">
    <div class="button"><span class="icon download">&nbsp;</span>
      <span>Download code </span>
    </div>
    <span class="alert alert-warning">This project can be opened in Scratch 1.4 or 2.0</span>
    </div>

    <div id="new-scratch-project">
      <div class="button"><span class="icon download">&nbsp;</span>
        <span>Download code </span> 
      </div> 
      <span class="alert alert-warning">This project was edited in 2.0 so you need 2.0 to open it</span>
      <br />(dialog appears on the stage)
    </div>

  </div>
  <div class="close" data-control="close">x</div>
</div>

<div id="share-to-menu"  class="player-box-footer-module hide page">
  <div class="section embed first">
      <h4>Embed</h4> 
    <form class="form-horizontal">
    <textarea id="embed-textarea" width="98%">
      <iframe allowtransparency="true" width="485" height="402" src="//scratch.mit.edu/projects/embed/244087899/?autostart=false" frameborder="0" allowfullscreen></iframe>
    </textarea>
    <span class="small-text">Copy and paste the embed code above.</span>
    </form>
  </div>
  <div class="section social">
      <h4>Share</h4>
    <a class="social-icon facebook" href="http://www.facebook.com/sharer.php?u=https://scratch.mit.edu/projects/244087899/" target="_blank"></a>
    <a class="social-icon twitter" href="http://twitter.com/intent/tweet?original_referer=https://scratch.mit.edu/projects/244087899/&text=https://scratch.mit.edu/projects/244087899/ made w/ Scratch" target="_blank"></a>
    <a class="social-icon google-class" href="https://classroom.google.com/share?url=https://scratch.mit.edu/projects/244087899/" target="_blank"></a>
    <textarea readonly id="link-textarea" width="90%"></textarea>
  </div>
  <div class="section download hide" id="old-scratch-project">
    <h4>Download 1.4 Project</h4>
    <a class="grey button" href=""><span class="text">Download code</span></a>
 </div>

<div class="close">x</div>
</div>





<div class="cols related">
  <div class="col-11">
    <div class="box">
      <div class="box-head">
        <h4><span class="icon-sm comment black"></span>Comments <span id="comment-count"></span></h4>
      </div>
      <div class="box-content">
        
            



<div id="comments">
  
  
    <div id="comments-enabled-box" class="action-bar white scroll">
        <input type="checkbox" name="comments-enabled" id="comments-enabled" />
        <label for="comments-enabled"> Turn off commenting</label>
    </div>
  
  
  <div id="comment-form">
    
        <img class="avatar" src="//cdn2.scratch.mit.edu/get_image/user/26049657_60x60.png" width="45" height="45"/>
    
    
        <form id="main-post-form" class="comments-on" >
            <div class="control-group tooltip right">
                
                <textarea name="content" placeholder="Leave a comment" ></textarea>
                
                <span id="comment-alert" class="hovertext error" data-control="error" data-content="comment-error"><span class="arrow"></span><span class="text"></span></span>
                <span class="small-text">You have <span id="chars-left">500</span> characters left.</span>
            </div>
            <div class="control-group">
                <div class="button small" data-control="post" data-parent-thread="" data-commentee-id=""><a href="#null">Post</a></div>
            <div class="button small grey" data-control="cancel"><a href="#null">Cancel</a></div>
                <span class="notification"></span>
            </div>
        </form>
        
    
    <div class="clearfix"></div>
  </div>
  <div>
    <ul class="comments" data-content="comments">
      <li id="comments-loading" class="top-level-reply"><span>Comments loading...</span></li>
    </ul>
  </div>
</div>

        
      </div>
    </div>
  </div>

  <div class="col-5">
    
    
    
    <div class="box">
      <div class="box-head">
        <h4><span class="icon-sm remix black"></span>Remixes (3)</h4>
    <a href="remixes" class="right" onclick="on_click_remixes(window.location.pathname, '/projects/244087899/remixtree/', 244087899);">View all</a>
      </div>
      <div class="box-content grey">
        <ul class="media-col">
          
          <li>
          <div class="project thumb">
          <a href="/projects/245412417/" class="image" onclick="on_click_remixbar(window.location.pathname, '/projects/245412417/', 244087899, 245412417);">
            <img src="//cdn2.scratch.mit.edu/get_image/project/245412417_144x108.png" class="image">
          </a>
          <span class="title"><a href="/projects/245412417/" onclick="on_click_remixbar(window.location.pathname, '/projects/245412417/', 244087899, 245412417);">Nill- - V.1.8.25.F remix</a></span>
          <span class="owner">by COLI0</span>
          </li>
          
          <li>
          <div class="project thumb">
          <a href="/projects/245413491/" class="image" onclick="on_click_remixbar(window.location.pathname, '/projects/245413491/', 244087899, 245413491);">
            <img src="//cdn2.scratch.mit.edu/get_image/project/245413491_144x108.png" class="image">
          </a>
          <span class="title"><a href="/projects/245413491/" onclick="on_click_remixbar(window.location.pathname, '/projects/245413491/', 244087899, 245413491);">Nill- - V.1.8.25.F remix</a></span>
          <span class="owner">by long_ken003</span>
          </li>
          
          <li>
          <div class="project thumb">
          <a href="/projects/247506364/" class="image" onclick="on_click_remixbar(window.location.pathname, '/projects/247506364/', 244087899, 247506364);">
            <img src="//cdn2.scratch.mit.edu/get_image/project/247506364_144x108.png" class="image">
          </a>
          <span class="title"><a href="/projects/247506364/" onclick="on_click_remixbar(window.location.pathname, '/projects/247506364/', 244087899, 247506364);">Nill- - V.1.8.25.F  remix</a></span>
          <span class="owner">by long_ken003</span>
          </li>
          
        </ul>
      </div>
    </div>
    
    
    


    
    
    <div class="box galleries" id="galleries">
      <div class="box-head">
        <h4><span class="icon-sm studio black"></span>Studios  (5)</h4>
    <a href="studios" class="right">View all</a>
      </div>
      <div class="box-content grey">
        <ul class="media-col">
          
          



<!-- templates/carousel/gallery-thumb.html -->
<li class="gallery thumb item">
  <a href="/studios/5455254/" class="image">
    <span class="image">
      <img class="lazy" data-original="//cdn2.scratch.mit.edu/get_image/gallery/5455254_170x100.png" width="170" height="100" />
    </span>
    <span class="stats">
      <span class="icon-sm studio white"></span>
    </span>
  </a>
  <span class="title">
    <a href="/studios/5455254/">Add whatever you want Studio
    </a>
  </span>
</li>
<!-- end templates/carousel/gallery-thumb.html -->


          
          



<!-- templates/carousel/gallery-thumb.html -->
<li class="gallery thumb item">
  <a href="/studios/5340619/" class="image">
    <span class="image">
      <img class="lazy" data-original="//cdn2.scratch.mit.edu/get_image/gallery/5340619_170x100.png" width="170" height="100" />
    </span>
    <span class="stats">
      <span class="icon-sm studio white"></span>
    </span>
  </a>
  <span class="title">
    <a href="/studios/5340619/">NILL STUDIOS
    </a>
  </span>
</li>
<!-- end templates/carousel/gallery-thumb.html -->


          
          



<!-- templates/carousel/gallery-thumb.html -->
<li class="gallery thumb item">
  <a href="/studios/5242825/" class="image">
    <span class="image">
      <img class="lazy" data-original="//cdn2.scratch.mit.edu/get_image/gallery/5242825_170x100.png" width="170" height="100" />
    </span>
    <span class="stats">
      <span class="icon-sm studio white"></span>
    </span>
  </a>
  <span class="title">
    <a href="/studios/5242825/">Advertise your projects!
    </a>
  </span>
</li>
<!-- end templates/carousel/gallery-thumb.html -->


          
          



<!-- templates/carousel/gallery-thumb.html -->
<li class="gallery thumb item">
  <a href="/studios/4924369/" class="image">
    <span class="image">
      <img class="lazy" data-original="//cdn2.scratch.mit.edu/get_image/project/245411584_170x100.png" width="170" height="100" />
    </span>
    <span class="stats">
      <span class="icon-sm studio white"></span>
    </span>
  </a>
  <span class="title">
    <a href="/studios/4924369/">WEBBECOL000 STUDIOS!
    </a>
  </span>
</li>
<!-- end templates/carousel/gallery-thumb.html -->


          
          



<!-- templates/carousel/gallery-thumb.html -->
<li class="gallery thumb item">
  <a href="/studios/2098118/" class="image">
    <span class="image">
      <img class="lazy" data-original="//cdn2.scratch.mit.edu/get_image/gallery/2098118_170x100.png" width="170" height="100" />
    </span>
    <span class="stats">
      <span class="icon-sm studio white"></span>
    </span>
  </a>
  <span class="title">
    <a href="/studios/2098118/">Agents of S.H.I.E.L.D. Studio (Level 7 only)
    </a>
  </span>
</li>
<!-- end templates/carousel/gallery-thumb.html -->


          
        </ul>
      </div>
    </div>
    
    
  </div>

</div>


<div class="humane"><iframe class="iframeshim" frameborder="0" scrolling="no"><html><head></head><body></body></html></iframe></div>
<div id="tip-bar"></div>

        </div>


        


<div id="explore-bar">
	<div id="explore-header" class="closed">
		<div id="explore-header-closed">
			<div class="header-text"><div id="open">&nbsp;&nbsp;</div><!-- <span id="new" class="foo">New!</span> -->More projects by webbecol000</div>
		</div>
		<div id="explore-header-open" class="hidden">	
			<div class="header-text">
				<span id="creator-text" class="explore-by-text hidden" ></span>
				<span id="remixes-text" class="explore-by-text hidden"></span>
				<!-- <span id="location-text" class="explore-by-text hidden"></span> -->
			</div>
			<div id="explore-buttons">
				<span id="creator" class="explore_button button small grey"><span>Creator</span></span></a>
			<span  id="remixes" class="explore_button button small grey"><span>Remixes</span></span></a>
				<!--<span id="loves" class="explore_button button small grey"><span>Mutual Loves</span></span></a>-->
				<!--<span id="location" class="explore_button button small grey"><span>Location</span></span></a> -->
			</div>
			<div id="close">&nbsp&nbsp</div>
		</div>
	</div>
	<div id="related-projects" class="carousel">
		<div id="inner" class="carousel-inner">
			<ul class="list-container hidden " id="creator-list"><div class="ajax-loader"></div></ul>
			<ul class="list-container hidden " id="remixes-list"><div class="ajax-loader"></div></ul>
			<!--<ul class="list-container hidden " id="loves-list"><div class="ajax-loader"></div></ul>-->
			<!--<ul class="list-container hidden " id="location-list"><div class="ajax-loader"></div></ul>-->
		</div>
		<a class="carousel-control left arrow-left off" href="#related-projects" data-slide="prev">&lsaquo;</a>
	  	<a class="carousel-control right arrow-right on" href="#related-projects" data-slide="next">&rsaquo;</a>
	</div>
</div>


        
    </div>
    <div id="footer">
      <div class="container">
        <style>
          #footer ul.footer-col li {
            list-style-type:none;
            display: inline-block;
            width: 184px;
            text-align: left;
            vertical-align: top;
          }

          #footer ul.footer-col li h4 {
            font-weight: bold;
            font-size: 14px;
            color: #666;
          }

        </style>
        <ul class="clearfix footer-col">
          <li>
            <h4>About</h4>
            <ul>
              <li><a href="/about/">About Scratch</a></li>
              <li><a href="/parents/">For Parents</a></li>
              <li><a href="/educators/">For Educators</a></li>
              <li><a href="/developers">For Developers</a></li>
              <li><a href="/info/credits/">Credits</a></li>
              <li><a href="/jobs/">Jobs</a></li>
              <li><a href="https://www.scratchfoundation.org/media-kit/">Press</a></li>
            </ul>
          </li>
          <li>
            <h4>Community</h4>
            <ul>
              <li><a href = "/community_guidelines/">Community Guidelines</a></li>
              <li><a href = "/discuss/">Discussion Forums</a></li>
              <li><a href = "http://wiki.scratch.mit.edu/">Scratch Wiki</a></li>
              <li><a href = "/statistics/">Statistics</a></li>
            </ul>
          </li>
          <li>
            <h4>Support</h4>
            <ul>
              <li><a href = "/tips">Tips</a></li>
              <li><a href = "/info/faq/">FAQ</a></li>
              <li><a href = "/download">Offline Editor</a></li>
              <li><a href = "/contact-us/">Contact Us</a></li>
              <li><a href="/store">Scratch Store</a></li>
              <li><a href = "https://secure.donationpay.org/scratchfoundation/">Donate</a></li>
            </ul>
          </li>
          <li>
            <h4>Legal</h4>
            <ul>
              <li><a href="/terms_of_use/">Terms of Use</a></li>
              <li><a href="/privacy_policy/">Privacy Policy</a></li>
              <li><a href = "/DMCA/">DMCA</a></li>
            </ul>
          </li>
          <li>
            <h4>Scratch Family</h4>
            <ul>
              <li><a href="http://scratched.gse.harvard.edu/">ScratchEd</a></li>
              <li><a href="http://www.scratchjr.org/">ScratchJr</a></li>
              <li><a href="http://day.scratch.mit.edu/">Scratch Day</a></li>
              <li><a href="/conference/">Scratch Conference</a></li>
              <li><a href="http://www.scratchfoundation.org/">Scratch Foundation</a></li>
            </ul>
          </li>
        </ul>
        <ul class="clearfix" id="footer-menu" >
          <li>
            <form id="lang-dropdown" method="post" action="/i18n/setlang/">
              <select id="language-selection" name="language">
              
                <option value="ab" >Аҧсшәа</option>
              
                <option value="ar" >العربية</option>
              
                <option value="an" >Aragonés</option>
              
                <option value="ast" >Asturianu</option>
              
                <option value="id" >Bahasa Indonesia</option>
              
                <option value="ms" >Bahasa Melayu</option>
              
                <option value="be" >Беларуская</option>
              
                <option value="bg" >Български</option>
              
                <option value="ca" >Català</option>
              
                <option value="cs" >Česky</option>
              
                <option value="cy" >Cymraeg</option>
              
                <option value="da" >Dansk</option>
              
                <option value="de" >Deutsch</option>
              
                <option value="yum" >Edible Scratch</option>
              
                <option value="et" >Eesti</option>
              
                <option value="el" >Ελληνικά</option>
              
                <option value="en" selected >English</option>
              
                <option value="eo" >Esperanto</option>
              
                <option value="es" >Español</option>
              
                <option value="eu" >Euskara</option>
              
                <option value="fa" >فارسی</option>
              
                <option value="fr" >Français</option>
              
                <option value="fur" >Furlan</option>
              
                <option value="ga" >Gaeilge</option>
              
                <option value="gd" >Gàidhlig</option>
              
                <option value="gl" >Galego</option>
              
                <option value="ko" >한국어</option>
              
                <option value="hy" >Հայերեն</option>
              
                <option value="he" >עִבְרִית</option>
              
                <option value="hi" >हिन्दी</option>
              
                <option value="hr" >Hrvatski</option>
              
                <option value="zu" >isiZulu</option>
              
                <option value="is" >Íslenska</option>
              
                <option value="it" >Italiano</option>
              
                <option value="kn" >ಭಾಷೆ-ಹೆಸರು</option>
              
                <option value="kk" >Қазақша</option>
              
                <option value="rw" >Kinyarwanda</option>
              
                <option value="ht" >Kreyòl</option>
              
                <option value="ku" >Kurdî</option>
              
                <option value="la" >Latina</option>
              
                <option value="lv" >Latviešu</option>
              
                <option value="lt" >Lietuvių</option>
              
                <option value="mk" >Македонски</option>
              
                <option value="hu" >Magyar</option>
              
                <option value="ml" >മലയാളം</option>
              
                <option value="mt" >Malti</option>
              
                <option value="mr" >मराठी</option>
              
                <option value="cat" >Meow</option>
              
                <option value="mn" >Монгол хэл</option>
              
                <option value="my" >မြန်မာဘာသာ</option>
              
                <option value="nl" >Nederlands</option>
              
                <option value="ja" >日本語</option>
              
                <option value="ja-hr" >にほんご</option>
              
                <option value="nb" >Norsk Bokmål</option>
              
                <option value="nn" >Norsk Nynorsk</option>
              
                <option value="uz" >Oʻzbekcha</option>
              
                <option value="th" >ไทย</option>
              
                <option value="pl" >Polski</option>
              
                <option value="pt" >Português</option>
              
                <option value="pt-br" >Português Brasileiro</option>
              
                <option value="ro" >Română</option>
              
                <option value="ru" >Русский</option>
              
                <option value="sc" >Sardu</option>
              
                <option value="sq" >Shqip</option>
              
                <option value="sk" >Slovenčina</option>
              
                <option value="sl" >Slovenščina</option>
              
                <option value="sr" >Српски</option>
              
                <option value="fi" >Suomi</option>
              
                <option value="sv" >Svenska</option>
              
                <option value="te" >తెలుగు</option>
              
                <option value="nai" >Tepehuan</option>
              
                <option value="vi" >Tiếng Việt</option>
              
                <option value="tr" >Türkçe</option>
              
                <option value="uk" >Українська</option>
              
                <option value="zh-cn" >简体中文</option>
              
                <option value="zh-tw" >正體中文</option>
              
              </select>
            </form>
          </li>
        </ul>
        <p >Scratch is a project of the Lifelong Kindergarten Group at the MIT Media Lab</p>
      </div>
    </div>
    

    
<!-- templates/modal-login.html block -->
	    <div class="modal hide fade in" id="login-dialog" style="width: 450px">
        <form method="post" action="/login/">
          <fieldset>
            <div class="modal-header">
              <a href="#" data-dismiss="modal" class="close">x
              </a>
	      <h3>Sign in</h3>
            </div>
            <div class="modal-body">
            
              <div class="control-group">
		      <label class="control-label" for="username">Username
                </label>
                <div class="controls">
                  <input class="username" type="text" name="username" maxlength="30" />
                </div>
              </div>
              <div class="control-group">
		            <label class="control-label" for="password">Password
                </label>
                <div class="controls">
                  <input type="password" name="password" class="password" />
                </div>
              </div>
              
              <div class="control-group" id="recaptcha_field">
                <script src="https://www.google.com/recaptcha/api.js?render=explicit" async defer></script>
                <div class="g-recaptcha" id="recaptcha-container" data-sitekey="6LeRbUwUAAAAAFYhKgk3G9OKWqE_OJ7Z-7VTUCbl"></div>
              </div>
              
            </div>
            <div class="modal-footer">
              <span class="error">
              </span>
              <div class="buttons-right">
                <button class="button primary" type="submit">Sign in</button> 
                
		<a data-control="registration">Or Join Scratch</a>
                
              </div>
            </div>
           
          </fieldset>
        </form>
        <iframe class="iframeshim" frameborder="0" scrolling="no"><html><head></head><body></body></html></iframe>
      </div>
<!-- end templates/modal-login.html -->

    
        <div id="registration" class="registration modal hide fade" data-backdrop="static">
          <iframe class="iframeshim" frameborder="0" scrolling="no"><html><head></head><body></body></html></iframe>
        </div>
    

    
    

    
<div id="remix-modal" class="modal hide fade in">

    <div class="modal-header">
        <span type="button" class="close" data-dismiss="modal">×</span>
        <h3>Ready to Remix!</h3>
    </div>

    <div class="modal-body">
      <div id="remix-dialog">
      <p>Add your ideas! You could try:</p>
      <ul>
        <li>drawing a new costume</li>
        <li>changing the scripts</li>
        <li>creating a new sprite</li>
      </ul>
      </div>
    </div>

    <div class="modal-footer">
      <div class="buttons-right">
        <button class="button primary" type="submit">OK, Got it.</button> 
      </div>
    </div>
    <iframe class="iframeshim" frameborder="0" scrolling="no"><html><head></head><body></body></html></iframe>

</div> <!-- #remix-modal -->


    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/jquery-ui.min.js"></script>

    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/main.js" charset="utf-8"></script>

  
  <script type="text/javascript">
    // load gaq script
    (function() {
      var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
      ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
      var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
    })();
  </script>

    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/base.js" charset="utf-8"></script>
    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/lazyload.js" charset="utf-8"></script>
    
<script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/lib/jquery-visibility.js"></script>
<script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/carousel.js"></script>
<script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/explore-bar.js"></script>

<script>
  backbone_data = {
    project:  {
      
      pk: 244087899,
      fields: {
        creator: 'webbecol000',
        title: 'Nill V.1.X.6.4 (UPDATE)',
      },
      
    },
  };

  data = {
   
    user: {
      username: 'webbecol000',
      id: 26049657
    },
    
    
    project: {
      id: 244087899,
      parentId: null,
      creator: 'webbecol000',
      title: 'Nill V.1.X.6.4 (UPDATE)',
      isPrivate: false,
    }
    
  };
</script>


<script>
  var projectUrl = '/projects/244087899/';
</script>



<script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/save_actions.js"></script>

<script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/tag_regex.js"></script>
<script>
  $('#link-textarea').val(window.location.href);
</script>

    

    
<script type="text/template" id="template-alert-project-changed">
    <p>Project was updated  successfully.</p>
</script>

<script type="text/template" id="template-tip-bar">
  <div id="tip-bar-inner" class="<%- isOpen ? 'tipsopen' : 'tipsclosed' %>">
    <div class="tip-header">
      <span class="tip-icon toggle-control">?</span>
      <h5>
        <span class="close-circle-dark">x</span>
        <span class="tip-ctrl tip-home active">All Tips</span>
      </h5>
    </div>
    <div class="tip-content">
        <div class="tip-arrow-container">
            <span class="tip-arrow opentip toggle-control">&#9664;</span>
        </div>
        <iframe id="tip-content-container" src="" frameBorder="0" <% if (bowser.name !== 'Internet Explorer') { %>webkitallowfullscreen mozallowfullscreen allowfullscreen <% } %>></iframe>
    </div>
  </div>
  <iframe class="iframeshim" frameborder="0" scrolling="no"><html><head></head><body></body></html></iframe>
</script>





<script type="text/template" id="template-collection-count">
  <%- count %>
</script>

<script type="text/template" id="template-comment-actions">
<% if (can_delete) { %>
  <% if (is_staff && comment_user == current_user) { %>
    <span data-control="delete" class="actions report">Delete</span>
  <% } else if (type != "gallery" || comment_user == current_user) { %>
    <span data-control="delete" class="actions report">Delete</span>
  <% } %>
<% } %>
<% if (current_user != comment_user) { %>
  <span data-control="report" class="actions report">
  <% if (student_of_educator) { %>
    Delete
  <% } else { %>
    Report
  <% } %></span>
<% } %>
</script>

<script type="text/template" id="template-modal-login">
<div class="modal hide fade in" id="login-dialog" style="width: 450px">
  <form method="post" action="/login/">
    <fieldset>
      <div class="modal-header">
        <a href="#" data-dismiss="modal" class="close">x
        </a>
        <h3>Login</h3>
      </div>
      <div class="modal-body">
        <div class="control-group">
        <label class="control-label" for="username">Username
          </label>
          <div class="controls">
            <input id="username" type="text" name="username" maxlength="30" />
          </div>
        </div>
        <div class="control-group">
        <label class="control-label" for="password">Password
          </label>
          <div class="controls">
            <input type="password" name="password" id="password" />
          </div>
        </div>
      </div>
      <div class="modal-footer">
        <span class="error">
        </span>
        <span class="button primary" id="sign-in" data-control="site-login">
        <span>{% trans "Sign in" $}
          </span>
        </span>
      </div>
    </fieldset>
  </form>
</div>
</script>

<script type="text/template" id="template-comment-reply">
  <form>
    <div class="control-group tooltip right">
      <textarea name="content"></textarea>
      
      <span class="hovertext error" data-control="error" data-content="comment-error"><span class="arrow"></span><span class="text"></span></span>
      <span class="small-text">You have <span id="chars-left-<%- comment_id %>">500</span> characters left.</span>
    </div>
    <div class="control-group">
        <div class="button small" data-parent-thread="<%- thread_id %>" data-commentee-id="<%- commentee_id %>" data-control="post"><a href="#null">Post</a></div>
        <div class="button small grey" data-control="cancel"><a href="#null">Cancel</a></div>
      <span class="notification"></span>
    </div>
  </form>
</script>

<script type="text/template" id="template-deletion-canceled">
<div class="deletion-canceled">
  <div class="form">
    <p>
    Your account was scheduled for deletion but you logged in. Your account has been reactivated. If you didn’t request for your account to be deleted, you should <a href="/accounts/password_change/">change your password</a> to make sure your account is secure. 
    </p>
  </div>
</div>
</script>

<script type="text/template" id="template-unsupported-browser">
  <div class="unsupported-browser banner" data-cue="unsupported_browser">
    <div class="container">
      <span>Scratch works best on newer browsers. We suggest you upgrade to <a href="/info/faq/#requirements">a supported browser</a>, <a href="/scratch2download/">download the offline editor</a>, <a href="https://en.scratch-wiki.info/wiki/List_of_Bug_Workarounds">or read about common workarounds</a>.</span>
      <div class="close">x</div>
    </div>
  </div>
</script>

<script type="text/template" id="template-unsupported-msie">
  <div class="unsupported-browser banner" data-cue="unsupported_browser">
    <div class="container">
      <span>Scratch will stop supporting Internet Explorer 8 on April 30, 2015. We suggest you upgrade to <a href="/info/faq/#requirements">a supported browser</a>, <a href="/scratch2download/">download the offline editor</a>, or <a href="https://en.scratch-wiki.info/wiki/List_of_Bug_Workarounds">read about common workarounds</a>.</span>
      <div class="close">x</div>
    </div>
  </div>
</script>


<script type="text/template" id="template-project-title">
  <div id="title" class="editable read inline">
    <form>
      <h2><input value="Nill V.1.X.6.4 (UPDATE)" name="credits"></h2>
    </form>
  </div>
</script>
<script type="text/template" id="template-report">
  
  <div class="section first report">
      <div class="form">
        
          <h4>Report as inappropriate</h4>
          <div>
              
              
              From the dropdown below, please select the reason why you feel this project is disrespectful or inappropriate, or otherwise breaks the <a href="/community_guidelines/" target="_blank">Scratch Community Guidelines.</a>
              
              <br>
              If your report is about disrespectful or inappropriate use of Cloud Data, you can view the <a href="/cloudmonitor/244087899/">list of all Cloud Data operations</a> for this project.
              
          </div>
          <form class="form-horizontal">
              <select name="report_category" id="report-category-selector">
                  <option value="">Select a reason</option>
                  <option value="0">Exact Copy of Project</option>
                  <option value="1">Uses Image/Music Without Credit</option>
                  <option value="2">Too Violent or Scary</option>
                  <option value="3">Inappropriate Language</option>
                  <option value="4">Inappropriate Music</option>
                  <option value="8">Inappropriate Images</option>
                  <option value="5">Sharing Personal Contact Information</option>
                  <option value="6">Other</option>
              </select>
              <textarea id="report-explanation" placeholder="Select a reason why above"></textarea>
              <button type="button" data-control="submit">Send</button>
          </form>
        </div>
        <div class="message">
          We have received your report. The Scratch Team will review the project based on the Scratch community guidelines.
        </div>
      
  </div>
<div data-control="close" class="close">x</div>

</script>

<script type="text/template" id="template-censor-reshare-dialog">
<p>
  Are you sure your project is OK for Scratch? Read the <a href="/community_guidelines" target="_blank">Community Guidelines</a> to be sure.
</p>
</script>









    

    <!-- load javascript translation catalog, and javascript fuzzy date library -->
    <script type="text/javascript" src="/jsi18n/"></script>
    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/lib/jquery.timeago.settings.js"></script>

    
    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/apps/registration/main.js"></script>
    

    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__//js/apps/global.js"></script>
    <script>
      Scratch.NotificationPollTime = 300000;
    </script>

    
    <script type="text/javascript" src="//cdn.scratch.mit.edu/scratchr2/static/__8f96f1e236e1272ebf8be2ee9598823a__/js/project_base.js" charset="utf-8"></script>


    
    <script>
    $(document).on("accountnavready", function(e){
        $('#topnav .messages').notificationsAlert();
    });
    </script>
    
  </body>
  <!-- Site Version: 2.2018.11.16_2018_11_16_06_46 -->
</html>

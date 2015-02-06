<h3>CopyMe.js</h3>
CopyMe.js is a JavaScript library that enables a web page to easily monitor what text is being copied from it. It can be used to receive copy/cut events (whether done by mouse of keyboard shortcuts). Such information can prove useful - it could help detect potential plagiarism, help determine what portions of a page's content is most useful to viewers, or simply provide metrics for how users are engaging with a page.

<h3>Demo</h3>
A demo of CopyMe.js can be seen here: www.jasonzissman.com/copyme/index.html.

<h3>Where do I get CopyMe.js?</h3>
You can download the most recent copy at <a href="https://github.com/jasonzissman/CopyMe.js">the CopyMe Github project</a>.

<h3>Supported Browsers</h3>
Currently (Feb 5, 2015) only Firefox and Chrome are tested and working.

<h3>How do I use CopyMe.js?</h3>
Simply include the following lines of code in your page's head element: <br/>
<pre><code>&lt;script src="CopyMe.js"&gt;&lt;/script"&gt;
&lt;script type="text/javascript""&gt;
  window.onload = function(){
    CopyMe.setCopyCallback(function(copiedText){
      // Do something here when text is copied
    });
    CopyMe.setCutCallback(function(cutText){
      // Do something here when text is cut
    });
  }
&lt;/script"&gt;</code></pre>

That's all there is to it!  In addition to defining handlers that handle the copy events, CopyMe lets one review all the text that has been copied or cut by the user.<br/>
<pre><code>CopyMe.getAllCopiedOrCutText();
CopyMe.getLastCopiedOrCutText();</code></pre>

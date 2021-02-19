## PathX

## Notes

https://codepen.io/cdalson/pen/GRjXjZa
https://codepen.io/cdalson/pen/WNGgRyV
https://github.com/quilljs/parchment/
https://quilljs.com/docs/delta/
https://quilljs.com/docs/api/#editor-change
https://github.com/quilljs/delta
https://quilljs.com/guides/building-a-custom-module/
https://codepen.io/dnus/pen/OojaeN
https://codepen.io/cdalson/pen/Exgpgve
https://codepen.io/quill/pen/qNJrYB

> Increase number of file watcher temporarily:
  - sudo sysctl fs.inotify.max_user_watches=524288

## PathX Wordpress Section

> https://getdiyai.com/test-fullscreen-iframe/

## Diagram

{% swimlanes %}
  
Title: Code Block by Order of Execution

WebPage -> WebPageEnd: Message

note:

**Header** Scripts loaded in the head

  **Custom CSS & JS Blocks** Wordpress plugin utilized:::

  **JQuery 3.5.1** depedency for the following libraries:

    - `Isotope`
    - `TinyMCE v5`



**Bootstrap@5 JS CSS** 
  - dependency for page interface

**Flickity @ 2 CSS - Flickity 2 JS** 
  - dependency for `flickity` implementation

**Isotope@3 JS Isotope@3 CSS** 
  - dependency for `Isotope` implementation

**Plotly d3.js** 
  - dependency for `plotly` implementation
  - dependency for `d3.js` implementation

**Compromise JS** 
  - dependency for `compromise` implementation

**Footer** Code loaded in the footer:::

**Entire implementation - JS - Combined file** all js code blocks
  - dependency for all js that can execute w/o a delay
  
  ::: all code blocks listed here:

**Post Form Interface - CSS Implementation - Combined File** all css for post form interface
  - dependency for `isotope` and post form implementation


**Copy the url** to save or share the diagram, _note that the url changes whenever you update the diagram_.

Or `Sign in {fa-sign-in-alt}` to create an account and collect all of your diagrams.


WebPageEnd -> WebPageEnd: To self

WebPageEnd -->> JIT_Scripts: _Notification_

WebPageEnd -> WebPage: `ok`

note: See **[full syntax overview](/gallery/full-syntax)** for more details

{% endswimlanes %}

### Medium Editor

```
tinymce.init({
  selector: "#editor",
  plugins: "autoresize quickbars image media table hr paste",
  skin: "snow",
  icons: "thin",
  menubar: false,
  toolbar: false,
  content_style: "@import url('https://fonts.googleapis.com/css2?family=Tinos&display=swap'); body { font-family: 'Tinos', serif; font-size: 16pt; color: #292929; }",
  placeholder: "Tell your story...",
  quickbars_selection_toolbar: "bold italic link | h1 h2 | blockquote",
  quickbars_insert_toolbar: "image media table hr"
});
```

### Add script after page loads

```
var script = document.createElement('script'); 
          
        script.src =  
"https://cdn.tiny.cloud/1/qagffr3pkuv17a8on1afax661irst1hbr4e6tbv888sz91jc/tinymce/5/tinymce.min.js"; 
          
        document.head.appendChild(script) 
```

### TinyMCE Inline Editing Example

```
tinymce.init({
  selector: 'h2.editable',
  inline: true,
  toolbar: 'undo redo',
  menubar: false
});

tinymce.init({
  selector: 'div.editable',
  inline: true,
  plugins: [
    'advlist autolink lists link image charmap print preview anchor',
    'searchreplace visualblocks code fullscreen',
    'insertdatetime media table contextmenu paste'
  ],
  toolbar: 'insertfile undo redo | styleselect | bold italic | alignleft aligncenter alignright alignjustify | bullist numlist outdent indent | link image',
  content_css: [
    '//fonts.googleapis.com/css?family=Lato:300,300i,400,400i',
    '//www.tinymce.com/css/codepen.min.css']
});
```

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="cdalson" data-slug-hash="ZEpjdPB" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="TinyMCE Inline Mode">
  <span>See the Pen <a href="https://codepen.io/cdalson/pen/ZEpjdPB">
  TinyMCE Inline Mode</a> by Clifford Dalson III (<a href="https://codepen.io/cdalson">@cdalson</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### TinyMCE code snippets

```
tinyMCE

tinyMCE.activeEditor.contentDocument.body.innerText 

tinyMCE.activeEditor.on('keyup', function(e){ console.log("Test")})

tinymce.init({
    selector: '#mytextarea'
  });

tinymce.get("mytextarea").getContent();


tinymce.get("mytextarea").on('keyup', function(e){ console.log("Test")})

tinymce.get("mytextarea").contentDocument.body.innerText

textarea_1_11076

https://codepen.io/desandro/pen/btFfG

```
Codepen Example

[](codepen://Lingyucoder/AsFJh?height=800&theme=0)

<p class="codepen" data-height="565" data-theme-id="light" data-default-tab="js,result" data-user="borntofrappe" data-slug-hash="yRmOrK" data-preview="true" data-editable="true" style="height: 565px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="D3 Hierarchy">
  <span>See the Pen <a href="https://codepen.io/borntofrappe/pen/yRmOrK">
  D3 Hierarchy</a> by Gabriele Corti (<a href="https://codepen.io/borntofrappe">@borntofrappe</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Javascript script fetch

https://levelup.gitconnected.com/how-to-load-external-javascript-files-from-the-browser-console-8eb97f7db778

## Collaborative Editing

https://github.com/thealmarques/tinymce-collaborative-editing-plugin

## Emulating Medium Editor

https://www.tiny.cloud/blog/medium-editor/

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="tinymce" data-slug-hash="ZEbrjPB" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Emulating the Medium editor">
  <span>See the Pen <a href="https://codepen.io/tinymce/pen/ZEbrjPB">
  Emulating the Medium editor</a> by TinyMCE (<a href="https://codepen.io/tinymce">@tinymce</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## D3 Heigharchy

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="js,result" data-user="borntofrappe" data-slug-hash="yRmOrK" data-preview="true" data-editable="true" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="D3 Hierarchy">
  <span>See the Pen <a href="https://codepen.io/borntofrappe/pen/yRmOrK">
  D3 Hierarchy</a> by Gabriele Corti (<a href="https://codepen.io/borntofrappe">@borntofrappe</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Isotope Combination Filtering

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="js,result" data-user="orbitalnight" data-slug-hash="mpoJwg" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Isotope Combination Filtering">
  <span>See the Pen <a href="https://codepen.io/orbitalnight/pen/mpoJwg">
  Isotope Combination Filtering</a> by Bev (<a href="https://codepen.io/orbitalnight">@orbitalnight</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
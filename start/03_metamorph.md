!SLIDE bullets incremental transition=fade
# Metamorph

* Create a "morph" object
* Insert it into the DOM
* Update the object
* Your DOM element is updates automagically

!SLIDE small transition=fade

    @@@javascript
    // Create the morph object
    var morph = Metamorph("Hello World");

    // insert it into the DOM
    $("body").html(morph.outerHTML());

    // replace the contents
    morph.html("Bonjour le monde");

---

    @@@javascript
    <body>
      <script id="metamorph-1-start"
        type="text/x-placeholder"></script>
       Hello World
      <script id="metamorph-1-end"
        type="text/x-placeholder"></script>
    </body>

!SLIDE bullets incremental transition=fade
# And so what ?

* Ember integrates both those libraries natively
* But you can use them independently

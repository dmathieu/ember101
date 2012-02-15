!SLIDE bullets incremental transition=fade
# Handlebars

* A templating language written in javascript
* Inspired by Mustache.js
* But mush faster because it is precompiled into pure javascript.

!SLIDE small transition=fade

    @@@javascript
    people = [
      {firstname: 'Sheldon', lastname: 'Cooper'},
      {firstname: 'Melody', lastname: 'Pond'}
    ]

---

    @@@javascript
    <ul>
      {{#each people}}
        <li>Hello, {{firstname}} {{lastname}}!</li>
      {{/each}}
    </ul>

---

    @@@javascript
    <ul>
      <li>Hello, Sheldon Cooper!</li>
      <li>Hello, Melody Pond!</li>
    </ul>

!SLIDE small transition=fade
# Try it in your browser

    @@@javascript
    <script type="text/x-handlebars">
      Hello {{firstname}}
    </script>

!SLIDE small transition=fade
# Or precompile and create views
## that's nicer

    @@@javascript
    view = Ember.View.create({
      template: Handlebars.compile("Hello {{firstname}}"),
      firstname: "Sheldon"
    });
    view.appendTo('body');

!SLIDE bullets incremental transition=fade
# You can automate the precompilation of course

* With the rails asset pipeline, see [github.com/emberjs/ember-rails](https://github.com/emberjs/ember-rails)
* Just create `filename.js.hjs` view files
* Perhaps there are similar tools for other languages ? Please tell me so I can add them here.

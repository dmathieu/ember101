!SLIDE small transition=fade
# Bindings

    @@@javascript
    MyTVShowApp.person = Ember.Object.create({
      firstName: "Sheldon",
      lastName:  "Cooper"
    });

    MyTVShowApp.show = Ember.Object.create({
      heroNameBinding: 'MyApp.person.firstName'
    });

    // Later, after Ember has resolved bindings...
    MyTVShowApp.country.get('heroName');
    // "Sheldon"


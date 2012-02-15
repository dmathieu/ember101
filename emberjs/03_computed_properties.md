!SLIDE small transition=fade
# Computed properties

    @@@javascript
    MyTVShowApp.person = Ember.Object.create({
      firstName: "Sheldon",
      lastName: "Cooper",

      fullName: function() {
        return this.get('firstName') + ' ' + this.get('lastName');
      }.property()
    });

    MyTVShowApp.person.get('fullName');
    // "Sheldon Cooper"

!SLIDE small
# Computed properties

    @@@javascript
    MyTVShowApp.person = Ember.Object.create({
      firstName: "Sheldon",
      lastName: "Cooper",

      fullName: function() {
        return this.get('firstName') + ' ' + this.get('lastName');
      }.property('firstName', 'lastName')
    });

    MyTVShowApp.person.get('fullName');
    // "Sheldon Cooper"


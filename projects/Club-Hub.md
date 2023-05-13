---
layout: project
type: project
image: img/9c0d82d7-975d-4a83-9d94-b30667351c33.png
title: "Club-Hub"
date: 2023
published: true
labels:
  - HTML
  - CSS
  - JavaScript
  - React
summary: "My team developed a website offering every club at UH Manoa for students to easily view and save."
---

# Club-Hub: Find your club at UH Manoa

<div class="text-center p-4">
  <img src="../9c0d82d7-975d-4a83-9d94-b30667351c33.png" class="img-thumbnail" >
</div>

In this group project, the objective was to create a project solving a problem applicable to UH Manoa students. This was a website geared towards students looking for a compiled registry of all of the clubs a student could join. The student not only has the ability to view every club available to students, but also offers the student the option of saving the clubs they are interested in to their profile. Each club contains its own webpage, consisting of a photo, an accurate description of the club, its goals, and the contact information of its officers. After the user adds a club they are interested in to their profile, they also have the ability to see the clubs associated events. The website also has admin capabilities, in which the admin can easily add, edit, and delete clubs, as well as add, edit, and delete events.

This project used the Bowfolios template as the base for our project. We also included the sign up/in capabilities and retained user-based role permissions depending on the role of admin or user. For this project, I was responsible for coding the add, edit, and remove club functionality. This required interfacing with the collections and publications, as well as creating new meteor methods to bypass permissions set by the boilerplate code. I learned so much about the intricacies of how such databases were stored and implemented. As our page stored over 180 clubs, it was necessary to be able to filter the clubs, which I was also responsible for. Lastly, I edited the actual design of the website itself. This was an extremely complicated project, and learning how to write code based off of code written by others previously was a tough but necessary task. 

Here is some code shows how we constructed the schema for the clubs in the collection:

```javascript
constructor() {
    // The name of this collection.
    this.name = 'ClubsCollection';
    // Define the Mongo collection.
    this.collection = new Mongo.Collection(this.name);
    // Define the structure of each document in the collection.
    this.schema = new SimpleSchema({
      name: { type: String },
      slug: { type: String },
      abbreviation: { type: String },
      topics: { type: Array },
      'topics.$': {
        type: String,
        allowedValues: ['Academic', 'Social', 'ICS', 'Service', 'Leisure', 'Professional', 'Engineering', 'Recreational'],
      },
      description: { type: String },
      goals: { type: String },
      email: { type: String },
      logo: { type: String },
    });
    // Ensure collection documents obey schema.
    this.collection.attachSchema(this.schema);
    // Define names for publications and subscriptions
    this.userPublicationName = `${this.name}.publication.user`;
    this.adminPublicationName = `${this.name}.publication.admin`;
  }
```

You can visit the website at https://club-hub.site/ .

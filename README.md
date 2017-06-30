# meteor_simple-todos
Meteor example from https://www.meteor.com/tutorials/blaze/creating-an-app

---
The HTML entry-point is in [client/main.html](client/main.html)

---
Modified body looks like the following.

body.html
```html
<body>
  <div class="container">
    <header>
      <h1>Todo List</h1>
    </header>
 
    <ul>
      {{#each tasks}}
        {{> task}}
      {{/each}}
    </ul>
  </div>
</body>
 
<template name="task">
  <li>{{text}}</li>
</template>
```

body.js
```javascript
import { Template } from 'meteor/templating';
 
import './body.html';
 
Template.body.helpers({
  tasks: [
    { text: 'This is task 1' },
    { text: 'This is task 2' },
    { text: 'This is task 3' },
  ],
});
```

See [https://www.meteor.com/tutorials/blaze/templates](https://www.meteor.com/tutorials/blaze/templates) for more details.

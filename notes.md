Objects
=======

```

var user = {
  username: 'laura',
  password: 'hammerTime',
  age: 100,
  likesIceCream: true,
  sayHi: function() {
    var sentence = 'My username is '
    console.log(sentence + this.username);
  }
};

console.log(user.username);

```

**to add to the object**

```

user.isPremium = true;

```

**Bracket Notation**
 * keys that are numbers can't be reached with dot notation
 * instead, use bracket notation:

 ```

 var squares = {
   2: 4,
   3: 9,
   4: 16,
   5: 25
 };

 console.log(squares[5]); // 25

 //to add to the squares object:
 squares[6] = 36;
 squares[7] = 49;

 ```

 **When to use bracket notation?**

 ```

 function addProperty(object, newProperty, newValue) {
   object[newProperty] = newValue;
   return object;
 }

 addProperty(user, 'livesInUSA', false);
 addProperty(user, 'canBake', true);
 addProperty(user, 'job', 'web dev');
 console.log(user)

 ```

 **Delete a property**

 ```

 delete user.likesIceCream;

 ```

 **Iterate over an object**

 ```
// for in loop:

 for (var key in user) {
   console.log('>>>key', key);
   console.log('>>>value', user[key]);
 }

 ```

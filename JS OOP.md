> [!note]
> an object can be a property of another object
```js

let Amy = {
  name : 'Amy Liao',
  talk(){
      console.log("Hello");
  }
}

let JYu={
  name: 'JYu Chan',
  spouse: Amy,
  walk(){
      console.log("I am walking on the street.")
  }
}



console.log(JYu.spouse);
JYu.spouse.talk();
```

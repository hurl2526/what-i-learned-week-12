# # **What I Learned Week 12**
## **Day 42** 

Went over hw

Started making objects with functions

example:  

const colors = require('colors');

const primaryColors = ['blue', 'yellow', 'red'];

const capitalizeFirstWord = function(color) {
  return color[0].toUpperCase() + color.slice(1).toLowerCase();
}

const capitalizedColors = primaryColors.map(capitalizeFirstWord);


const dNames = [
  {
    firstName: 'DeAundre',
    lastName: 'Prescott',
    term: 1,
  },

  {
    firstName: 'David',
    lastName: 'Lau',
    term: 1,
  },

  {
    firstName: 'Denis',
    lastName: 'Savgir',
    term: 1,
  },
]

const newStudent = function(firstName, lastName, term = 1) {
  const student = {
    firstName: firstName,
    lastName: lastName,
    term: term,
  }

  return student;
}

const graduate = function(student) {
  //   manual version:
//   const copyOfStudent = {
//     name: student.name,
//     term: student.term,
//   }

  //   function version:
  const copyOfStudent = newStudent(student.firstName, student.lastName, student.term);
  copyOfStudent.term = copyOfStudent.term + 1;

  return copyOfStudent;
}




## **Day 43**

Went over HW

Methods: making objects with functions:


const makeDino = function(name, isCarnivore) {
  const newObj = {
    name: name,
    isCarnivore: isCarnivore,
    humansEaten: 0,

    sayHi: function() {
      const diet = this.isCarnivore ? 'carnivorous' : 'herbivorous';
      return `Rawr! I'm a ${diet} ${this.name}!`;
    },

    switchDiet: function() {
      if (this.isCarnivore === true) {
       this.isCarnivore = false;
      } else {
        this.isCarnivore = true;
      }
    },

    eatMeal: function() {
      if (this.isCarnivore) {
        this.humansEaten += 2;
      }
    },

    eatMeals: function(mealsToEat) {
      let mealsEaten = 0;
      while (mealsEaten < mealsToEat) {
        this.eatMeal();
        mealsEaten++;
      }
    },
  };

  return newObj;
}


## **Day 45**
Went over HW  

Started writing our own object method functions for .push, .pop, .unshift ….

## **Day 41**

went over hw

Started with object Class stuff. cleaner way to write objects  

example:

class Animal{
Constructor(name, age){
Name: name




have to always say ‘new’ Animal(‘dog’)

class Animal {
  constructor(name, species, legs = 4) {
    this.name = name;
    this.species = species;
    this.legs = legs;
  }

  sayHi() {
    return `I'm a ${this.species} with ${this.legs} legs.`;
  }

  sayBye() {
    return 'Bye for now!';
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name, 'dog', 4);
    this.name = name;
  }

  sayHi() {
    return `Woof! ` + super.sayHi();
  }
}

class Tiger extends Animal {
  constructor(name) {
    super(name, 'tiger', 4);
  }

  sayHi() {
    return `RAWR!! ` + super.sayHi();
  }
}

class Snake extends Animal {
  constructor(name) {
    super(name, 'snake', 0);
  }

  sayHi() {
    return `hiss ` + super.sayHi();
  }
}


class Cat extends Animal {
  constructor(name) {
    super(name, 'cat');
  }

  sayHi() {
    return `Meow! ` + super.sayHi();
  }
}

**keyboard shortcuts to remember**  
* multiplt cusors: click at end of one word 
* option click at end of another word.
* Also, highlight a word and then click command D to grab the next of same word  
* select word, command shift L selects them all
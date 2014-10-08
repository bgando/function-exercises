# [Part 2: eFarmony Functions](id:pt2)
[Back to Home](https://github.com/bgando/JS102)

**You will be placing all your code into the scripts.js file** 

### [Scenario 1: Animal User](id:profile)

1. Write a function, `AnimalTestUser`, that has one string parameter, `username`. It returns an object with a username property.

  ```javascript
  var testSheep = AnimalTestUser('CottonBall');
  console.log(testSheep); //{ username: 'CottonBall' }
  ```


1. Write a constructor function, `AnimalCreator` that returns a single animal object. The constructor function has 4 parameters: `username`, `species`, `tagline,` and `noises`. The animal object should have at least 5 properties: `username`, `species`, `noises`, `tagline`, and `friends`. The values should all be strings except `noises` and `friends`, which are arrays. 
  
  ```javascript
  var sheep = AnimalCreator('Cloud', 'sheep', 'You can count on me!', ['baahhh', 'arrgg', 'chewchewchew']);
  console.log(sheep);
        // { username: 'Cloud', 
        //  species: 'sheep', 
        //  tagline: 'You can count on me!', 
        //  noises: ['baahhh', 'arrgg', 'chewchewchew'], 
        //  friends: []
        // }
  ```

1. Write a function, `addFriend` that takes an animal object (like the one returned from the `AnimalCreator` function) and adds another animal object as a friend. 

  ```javascript
    addFriend(sheep, cow);
    console.log(sheep);
          // { username: 'Cloud', 
          //  species: 'sheep', 
          //  tagline: 'You can count on me!', 
          //  noises: ['baahhh', 'arrgg', 'chewchewchew'], 
          //  friends: [{username: 'Moo', species: 'cow'...}]
          // }
    addFriend(sheep, llama);
    console.log(sheep);
          // { username: 'Cloud', 
          //  species: 'sheep', 
          //  tagline: 'You can count on me!', 
          //  noises: ['baahhh', 'arrgg', 'chewchewchew'], 
          //  friends: [{username: 'Moo', species: 'cow'...}, {username: 'Zeny', species: 'llama'...}]
          // }
  ```

1. Change your `addFriend` function to only add the username of the friend, not the whole object.

  ```javascript
    addFriend(sheep, cow);
    console.log(sheep);
          // { username: 'Cloud', 
          //  species: 'sheep', 
          //  tagline: 'You can count on me!', 
          //  noises: ['baahhh', 'arrgg', 'chewchewchew'], 
          //  friends: ['Moo']
          // }
    addFriend(sheep, llama);
    console.log(sheep);
          // { username: 'Cloud', 
          //  species: 'sheep', 
          //  tagline: 'You can count on me!', 
          //  noises: ['baahhh', 'arrgg', 'chewchewchew'], 
          //  friends: ['Moo', 'Zeny']
          // }
  ```
  
1. 

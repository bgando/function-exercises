# [Part 2: eFarmony Functions](id:pt2)
[Back to Home](https://github.com/bgando/JS102)

These exercises emulate real problems you will encounter when making a dating app. Your task is to respond with solutions to the challenges presented. This is a free-form exercise so be creative!

**You will be placing all your code into the scripts.js file** 

### [Scenario 1: Animal User](id:profile)

1. Write a constructor function, `AnimalCreator` that returns a single animal object. The constructor function has 4 parameters: `username`, `species`, `tagline,` and `noises`. The animal object should have at least 5 properties: `username`, `species`, `noises`, `tagline`, and `friends`. The values should all be strings except `noises` and `friends`, which are arrays. 
  
  ```javascript
  var sheep = AnimalCreator('Cloud', 'sheep', 'You can count on me!', ['baahhh', 'arrgg', 'chewchewchew'])
  sheep // {username: 'Cloud', species: 'sheep', tagline: 'You can count on me!', noises: ['baahhh', 'arrgg', 'chewchewchew'], friends: []}
  


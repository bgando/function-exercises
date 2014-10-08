# [Part 2: eFarmony Functions](id:pt2)
[Back to Home](https://github.com/bgando/JS102)

These exercises emulate real problems you will encounter when making a dating app. Your task is to respond with solutions to the challenges presented. This is a free-form exercise so be creative!

**You will be placing all your code into the scripts.js file** 

### [Scenario 1: Animal Profile Page](id:profile)
In our first scenario, we want to create a profile page for one of our animals. We will create functions that will help organize our data and present it to the user in a human-readable way.

##### 1a: Log the Animal Personal Data
- Write a function named `welcomeMessage` that takes an animal object like this one: `{ username: 'duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }` 
  and returns a string that says "Welcome, \<username>!".
  - Your result should look like this: `"Welcome, Duck!"`
  - use your `CapitalizeStr` function inside `welcomeMessage` to ensure correct capitalization.
- Write a function named `profileData` that takes an animal object like the duck example in the previous exercise. It returns a string that includes both the username and tagline with their corresponding values. The result should look like this:
  - `"username: duck, tagline: Afflack"`
  - Note: Do not include the noises array for now
  - use `capitalizeStr` inside of `profileData` to ensure proper capitalization
    -new output will look like this: `"username: Duck, tagline: Afflack"`
- Edit your profileData function to include the noises array with its values
  - `"username: Duck, tagline: Afflack, noises: quack, honk, sneeze, growl"` 

  
##### 1b: Animal Relationship Data
- Create a function called `relationshipLogger` that takes an animal object and returns the relationship object if it contains one. Otherwise, have your function log `"You have no relationships :("` 

- Write a function called `relationshipChecker` that takes two parameters, the username name and an animal object. The function returns the relationship between the username and animal. 
  - Suggested outputs:'\<username> is a match of \<animal>', '\<username> is a friend of \<animal>', '\<username> and \<animal> have no relation yet', etc. 
  - Make sure you test all these different scenarios
- `addFriend` is a function that allows your animal object to add a friend. It takes a username (this could be just the name or the entire object depending on how you want to architect your app) and an animal object and adds that username on to the animal object 
  - Remember the friendslist in the relationship object? That is where you should store data about friends in your animal object
- Similar to `addFriend`, `addMatch` should add a match to your animal object. 
    
### [Scenario 2: Browse Animals Page](id:browse)
In this scenario, we will show all the animals in our collection so that a user can browse through and see who is out there on our app. This page or the profile page might be the homepage application.

- `nonFriends` is a function that shows which animals in your collection are not in your friendlist. You don't want current friends to show up while you are browsing for new friends.
  - You can choose how to present this data in a way that makes the most sense to you.

### [Scenario 3: Search and Add Friends](id:search)
All social networking sites have a search component so that you can find a particular user. You also need to be able to add friends and matches. Let's do these exercises and see what that might look like in code. 

- `search` takes a search query and returns an array of animal objects that contain an exact match anywhere in the body of the object. 
  - Note: the match must be exact for this to work and won't work with objects or arrays. Just primitive types (numbers, strings, booleans, etc.) 
  - You will be searching through your entire animals collection
- Extra credit: How can you make this work with any type of nested data structure? (Assuming we might want to change the structure of our data in the future and wouldn't want it to break our code.)
- Write a function that ensures that no friends in your friendslist are repeated. It might take an array and return that array without any duplicate entries.

### [Scenario 4: Edit Animal Profile Page](id:editprofile)
What if you wanted to edit your profile page? Let's create the logic that goes into that!

- Create a function that takes your animal object, the key you wish to change and the new value.
  - if the the property doesn't yet exist, add it! 
  

### [Scenario 5: Edit Animal Collection Data](id:editcollection)
What if you wanted to change the data on the whole collection? 

- Write a function to introduce a new property with an initial value. This might be for the administrator of the website/database. 

  - Use this function to add a property called points and have all users start off with 0 points. 
  - Be sure to first check if the property already exists. If it does, don't override it with the in initial value.

- Write a function that creates a new animal object and adds it to the animals collection. You might want to pass in the username values, friends, etc as arguments into your function. 
  - How could the arguments keyword come in handy here?
- `cleanseData` is a function that takes the animals collection and a series of key names. It will remove any properties on the animal objects that are not given as arguments
  - input `cleanseData([{'a': 'b', 'c': 'd'},{'a': 'q'}], 'a');`
  - output `[{'a': 'b'},{'a': 'q'}]`

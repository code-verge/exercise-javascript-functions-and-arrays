# exercise-javascript-functions-and-arrays

## Learning Goals

Upon completing this exercise, you will be able to:

- Create and manipulate arrays in JavaScript
- Implement functions with parameters and return values
- Utilize loops (`for`, `forEach`) to iterate over arrays
- Create and work with objects in JavaScript
- Use the `map()` method to transform arrays
- Filter arrays based on specific criteria

## Introduction

Welcome to the world of espionage! As a skilled spymaster working for MI5, your mission is to manage and analyze intelligence data related to our top agents. Your task is to create a set of JavaScript functions and utilize arrays to efficiently handle the spy roster, agent details, and gadget assignments. Your code will play a crucial role in organizing and extracting valuable information about our spies, ensuring the success of our covert operations. Get ready to put your coding skills to the test and prove yourself as a valuable asset to the agency.

Let’s dive in! 🔥

## Getting Started

1. Fork the repository
2. Clone the repository to your computer
3. Open the repository in VS Code
4. Start the Live Server in VS Code
5. Follow instructions

## **Instructions**

Create a file named `spymaster.js` to write your JavaScript code for the following tasks.

### **Task 1: Spy Roster**

"James", "Sarah", "Michael", and "Emily" are all spies based in Baker Street, London. Store their names in an array called `londonSpies`.

Create a function called `printSpyRoster` that takes in the following parameter:

- `spies` (array of strings): An array containing the names of the spies.

The function should do the following:

1. Print the names of the spies in the array using a `forEach` loop.
2. Print the number of spies in the array.

Expected output:

```jsx
James
Sarah
Michael
Emily
Number of spies: 4
```

### **Task 2: Spy Credentials**

Create a function called `createSpyCredentials` that takes in the following parameters:

- `name` (string): The name of the spy
- `alias` (string): The spy's alias
- `skills` (array of strings): An array containing the spy's skills

The function should return an object called `spyObject` with the following properties:

- name: The name of the spy
- alias: The spy's alias
- skills: The array of spy skills

Expected output:

```jsx
{
  name: "James Bond",
  alias: "007",
  skills: ["Stealth", "Deception", "Marksmanship"]
}
```

*In the expected output above, we provide example values for the name, alias, and skills variables. When calling this function, you can pass these values as arguments. Make sure that your function returns an object called `spyObject` that resembles the expected output above.*

### Task 3: Spy Evaluation

Create a function called `evaluateSpySkills` that takes in the following parameter:

- `spyObject` (object): An object representing a spy, with properties name, alias, and skills.

The function should iterate over the `skills` array using a `for` loop and print each skill to the console.

Expected Output:

```jsx
Stealth
Deception
Marksmanship
```

### Task 4: Spy Extraction

Create an array of spy objects called `topSpies` where each object represents a spy with properties name, alias, and skills. Use the data below to populate your array.  

*Note that `skills` is an array too.*

| **name** | **alias** | **skills (array)** |
| --- | --- | --- |
| James Bond | 007 | Stealth, Deception, Marksmanship |
| Ethan Hunt | IMF Agent | Infiltration, Disguise, Hand-to-Hand Combat |
| Naomi Bourne | Bourne | Martial Arts, Surveillance, Deception |

Create a function called `extractSpyNames` that takes in the `topSpies` array.

The function should extract the names of the spies from the `topSpies` array and return a new array containing only the spy names.

Expected Output

```jsx
["James Bond", "Ethan Hunt", "Jason Bourne"]
```

### Task 5: Spy Filtering

Create a function called `filterSpiesBySkill` that takes in the following parameters:

- `spies` (array of objects): An array of spy objects, where each object has properties name, alias, and skills.
- `skill` (string): The skill to filter the spies by.

The function should return a new array containing only the spies who possess the specified skill.

Test your function by passing in your `topSpies` array from the previous task and pass in one of the skills of your choosing.

Expected Output:

```jsx
const stealthSpies = filterSpiesBySkill(topSpies, "Stealth");
console.log(stealthSpies);

/* Output:

[
  {
    name: "James Bond",
    alias: "007",
    skills: ["Stealth", "Deception", "Marksmanship"]
  }
]
*/
```

*You can achieve this result with either a `for` loop or a `forEach` loop however, try to use the `map()` method.*

### **Bonus Task: Spy Gadget Inventory**

You are given an array of `gadgets`, where each gadget is represented as an object with properties name and skill. Here's the `gadgets` array:

```jsx
const gadgets = [
  { name: "Invisibility Cloak", skill: "Stealth" },
  { name: "Disguise Kit", skill: "Deception" },
  { name: "Laser Watch", skill: "Marksmanship" },
  { name: "Grappling Hook", skill: "Infiltration" },
  { name: "Voice Modulator", skill: "Disguise" },
  { name: "Shock Gloves", skill: "Hand-to-Hand Combat" },
  { name: "Smoke Bomb", skill: "Martial Arts" },
  { name: "Mini Drone", skill: "Surveillance" },
  { name: "Standard Issue", skill: "Standard Issue" }
];
```

Don’t forget to copy and paste this array into your JavaScript file.

Create a function called `assignGadget` that takes in the following parameters:

- `spy` (object): An object representing a spy, with properties name, alias, and skill.

The function should assign a gadget to the spy based on their skill. The function should return the `spy` object with an additional property `gadget` representing the assigned gadget.

The assignment of gadgets should follow this rule:

- If the spy's skill matches the skill of a gadget, assign that gadget to the spy.
- If no matching gadget is found, assign the gadget with the skill "Standard Issue".

Example Output:

```jsx
{
  name: "James Bond",
  alias: "007",
  skill: "Marksmanship",
  gadget: {
    name: "Laser Watch",
    skill: "Marksmanship"
  }
}
```

## **Submission**

When you've completed the exercise:

1. Run the following commands:

```jsx
git add .
git commit -m "Completed JavaScript Functions and Arrays"
git push origin main
```

1. Create a Pull Request and submit your assignment.

Happy coding, agent! 🕵🏻‍♀️💻

## Frequently Asked Questions (FAQs)

<details>
  <summary>How can I iterate over an array in JavaScript?</summary>
 
You can use a `for` loop or the `forEach()` method to iterate over an array in JavaScript. The `for` loop allows you to specify the starting point, condition, and increment/decrement, while the `forEach()` method executes a provided function once for each array element.
    
    ```jsx
    // for loop
    const numbers = [1, 2, 3, 4, 5];
    for (let i = 0; i < numbers.length; i++) {
      console.log(numbers[i]);
    }
    
    // forEach method
    const numbers = [1, 2, 3, 4, 5];
    numbers.forEach(function(number) {
      console.log(number);
    });
    ``` 
 
</details>

<details>
  <summary>How can I create an object in JavaScript?</summary>
 
You can create an object in JavaScript using the object literal notation. Object literal notation is the most common way, where you define an object using curly braces `{}` and specify its properties and values using key-value pairs.
    
    ```jsx
    // Creating an object using object literal notation
    const person = {
      name: "John",
      age: 30,
      city: "New York"
    };
    ```

 
</details>

<details>
  <summary>What is the `map()` method in JavaScript?</summary>
 
The `map()` method creates a new array by calling a provided function on every element in the original array. It transforms each element based on the logic defined in the provided function and returns a new array with the transformed elements.
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5];
    const doubledNumbers = numbers.map(function(number) {
      return number * 2;
    });
    console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
    ```
 
</details>

<details>
  <summary>How can I filter an array based on a specific condition?</summary>

You can use the `filter()` method to create a new array with all elements that pass a specific condition. The `filter()` method takes a callback function as an argument, which is executed for each element in the array. The elements for which the callback function returns true are included in the new array.
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5];
    const evenNumbers = numbers.filter(function(number) {
      return number % 2 === 0;
    });
    console.log(evenNumbers); // Output: [2, 4]
    ```

</details>

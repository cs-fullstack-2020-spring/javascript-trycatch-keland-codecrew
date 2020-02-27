# JavaScript loops, try/catch, Objects classwork

## Excercise 1: try/catch
Review the following JavaScript

```
<!DOCTYPE html>
<html>
<head>
      <title>Intro to JavaScript</title>
      <meta charset="utf-8" />
</head>
<body>
      <script>
           try {
                processFile()
           }
           catch (ex) {
                console.log(ex);
           }
           finally {
                console.log('Closing the file')
           }

           function processFile(filename) {
                if (!filename)
                     throw new Error('No file to process!');
                console.log('Working on it');
                try {
                     console.log('Opening the file');
                     throw new Error('Issue with the file content');
                }
                catch (ex) {
                     console.log('File content not formatted properly');
                }
                finally {
                     console.log('Wrapping up')
           }
      }
      </script>
</body>
</html>

```
- WITHOUT RUNNING THIS CODE What will the output be in the browser?
Record answer here: THE CORRECT ANSWER IS: 
```
ANSWER A
Error: No file to process! 
Closing the file

ANSWER B
No file to process! 
Working on it 
Opening the file
Issue with the file content File content not formatted properly 
Wrapping up

ANSWER C
No file to process! 
Working on it 
Opening the file 
Issue with the file content File content not formatted properly
Wrapping up Closing the file
```

## Exercise 2: Loops/continue/break
- Write a JavaScript program that prompts the user team name and then team city
- If the user leaves either field blank, display an alert that says `Field cannot be blank!' and reprompts the user for team name and city
- If the user enters data for both fields, then use a `confirm` box to get confirmation from the user that they want to add the team to the list (ex. `Add the Grizzlies of Memphis to your Team list?`
  - If the user selects cancel, do not add team to list and prompt for next team
  - If user confirms addition of team to list, add the team to a team array and prompt for next team
- If the user enters `X` for either entry, you should break from your loop and print out the list of teams entered in the console

## Exercise 3: Object Literals
- Create an object literal that represents a Club Member
- Each Member should have a name, club role, contact email, and contact phone number
- In your code, create 4 instances of Club Members using any data you like and add them to an array called `club_members`
- Write the code to create a club member listing by printing a *Report Title`, then looping through the club member array printing each club member's details, and finally printing a count of club members

Example Output:
```
CURRENT CLUB MEMBERS

Name: Bob
Role: Secretary
email: bob@mail.com
Phone: 555-555-55555

Name: Bob
Role: Secretary
email: bob@mail.com
Phone: 555-555-55555

OUR CLUB PRESENTLY HAS 2 MEMBERS
```

## Challenges:
- Create each member object instance by adding all properties through code
- Create a function that when passed a club member object will return a formatted member details string to output (Call for each club member)



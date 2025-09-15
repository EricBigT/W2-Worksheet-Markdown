# W2-Worksheet-Markdown

1. What is fault localization?
  - Fault localization is when you **backtrace** your code from the point of error to the root cause of it
2. What are three benefits of Test Driven Development (TDD)?
  - Your tests are not biased by your code
  - Writing tests helps you think about how you might write code
  - Writing tests helps you think about the requirements of your system
3. Using input domain partitioning, write a test set that checks that a method that gives discounts to children and seniors of 50% and 25% respectively works as intended. The input to this method is a single variable, age, and the output is the discount.
  - public double determineDiscount(int age){
      if (age >= 0 && age <= 17){
        return 0.5;}
      else if (age >= 60 && age <= 100){
        return 0.25;}
      else if(age < 0){
        throw invalidArgument;}
      else{
        return 1.0;}
      }
4. Given the example of requirements for generating a password:
  - It must have at least one number.
  - It must have at least one uppercase letter.
  - It must have at least one lowercase letter.
  - It must not contain the website gmail anywhere. (For example if we were generating a password for gmail accounts)
  - It can only be made up of letters, numbers, and the underscore.
What are the input domain paritions for this eIf xercise?
  - public boolean workingPassword(String input){
    int uppercase, lowercase, digit, underscore = 0;
      for (int i = 0; i < input.length; i++){
        if (input.charAt(i) >= 65 && input.charAt(i) <= 90){
          uppercase++;}
        else if (input.charAt(i) >= 97 && input.charAt(i) <= 122){
          lowercase++;}
        else if (input.charAt(i) >= 48 && input.charAt(i) <= 57){
          digit++;}
        else if (input.charAt(i) == 95){
          underscore++;}
        else{
          return false;}
        if (uppercase > 0 && lowercase > 0 && digit > 0){
          return true;}
5. What are the input domain paritions for this exercise?
  - lists of size 1: only one location
  - lists of size 2: min at start or min at end
  - lists of size 3 or more: min at start, min at end, min in middle

6. | a > b | G | x < y | Predicate Outcome |
   |------|---|-------|------------------|
   |  T   | F |   T   |        T         |
   |  F   | F |   T   |        F         |
   |  F   | T |   T   |        T         |
   |  F   | F |   T   |        F         |
   |  T   | F |   T   |        T         |
   |  T   | F |   F   |        F         |

7.  1 → 2 → 5 → 7
    1 → 2 → 5 → 6 → 7
    1 → 3 → (4 → 3)* → 5 → 7
    1 → 3 → (4 → 3)* → 5 → 6 → 7
This is not a finite set because the loop of 4 to 3 could go on infinitely many times.

8. The benefit of using [mutation testing](https://www2.seas.gwu.edu/~kinga/CS2113_F25/lectures/l2.html) is that it can uncover gaps in your test cases and checks the quality of you test cases by seeing if your test cases catch the new changes.

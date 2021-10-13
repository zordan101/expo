## Run test code :-
  - Run the test code with the below command :-
  ```
  # /usr/bin/food_size_estimator-test <input-folder-name>
  ```
   - input folder has all the images on which food_size_estimator is to be tested
   - input folder should also have a text file named 'input.txt'
   - 'input.txt' should have data in the following format :-
      
      <*image-name*> <*food-index*> <*ground-truth*>
       
       example :-
       ```
       image_210716(102914).jpg 0 7
       image_210716(102919).jpg 6 11
       image_210716(102922).jpg 8 2
       ```
   - after running the test command, input foler will have a text file 'result.txt' which has results in the following format :-
      
      <*Sr No.*> <*image-name*> <*time-required*> <*food-item*> <*ground-truth*> <*predicted count or volume*> <***O*** *or* ***X***>
       
       example :-
       ```
       1 image_210716(102914).jpg 354ms chickenbreast 10 10 O
       2 image_210716(102919).jpg 356ms salmonsteak 15 14 X
       3 image_210716(102922).jpg 354ms lasagna 2 2 O
       ```

## Note
  - For food items targeted for food-count ground truth values range from 0 to 16 which is the number of food item present in the image.
  - For food items targeted for food-volume ground truth values can be **1 - small, 2 - medium, 3 - large** food sizes. Predicted food-volume can also be **0 - unknown** including other three values.
  - Right or wrong prediction result is displayed using **O for correct prediction** and **X for incorrect prediction**.
  - Following are the food indices for food items used in the library.
    | Food item     | Food index |
    | ------------- |:-------------:|
    |chickenbreast      | 0     |
    | chickendrumsticks      | 1     |
    | salmonfillet      | 2     |
    |peeledpotatohalves      | 3     |
    |duckbreast      | 4     |
    |baguettes      | 5     |
    |salmonsteak      | 6     |
    |frozenpizza      | 7     |
    |lasagna      | 8     |
    |wholechicken      | 9     |
    |sconebiscuits      | 10     |
    |chocochipcookies      | 11    |
---

## Run test code :-
  - Run the test code with the below command :-
  ```
  # /usr/bin/vnn-cooking_state_recognition-test --video <path-to-test-video> --done_time <time(minutes)> --overdone_time <time(minutes)  --result <path-to-output-file>
  ```
   - provide complete path to test video file. 
   - done_time is the time when done state of food started.
   - overdone_time is the time when overdone state of food started.
   - If the done or overdone state is not achieved then need to provide the complete video file duration(minutes).
   - provide complete output/result text file path.
   
       

   - after running the test command, specified output text file will have results in the following format :-
      
      <*Sr No.*> <*test-video-file*> <*current-time(minutes)*> <*ground-truth-food-state*> <*predicted-food-tate*> <inference-time>
       
       example :-
       ```
       1 /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4  1       0       0       287
       2 /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4  2       0       0       295
       3 /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4  3       0       0       267
       ```
  
## Note
  - Three food states `UnderCooked/UnderDone`, `Cooked/Done`, `OverCooked/OverDone` are considered for targeted food items for cooking-state-recognition 
  - For food items targeted for cooking-state-recognition ground truth values can be **0 - underdone, 1 - done, 2 - overdone** . 
  
---

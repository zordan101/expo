## Run test code :-
  - Run the test code with the below command :-
  ```
   /usr/bin/vnn-cooking_state_recognition-test --video <input-video-file> --done_time <time(minutes)> --overdone_time <time(minutes)>  --result <output-file>
  ```
   - input video file is the path to the mp4 video file on which cooking-state-recognition to be tested. 
   - done_time is the ground truth time(in minutes) for the input video when the done state of food starts.  
   - overdone_time is the ground truth time(in minutes) for the input video when the overdone state of food starts.
   - If the done or overdone state is not achieved then need to provide the complete video file duration(minutes).
   - output file contains the results as predicted by cooking-state-recognition.
   
       

   - after running the test command, specified output text file will have results in the following format :-
      
       <*video-file*> <*current-time(minutes)*> <*ground-truth-food-state*> <*predicted-food-tate*> <*time-required (in milliseconds)*>
       
       example :-
       ```
        /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4  1       0       0       287
        /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4  2       0       0       295
        /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4  3       0       0       267
       
        /home/owner/media/cooking_data/SalmonSteak_case#2_20210726.mp4 33       1       1        280
       ```
  
## Note
  - Three food states `UnderCooked/UnderDone`, `Cooked/Done`, `OverCooked/OverDone` are considered for targeted food items for cooking-state-recognition.
  - The ground truth and predicted labels in the output file can be **0 - underdone, 1 - done, 2 - overdone** . 
  - If output file is not provided, the results will be present at ```/home/owner/media/cooking_state_result.txt``` by default.
  
---

# Graduation work in ML courses
The task is to predict whether the user will be able to successfully complete the online course

We will assume that the user has successfully completed the course if he has correctly solved more than 40 practical tasks.


## Data
### For training
Information about decisions and actions for 6184 students for the first two days of the course is stored. These are 6184 students who took the course in the period from May 2018 to January 2019. For a detailed description of the variables, see this step.

- /datasets/event_data_train.zip — data about actions performed by students with steps:
  - step_id 
  - user_id - anonymized user id.
  - timestamp - the time when the event occurred in unix date format
  - action - event, possible values:
    - started_attempt - start of the attempt to solve.
    - passed - a successful solution to a practical step.

- /datasets/submissions_data_train.zip — data about the time and status of submits for practical tasks:
  - submission_status - solution status
  - step_id 
  - user_id - anonymized user id.
  - timestamp - the time when the event occurred in unix date format
### For prediction
Using data from the first two days of activity on the course, you need to predict whether the user will score more than 40 points on the course or not.

- /datasets/event_data_test.csv — like event_data_train.zip, but contains data for the first 2 days.
- /datasets/submissions_data_test.csv — like submissions_data_train.zip, but contains data for the first 2 days.
## Results
In the final, a csv file is generated with an estimate of the probability of classes for each user

ROC AUC: 0.888. It is included in the top 10 results among the participants


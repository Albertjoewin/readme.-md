# readme.-md
Overview:
The app will initially take some inputs from the user whether he/she is interested in losing/maintaining/gaining muscle and some extra information regarding the same. Based on the inputs, the software will map the videos, diet and schedule them for the particular user. Further, the app keeps track of the workouts and diet maintained by the user and gives him a score to assess his discipline.

database:
| User |       |
|------|-------|
| id   | name  |
| 1    | Ilka  |
| 2    | James |

| Exercise |                     |               |
|----------|---------------------|---------------|
| id       | name                | track_type_id |
| 1        | Barbell Bench Press | 1             |
| 2        | Squats              | 1             |
| 3        | Deadlifts           | 1             |
| 4        | Rowing Machine      | 3             |

| Workout |         |                 |
|---------|---------|-----------------|
| id      | user_id | name            |
| 1       | 1       | Chest & Triceps |
| 2       | 1       | Legs            |

| Workout_Exerice (Junction table)   |            |
|-----------------|------------------|------------|
| id              | exersice_id      | workout_id |
| 1               | 1                | 1          |
| 2               | 2                | 1          |
| 3               | 4                | 1          |

| Workout_Sets |                     |      |        |
|--------------|---------------------|------|--------|
| id           | workout_exersice_id | reps | weight |
| 1            | 1                   | 12   | 120    |
| 2            | 1                   | 10   | 120    |
| 3            | 1                   | 8    | 120    |
| 4            | 2                   | 10   | 220    |
| 5            | 3                   | null | null   |

| TrackType |                 |
|-----------|-----------------|
| id        | name            |
| 1         | Weight and Reps |
| 2         | Reps Only       |
| 3         | Distance Time   |

# QoE-and-Immersion-of-Dynamic-Point-Cloud
This repository contains the results of a subjective test on the quality of experience (QoE) for dynamic point clouds. Details and analysis can be found in the Reference section.

## Data Description
The results include two files: `subjective_test_results.csv` and `questionnaire_responses.csv`. This section describes the content of each files.

### Subjective Test Results
The table in file `subjective_test_results.csv` contains the following information of the subjective test results

| Column Name   | Data Type | Description                                                  |
|---------------|-----------|--------------------------------------------------------------|
| participant   | Int       | The index of the participant                                 |
| object        | String    | The name of the 3D object in the test sequence               |
| start_quality | String    | The quality in the first 5 s of the test sequence            |
| end_quality   | String    | The quality in the last 5 s of the test sequence             |
| distance      | Float     | The viewing distance (m)                                     |
| start_gqp     | Int       | The Geometry QP (G-QP) in the first 5 s of the test sequence |
| start_tqp     | Int       | The Texture QP (T-QP) in the first 5 s of the test sequence  |
| end_gqp       | Int       | The Geometry QP (G-QP) in the last 5 s of the test sequence  |
| end_tqp       | Int       | The Texture QP (G-QP) in the last 5 s of the test sequence   |
| qoe           | Int       | The score rated by the participant                           |

### Questionnaire Responses
Before the test, we asked the participant to provide some background information, tested their color vision with Ishihara[^1].
[^1]: [https://en.wikipedia.org/wiki/Ishihara_test](https://en.wikipedia.org/wiki/Ishihara_test)

After the test, the participants answered a survey about cybersickness and the immersion level of the tested objects.
The answers are stored in the table of file `questionnaire_responses.csv`. The structure of the table is described as follow.

| Column Name                                                                                                   | Data Type | Description                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------|
| participant                                                                                                   | Int       | The index of the participant                                                                                     |
| Which number do you see below?                                                                                | Int       | The first tested number for Ishihara test (must be 12)                                                           |
| Which number do you see below?                                                                                | Int       | The second tested number for Ishihara test (must be 45)                                                          |
| Which number do you see below?                                                                                | Int       | The third tested number for Ishihara test (must be 74)                                                           |
| During the assignment I felt... [General discomfort]                                                          | String    | Level of agreement with options: `Strongly disagree`, `Disagree`, `Neutral`, `Agree`, `Strongly Agree`           |
| During the assignment I felt... [Nausea]                                                                      | String    | Level of agreement with options: `Strongly disagree`, `Disagree`, `Neutral`, `Agree`, `Strongly Agree`           |
| During the assignment I felt... [Sweating]                                                                    | String    | Level of agreement with options: `Strongly disagree`, `Disagree`, `Neutral`, `Agree`, `Strongly Agree`           |
| During the assignment I felt... [Headache]                                                                    | String    | Level of agreement with options: `Strongly disagree`, `Disagree`, `Neutral`, `Agree`, `Strongly Agree`           |
| During the assignment I felt... [Dizziness]                                                                   | String    | Level of agreement with options: `Strongly disagree`, `Disagree`, `Neutral`, `Agree`, `Strongly Agree`           |
| How would you describe the general experience? [I felt the objects were part of the real environment]         | String    | Level of agreement with options: `Strongly disagree`, `Disagree`, `Neutral`, `Agree`, `Strongly Agree`           |
| What is your gender?                                                                                          | String    | Gender with options: `Male`, `Female`, `Non-binary`, `Prefer not to say`                                         |
| What is your age group?                                                                                       | String    | Age group with options: `Under 18`, `18-24`, `25-34`, `35-44`, `45-54`, `55-64`, `65-74`, `75-84`, `85 or older` |
| How often have you watched/experienced extended reality content (e.g, 360 videos/games, holographic content)? | String    | Frequency with options: `Never`, `Once`, `A few times`, `Monthly`, `Weekly`, `Daily`                             |

## Reference
If you use the data provided in this repository, please cite the following papers.

```
@INPROCEEDINGS{10178491,
  author={Nguyen, Minh and Vats, Shivi and Van Damme, Sam and Van Der Hooft, Jeroen and Vega, Maria Torres and Wauters, Tim and Timmerer, Christian and Hellwagner, Hermann},
  booktitle={2023 15th International Conference on Quality of Multimedia Experience (QoMEX)}, 
  title={Impact of Quality and Distance on the Perception of Point Clouds in Mixed Reality}, 
  year={2023},
  pages={87-90},
  doi={10.1109/QoMEX58391.2023.10178491}
}
```


# 📊 Esports Tournament Data Analysis
This project is about SQL to perform exploratory data analysis. The data set is a dummy data set with some minimal data.
This project is basically done to gain some better knowledge and have a more tighter grip upon SQL. 
For this I have used SQLite.



## 🗂 Creating Database
Created a database of a Tournament with and inserted some dummy data to do some analysis upon the data. The database, named zomato_data contains 4 tables: Teams, Matches and Players.

## 1️⃣ creating table Teams:
        CREATE TABLE Teams (
        team_id INT PRIMARY KEY,
        team_name VARCHAR(50) NOT NULL,
        country VARCHAR(50),
        captain_id INT
        );
## 2️⃣ creating table Players:
        CREATE TABLE Players (
        player_id INT PRIMARY KEY,
        player_name VARCHAR(50) NOT NULL,
        team_id INT,
        role VARCHAR(50),
        salary INT,
        FOREIGN KEY (team_id) REFERENCES Teams(team_id)
        );
## 3️⃣ creating table Matches:
        CREATE TABLE Matches (
          match_id INT PRIMARY KEY,
          team1_id INT,
          team2_id INT,
          match_date DATE,
          winner_id INT,
          score_team1 INT,
          score_team2 INT,
          FOREIGN KEY (team1_id) REFERENCES Teams(team_id),
          FOREIGN KEY (team2_id) REFERENCES Teams(team_id),
          FOREIGN KEY (winner_id) REFERENCES Teams(team_id)
          );
          
## 📈 Some Analysis That Are Performed
From next are some important questions based on which analysis is performed. Some these questions are really important in improving upon any particular product, the business model.

## 1. What are the names of the players whose salary is greater than 100,000?
![steel_data_p2_1](https://github.com/mr-omkar/sql/assets/65303335/81f85e77-d6fb-4815-8870-4f2c08467c2f)

## 2. What is the team name of the player with player_id = 3?
![steel_data_p2_2](https://github.com/mr-omkar/sql/assets/65303335/c7010a43-8ec8-4c1d-83ce-82e1c475618e)

## 3. What is the total number of players in each team?
![steel_data_p2_3](https://github.com/mr-omkar/sql/assets/65303335/2132dd6e-8878-4756-b475-5c91841245f4)

## 4. What is the team name and captain name of the team with team_id = 2?
![steel_data_p2_4](https://github.com/mr-omkar/sql/assets/65303335/8342369e-ebe3-4f27-8ad0-42b94cfbb08b)

## 5. What are the player names and their roles in the team with team_id = 1?
![steel_data_p2_5](https://github.com/mr-omkar/sql/assets/65303335/24863663-b578-4e56-990b-baa2c3e2fe0f)

## 6. What are the team names and the number of matches they have won?
![steel_data_p2_6](https://github.com/mr-omkar/sql/assets/65303335/396e1214-82c4-4c00-b6fd-c235f1696593)

## 7. What is the average salary of players in the teams with country 'USA'?
![steel_data_p2_7](https://github.com/mr-omkar/sql/assets/65303335/83d61d4d-18e4-426c-88bb-806c089e85d4)

## 8. Which team won the most matches?
![steel_data_p2_8](https://github.com/mr-omkar/sql/assets/65303335/090a21d6-281b-408a-b6a7-51d598eedbd0)

## 9. What are the team names and the number of players in each team whose salary is greater than 100,000?
![steel_data_p2_9](https://github.com/mr-omkar/sql/assets/65303335/047595c4-8322-4c4a-a99c-935d379a252b)

## 10 What is the date and the score of the match with match_id = 3?
![steel_data_p2_10](https://github.com/mr-omkar/sql/assets/65303335/bcb1f154-796f-44ca-9b78-2f5ac8dcfd6d)


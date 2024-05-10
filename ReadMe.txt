If you have questions on how to run, email ayupovalandis@gmail.com. Please title your email "GIT QUESTION - {Name of repository}. I will reply given some time and will possibly update the ReadMe if needed.

Had difficulty with replacing white arrow folder in github. Code for bot is here: https://github.com/AlandisAyupov/bot

TO RUN BOT:
Navigate to bot directory. 

run "npm install"

Replace process.env.PASS with the password for your MySQL database, and other settings (like database name) if needed. You can watch this tutorial on how to create a discord bot, some of the information isn't 
needed but this tutorial is still helpful: https://www.youtube.com/watch?v=KZ3tIGHU314&list=PLpmb-7WxPhe0ZVpH9pxT5MtC4heqej8Es .

// CODE YOU NEED TO EDIT - FIRST SEGMENT
const db = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: process.env.PASS,
  database: "fics",
});
// SECOND SEGMENT
const commands = [
  {
    name: 'fics',
    description: 'Displays fics.',
  },
];
// THIRD SEGMENT
await rest.put(
      Routes.applicationGuildCommands(
        process.env.CLIENT_ID,
        process.env.GUILD_ID
      ),
      { body: commands }
    );


TO RUN FICSCRAPER: 

Requirements:
Python installation. 
MySQL installation.

You may have to create your own virtual environment if you are running it under the newest version of Python. Delete the venv folder, and run the following commands.

Create virtual environment:
python -m venv venv

Activate virtual environment (May be different command depending on OS) - must be in directory where virtual environment is:
/venv/Scripts/Activate.ps1

Install Dependencies:
pip install scrapy mysql mysql-connector-python

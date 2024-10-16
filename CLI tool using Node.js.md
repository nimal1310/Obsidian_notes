- Create a npm project using and create a folder and initialize using `npm init or npm init -y`
- There are some default package were available in node js for easy CLI tool development
	1. Commander - It allow us to set command ,options etc
	2. Chalk - It is used to add color to text ,options present in our tool
	3. conf - It save the information of user machine.[Code 2]
	4. yargs - Most of the cli get the user input throught command line arguments,for that `yargs` package will use. [Code 1]
	5. Boxen - It is used to add box in the tool [Code 1]
	6. Ora - spinner animation [code 3]
	7. Figlet - ASCII layout to text [code 3]

```bash
npm i commander chalk conf yargs boxen ora figlet
```


## Program file

1. npm init
2. Create a *bin* folder to save the entry point files.
3. Create *index.js* entry point file and save it under bin folder
4. Modify *package.json* file likewise as mentioned below

```bash
"bin":{
"tran":"./bin/index.js"
}
```

 - where tran is the command name being used in terminal
 5. Add code to index.js

```js
#! /usr/bin/env node
{.....}
```

- \ #! -> is shebang line for interpreter 
6. Add *utils.js* for functionalities to the tool and connect it with index.js
7. Install *global* package to run the command globally `npm install -g .` install it i root directory of project.


## Directory Structure

![[Pasted image 20240921140106.png]]

## Sampleco

1. [Sample 1 code](https://dev.to/rushankhan1/build-a-cli-with-node-js-4jbi)
2. [Sample 2 code](https://blog.logrocket.com/creating-a-cli-tool-with-node-js/)
3. [Sample 3 code ](https://egmz.medium.com/building-a-cli-with-node-js-in-2024-c278802a3ef5)

## Publication
- Publish the code in NPM as open source for  anyone to  access.
- Push to github as open source tool
- Create an exe file to run without node.js in any os platform.
--- 


### CS572-Homework-09-RAG

Provided is the `movies.json` file, which contains an array of movie name and description `{name: string, description: string}`.
1. Generate Embedding for each movie description `{name: string, description: string, embedding: number[]}`
2. Save the data in Atlas collection
3. Create a Vector Search Index for the collection and `embedding` field
4. Write a function to perform semantic vector search using the aggregation pipeline

Note: You may use `readline` core module to read input from the console:
```typescript
import readline from "node:readline/promises";

const readline_interface = readline.createInterface({ input: process.stdin, output: process.stdout });
const user_answer = await readline_interface.question('What is your name?');
if (user_answer === 'exit') process.exit(0);
```
Alternatively, you may use [readline-sync](https://www.npmjs.com/package/readline-sync).

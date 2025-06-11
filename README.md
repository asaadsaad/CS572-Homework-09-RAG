### CS572-Homework-09-RAG

The provided `movies.json` file contains an array of movie name and description `{name: string, description: string}`
1. Generate Embedding for each movie description `{name: string, description: string, embedding: number[]}`.
2. Save the data within a collection in MongoDB Atlas Cluster.
3. Create a Vector Search Index for the collection on the `embedding` field.
4. Write a function to perform semantic similarity vector search using the aggregation pipeline.

Note: You may use `readline` core module to read an input from the console as follows:
```typescript
import readline from "node:readline/promises";

const readline_interface = readline.createInterface({ input: process.stdin, output: process.stdout });
const user_answer = await readline_interface.question('What is your name?');
if (user_answer === 'exit') process.exit(0);
```

### CS572-Homework-09-RAG

The provided `menu.json` file contains an array of dishes `{ name: string, description: string }`
1. Generate Embedding for each dish description `{name: string, description: string, embedding: number[]}`.
2. Store the enriched documents in a MongoDB Atlas collection. 
3. Create a Vector Search Index for the collection on the `embedding` field.
4. Implement a function that performs semantic similarity search using MongoDB’s aggregation pipeline. For example, given a user query ("vegetarian spicy food")
   * Generate query embedding
   * Use $vectorSearch
   * Return top 5 most similar dishes with similarity score.

Note: You may use `readline` core module to read an input from the console as follows:
```typescript
import readline from "node:readline/promises";

const readline_interface = readline.createInterface({ input: process.stdin, output: process.stdout });
const user_answer = await readline_interface.question('What is your name?');
if (user_answer === 'exit') process.exit(0);
```

#### Optional Requirement
Create an AI agent capable of helping users find suitable receipes based on ingredients they currently have in their fridge. 

Write a function/tool `createRecipeAgent({ingredients: string[]})` that accepts a list of ingredients `["chicken", "rice", "broccoli"]`, convert the ingredient list into an embedding query and perform semantic vector search on the menu collection. Return the top most relevant recipe. 


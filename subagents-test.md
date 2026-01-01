# Parallel Claude Code Test

Launch 2 parallel `claude` instances, each performing a different coding task.

Each instance should:
1. Complete its assigned task
2. Write the generated code to its designated output file
3. console debug the full path to the output file
4. Verify that the output exists, return error if it does not exist
5. Exit when done

Note: each subagent should work in the same current folder and the output files should be stored in the same folder


## Tasks

### Instance 1 > Output: j:\work\projects\2026\subagents-test\subagent1.ts
Create a TypeScript function that validates email addresses using regex.
Include proper type annotations and JSDoc comments.

### Instance 2 > Output: j:\work\projects\2026\subagents-test\subagent2.ts
Create a TypeScript class `Queue<T>` that implements a generic FIFO queue.
Include methods: enqueue, dequeue, peek, isEmpty, size.


Report total execution time and success/failure of each.
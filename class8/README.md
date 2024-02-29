# Class 8 - Feb 29

[Lesson 8](./Lesson8.pdf)

[Homework 8](./Homework8.pdf)

---
```Script
nvm use v21.6.1
npm install -g zkapp-cli
#make sure the installed app is in the PATH
```

```Script
zk --version
# 0.17.2
```

```Script
zk example sudoku

⠋ Fetch project template...(node:92166) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
✔ Fetch project template
✔ Extract example
✔ Initialize Git repo
✔ NPM install
✔ Set project name
✔ Git init commit

Success!

Next steps:
  cd sudoku
  git remote add origin <your-repo-url>
  git push -u origin main

To run the example:
  cd sudoku
  npm run test
  npm run build
  npm run start

```

```Script
npm run test

> sudoku@0.1.0 test
> node --experimental-vm-modules node_modules/jest/bin/jest.js

(node:92302) ExperimentalWarning: VM Modules is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
(node:92302) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
 PASS  src/sudoku.test.ts (33.184 s)
  sudoku
    ✓ accepts a correct solution (19025 ms)
    ✓ rejects an incorrect solution (3480 ms)

Test Suites: 1 passed, 1 total
Tests:       2 passed, 2 total
Snapshots:   0 total
Time:        33.46 s
```

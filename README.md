# s2026-lab09

## Running

1. Follow the directions in the [lab instructions](https://github.com/CMU-17-214/s2026/blob/main/labs/lab09.md) to set up a Google Cloud Vision API account and ensure you are logged in
1. `npm i` (shorthand for `npm install`)
1. `npm run compile`
1. `npm run start`

If your environment is properly set up, you should get output similar to:

```bash
$ npm run start

> lab09@1.0.0 start
> node .

Running logo detection on ./images/cmu.jpg
Running logo detection on ./images/logo-types-collection.jpg
Running logo detection on ./images/not-a-file.jpg
(node:55481) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
File ./images/not-a-file.jpg not found
Error: mainAsync not implemented
    at mainAsync (file:///Users/hammada/cmu-17-214/s26-lab09/dist/index.js:55:19)
    at file:///Users/hammada/cmu-17-214/s26-lab09/dist/index.js:65:1
"Carnegie Mellon University" found in in file ./images/cmu.jpg
Average score for ./images/cmu.jpg: 0.8701951503753662
"Starbucks" found in in file ./images/logo-types-collection.jpg
"Gillette" found in in file ./images/logo-types-collection.jpg
"Durex" found in in file ./images/logo-types-collection.jpg
"CNN" found in in file ./images/logo-types-collection.jpg
"Martini Racing" found in in file ./images/logo-types-collection.jpg
"Revolut" found in in file ./images/logo-types-collection.jpg
Average score for ./images/logo-types-collection.jpg: 0.8582128485043844
```

## Async-ify-ing

Reimplement the Promise version of `main` as an async version (in `mainAsync`). Your version of the code should not use `.then` and it should use `try/catch` instead of `.catch`.

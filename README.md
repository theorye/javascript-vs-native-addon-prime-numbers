# Speed up your Node.js App with Native Addons. What’s faster, C++ or JavaScript?

This example compares JavaScript to C++ in Node.js for computing prime numbers. 

JavaScript is a ridiculously fast scripting language thanks to modern JavaScript engines. But how fast is JavaScript compared to C++? This repository contains an example that computes prime numbers in Node both with JavaScript and with a native C++ addon.


## Usage

```
git clone git@github.com:fhinkel/javascript-vs-native-addon-prime-numbers.git
npm install
npm start
```

Experiment with this example yourself. Just remember to run `npm install` to recompile the addon if you change any C++ code. 

## Results

**If your Node app’s sole purpose is to compute prime numbers and you don’t want to use a fast lookup table, please rely on this benchmark 100%. For anything else, this benchmark is probably useless.**

Both the JavaScript and the C++ implementation use the same algorithm. Calling into the addon and running the computations in C++ optimized with -Os is slightly faster than staying in JavaScript. Even for small numbers, using the C++ addon is faster than JavaScript.

![Up to 200th prime](https://fhinkel.github.io/javascript-vs-native-addon-prime-numbers/first200.png)

![Up to 1000000th prime](https://fhinkel.github.io/javascript-vs-native-addon-prime-numbers/first1000000.png)
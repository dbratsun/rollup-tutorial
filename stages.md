# stage 1

rollup src/main.js -o bundle.js -f cjs

# stage 2

rm bundle.js
rollup -c

# stage 3

rm bundle.js
npm install rollup --save-dev
npm rollup --config

add script in package.json:
{
    "scripts": {
        "build": "rollup --config"
    }
}

# stage 4

rm bundle.js
npm install --save-dev rollup-plugin-json
npm run build

# stage 5

rm bundle.js
npm install --save-dev rollup-plugin-terser
npm run build

# stage 6

rollup src/main.js -f cjs -d dist
rollup src/main.js src/main2.js -f cjs
rollup src/main.js src/main2.js -f cjs -d dist
rollup src/main.js src/main2.js -f esm -d dist

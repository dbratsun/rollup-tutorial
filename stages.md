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



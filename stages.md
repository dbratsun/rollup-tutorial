# stage 1

rollup src/main.js -o bundle.js -f cjs

# stage 2

rm bundle.js
rollup -c

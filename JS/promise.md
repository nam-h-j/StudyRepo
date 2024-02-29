```js
function timeout (funcName){
   console.log('run time out ', funcName)
}

function promise_before(funcName){
  return new Promise((resolve, reject) =>{
    setTimeout(() => {
      console.log(funcName)
      resolve('resolve from Promise_Before');
    },0);
  })
}

function promise_after(funcName){
  return new Promise((resolve, reject) =>{
    setTimeout(() => {
      console.log(funcName)
      resolve('resolve from Promise_After');
    },0);
  })
}

async function main (funcName){
  console.log('==========>>> run ', funcName)
  
  setTimeout(timeout(funcName), 1)

  const result_before = await promise_before(funcName);
  
  console.log(result_before)
  
  const result_after = await promise_after(funcName);
 
  console.log(result_after)
}

main('main1');
main('main2');
```

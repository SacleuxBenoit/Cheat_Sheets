# algo

## Bubble Sort

```
const arr = [3, 45, 67, 98, 78, 25, 17];

const bubbleSort = arr => {
  for (let i = 0; i < arr.length - 1; i++) {
    for (let j = 0; j < arr.length - (i + 1); j++) {
      if (arr[j] > arr[j + 1]) {
        [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
      }
    }
  }
  return arr;
};

bubbleSort(arr);

console.log(arr);
```
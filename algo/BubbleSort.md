# algo

## En quoi consite le tri à bulles ?
Le tri à bulles consiste à comparer répétitivement les éléments consécutifs d'un tableau et à les permuter lorsqu'ils sont mal triés, il dois son nom au faite qu'il déplace les plus grands éléments à la fin du tableau, comme des bulles d'air qui remonteraient à la surface d'un liquide.

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

Pratique : 

## Donne des nombres aléatoires entre 1 et 1000

```
 const BubbleSort = arr => {
            for (i = 0; i < arr.length - 1; i++) {
                for (j = 0; j < arr.length - (i + 1); j++) {
                    if (arr[j] > arr[j + 1]) {
                        [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]]
                    }
                }
            } return arr;
        };

        function RandomInt(min, max) {
            min = Math.ceil(min);
            max = Math.floor(max);
            return Math.floor(Math.random() * (max - min + 1)) + min;

        }

        const a = RandomInt(1, 1000);
        const b = RandomInt(1, 1000);
        const c = RandomInt(1, 1000);

        const arr = [a, b, c]



        BubbleSort(arr);
        console.log(arr);
```
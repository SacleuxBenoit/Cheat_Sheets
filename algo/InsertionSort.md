# algo

## C'est quoi le tri par insertion ?

Le tri par insertion est beaucoup plus lent que d'autres algorithmes comme le `quick sort` pour traiter des grandes séquences,
il est cependant considéré comme le tri le plus efficace sur des entrées de petite taille, il est aussi rapide quand les données sont déjà presque triées.

## InsertionSort

 arr = [4818, 4918, 11, 171, 1261]
        const insertionSort = arr => {
            const len = arr.length;
            for (let i = 0; i < len; i++) {
                let el = arr[i];
                let j;

                for (j = i - 1; j >= 0 && arr[j] > el; j--) {
                    arr[j + 1] = arr[j];
                }
                arr[j + 1] = el;
            }
            return arr;
        };
        insertionSort(arr);
        console.log(arr);

## Donne des nombres aléatoires entre 1 et 1000

const insertionSort = arr => {
            const len = arr.length;
            for (i = 0; i < len; i++) {
                let el = arr[i];
                for (j = i - 1; j >= 0 && arr[j] > el; j--) {
                    arr[j + 1] = arr[j];
                }
                arr[j + 1] = el;
            }
            return arr;
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

        insertionSort(arr);
        console.log(arr);
  
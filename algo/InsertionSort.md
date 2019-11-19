# algo

## InsertionSort
















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
    </script>
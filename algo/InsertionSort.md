# algo

## InsertionSort

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

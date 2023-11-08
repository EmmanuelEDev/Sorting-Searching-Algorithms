# Insertion Sort Procedure

This README provides an overview of the `insertion_sort` procedure, which is used to sort an array of integers using the insertion sort algorithm.

## Procedure Description

The `insertion_sort` procedure sorts an array of integers in ascending order using the insertion sort algorithm. It iterates through the array, comparing each element with the elements to its left, moving the element to its correct position within the sorted part of the array.

## Procedure Variables

- `arr`: An array of integers to be sorted.
- `i`, `j`: Integer variables used as loop counters.
- `key`: Integer variable used to store the current element being inserted into the sorted part of the array.

## Procedure Pseudocode

```pascal
VAR
    arr : ARRAY_OF INTEGER;
    i, j, key : INTEGER;
BEGIN
    FOR i FROM 1 TO LENGTH(arr) - 1 DO
        key := arr[i];
        j := i - 1;
        WHILE (j >= 0 AND arr[j] > key) DO
            arr[j + 1] := arr[j];
            j := j - 1;
        END_WHILE
        arr[j + 1] := key;
    END_FOR
END
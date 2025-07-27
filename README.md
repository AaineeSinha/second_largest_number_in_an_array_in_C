# second_largest_number_in_an_array_in_C
To find second largest element in c
#include <limits.h>  // for INT_MIN

int getSecondLargest(int *arr, int n) {
    int first = INT_MIN, second = INT_MIN;

    for (int i = 0; i < n; i++) {
        if (arr[i] > first) {
            second = first;
            first = arr[i];
        } else if (arr[i] > second && arr[i] != first) {
            second = arr[i];
        }
    }

    return (second == INT_MIN) ? -1 : second;
}

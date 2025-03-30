#include <iostream>
using namespace std;

// Bubble Sort Function
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
            }
        }
    }
}

// Print Array Function
void printArray(int arr[], int n) {
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
}

// Main Function
int main() {
    int n;
    cout << "Enter number of elements: ";
    cin >> n;

    int arr[100]; // Define a fixed size array
    cout << "Enter elements: ";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    // Call Bubble Sort
    bubbleSort(arr, n);
    cout << "Sorted Array using Bubble Sort: ";
    printArray(arr, n);

    return 0;
}


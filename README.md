#include <iostream>
#include <climits>  // For INT_MAX and INT_MIN
using namespace std;

int getmax(int num[], int n) {
    int max = INT_MIN;  // Initialize max to the smallest possible integer
    for (int i = 0; i < n; i++) {
        if (num[i] > max) {
            max = num[i];
        }
    }
    return max;
}

int getmin(int num[], int n) {
    int min = INT_MAX;  // Initialize min to the largest possible integer
    for (int i = 0; i < n; i++) {
        if (num[i] < min) {
            min = num[i];
        }
    }
    return min;
}

int main() {
    int n;
    cout << "Enter the number of elements: ";
    cin >> n;
    
    int num[100];  // Assuming the array can hold up to 100 elements
    cout << "Enter the elements of the array: ";
    for (int i = 0; i < n; i++) {
        cin >> num[i];
    }

    int max = getmax(num, n);
    int min = getmin(num, n);

    cout << "The maximum number is: " << max << endl;
    cout << "The minimum number is: " << min << endl;

    return 0;
}

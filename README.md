# array-deletion
#include <iostream>
using namespace std;

int main() {
    int arr[100], n, pos;

    cout << "Enter size: ";
    cin >> n;

    cout << "Enter " << n << " elements: ";
    for(int i=0; i<n; i++) cin >> arr[i];

    cout << "\nArray before deletion: ";
    for(int i=0; i<n; i++) cout << arr[i] << " ";

    cout << "\nEnter position to delete (0 to " << n-1 << "): ";
    cin >> pos;

    
    if(pos < 0 || pos >= n) {
        cout << "Invalid position!";
    } else {
        for(int i=pos; i<n-1; i++) {
            arr[i] = arr[i+1]; // shift left
        }
        n--; 

        cout << "Array after deletion: ";
        for(int i=0; i<n; i++) cout << arr[i] << " ";
    }
    return 0;
}

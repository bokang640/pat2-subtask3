# pat2-subtask3
#include <iostream>
#include <iomanip>
using namespace std;

const int NUM_EXPERIMENTS = 3;
const int NUM_READINGS = 3;

int main() {
    int i, j;
    double readingValue, total, average;

  for (i = 1; i <= NUM_EXPERIMENTS; i++) {
     total = 0; // Reset total for each experiment

   cout << "EXPERIMENT " << i << endl;
    cout << "=============\n";

  for (j = 1; j <= NUM_READINGS; j++) {
    cout << "Enter reading " << j << " value: ";
     cin >> readingValue; 
    total += readingValue; 
        }

average = total / NUM_READINGS; // Removed the nonsensical + total

   cout << "Experiment " << i << " average: ";
   cout << fixed << setprecision(2) << average;

  
   if (average < 100) {
  cout << " is Below acceptable range\n";
   } else if (average >= 100 && average <= 300) {
   cout << " is Within acceptable range\n";
   } else {
        cout << " is Above acceptable range\n";
   }
   }

    return 0;
}

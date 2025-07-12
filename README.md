# Number-Guessing-Game
# This is a simple console-based number guessing game written in C++. The computer randomly generates a number between 1 and 60 using rand(), and the player has to guess it.
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;
 
int main() {
    int guess;
    
    srand(time(0));
    int num = rand() % 60 + 1;
    
    cout<< "Guess the number (1 to 60): ";
    
    while (true) {
        cin >> guess;
        if (guess > num) { 
            cout << "Your guess is too high. Try again: ";
        } else if (guess < num) {
            cout << "Your guess is too low. Try again: ";
        } else {
            cout << "🎉 Congratulations! You guessed the correct number!" << endl;
            break;
        }
    }
    return 0;
}

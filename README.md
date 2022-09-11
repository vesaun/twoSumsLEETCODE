#include <iostream>
#include <string>
#include <array>

using namespace std;

int main()
{

    int input[7] = {1, 2, 3, 4, 5, 6, 7}; //example inputs
    int target = 9; //example target

    int inputLength = sizeof(input); //to get the length of the array

    for (int i = 0; i < inputLength - 1; i++) //iterate over the array
    {
        for (int j = i + 1; j < inputLength; j++) //iterate again, but one ahead of the first one so that we can check each possible set of options
        {
            if ((input[i] + input[j]) == target) //if the current number and the one ahead in the array equal the target...
            {
                int complement = target - input[i]; //if the complement to the target between input[i] and the target is true...

                if( input[j] == complement)
                {
                    cout << "In " << input << ", " << endl;
                    cout << "The target's sums are " << input[i] << " " << input[j] << endl; //print out these
                }
            }
        }
    }


    return 0;
}

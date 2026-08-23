# string-uppercase-lowecase-digit-count
#include <stdio.h>

int main() {
    char sentence[1000];
    int total_chars = 0;
    int uppercase = 0;
    int lowercase = 0;
    int digits = 0;
    int spaces = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);
    for (int i = 0; sentence[i] != '\0'; i++) 
    {
        if (sentence[i] == '\n') 
        {
            continue;
        }

        total_chars++; 
        if (sentence[i] >= 'A' && sentence[i] <= 'Z') 
        {
            uppercase++;
        }
        else if (sentence[i] >= 'a' && sentence[i] <= 'z')
        {
            lowercase++;
        }
        else if (sentence[i] >= '0' && sentence[i] <= '9') 
        {
            digits++;
        }
        else if (sentence[i] == ' ') 
        {
            spaces++;
        }
    }

    printf("Total characters: %d\n", total_chars);
    printf("Number of uppercase letters: %d\n", uppercase);
    printf("Number of lowercase letters: %d\n", lowercase);
    printf("Number of digits: %d\n", digits);
    printf("Number of spaces: %d\n", spaces);

    return 0;
}

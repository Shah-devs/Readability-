#include <cs50.h>
#include <stdio.h>
#include <ctype.h>
#include <string.h>
#include <math.h>

//prototypes
int count_letters(string x);
int count_words(string x);
int count_sentences(string x);
int main(void)
{
    string text = get_string("Text:  ");
    // printf("%s\n", text);

    // counting letters/printf functions to test the code
    int letters = count_letters(text);
    // printf("%i\n", letters);

    //counting words

    int words = count_words(text);
    // printf("%i\n", words);

    //counting sentences
    int sentences = count_sentences(text);
    // printf("%i\n", sentences);

    //puting the numbers in the US grading formula

    float index = (0.0588 * letters / words * 100) - (0.296 * sentences / words * 100) - 15.8;
    int Index = round(index);
    if (Index < 1)
    {
        printf("Before Grade 1\n");
    }
    else if (Index < 16)
    {
        printf("Grade %i\n", Index);
    }
    else
    {
        printf("Grade 16+\n");
    }

}


//functions defenitions
int count_letters(string x)
{
    int length = strlen(x);
    int l = 0;
    for (int i = 0; i < length; i++)
    {
        if(x[i] != '\0' && ((isalpha(x[i]))))
        {
            l++;
        }
    }
    return l;

}

int count_words(string x)
{
    int length = strlen(x);
    int w = 1;
    for (int i = 0; i < length; i++)
    {
        if (x[i] != '\0' && ((isspace(x[i])))  && (isalpha(x[i+1])))
        {
            w++;
        }
    }
    return w;

}
int count_sentences(string x)
{
    int length = strlen(x);
    int s = 0;
    for (int i = 0; i < length ; i++)
    {
        if(x[i] == '.'  || (x[i] == '!' && x[i-1] !='!')  || x[i] == '?')
        {
            s++;
        }
    }
    return s;
}

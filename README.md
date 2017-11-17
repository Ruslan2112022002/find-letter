# find-letter
#include "txlib.h"

int find_first_letter (char const data [], int const Size, char const word [], int wordlen);
int find_word (int letter_to_start, char const data [], char const word [], int Size);

int main ()

    {           //  0         1         2         3         4
                //  01234567890123456789012345678901234567890123456789
    char data [] = "lhloh,kmeowjbkgkiбmeowoaofo,euwpmeowtwophddfgilweg,op";
    char word [] = "meow";
    int Size = strlen (data);
    int wordlen = strlen (word);
    find_first_letter (data, Size, word, wordlen);
    }

int find_first_letter (char const data [], int const Size, char const word [], int wordlen)

    {

    for (int i = 0; i < Size; i ++)

        {

        if (data [i] == word [0])
            {

            int a = find_word ( i, data, word, Size);
            if (a = 1) printf ("%d - %d = meow\n", i, i + wordlen);
            }

        }

    }

int find_word (int letter_to_start, char const data [], char const word [], int Size)

    {

    for (int i = letter_to_start + 1; i < Size; i ++)

        {

        if (!data [i] == word [ i - letter_to_start] ) return 0;

        }

    return 1;

    }

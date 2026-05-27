# String Programs in C

## 1. Write a program to read a string and count the number of vowels using a separate function.

### Code
```c
#include <stdio.h>

void countVowels(char str[])
{
    int i, count = 0;

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i]=='a' || str[i]=='e' || str[i]=='i' || str[i]=='o' || str[i]=='u' ||
           str[i]=='A' || str[i]=='E' || str[i]=='I' || str[i]=='O' || str[i]=='U')
        {
            count++;
        }
    }

    printf("Number of vowels = %d", count);
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    countVowels(str);

    return 0;
}
```

### Output
<img width="1593" height="892" alt="image" src="https://github.com/user-attachments/assets/58ac39e7-b379-406d-9d9b-fe2f305cac33" />


## 2. Write a function to reverse a string without using library functions like strrev().

### Code
```c
#include <stdio.h>

void reverseString(char str[])
{
    int i, len = 0;
    char temp;

    while(str[len] != '\0')
    {
        len++;
    }

    for(i = 0; i < len/2; i++)
    {
        temp = str[i];
        str[i] = str[len-i-1];
        str[len-i-1] = temp;
    }

    printf("Reversed string: %s", str);
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    reverseString(str);

    return 0;
}
```

### Output
<img width="1338" height="880" alt="image" src="https://github.com/user-attachments/assets/2971ed5d-8186-4469-9378-bb1ce6e0653e" />


---

## 3. Write a program to check whether a given string is palindrome or not using functions.

### Code
```c
#include <stdio.h>

void palindrome(char str[])
{
    int i, len = 0, flag = 1;

    while(str[len] != '\0')
    {
        len++;
    }

    for(i = 0; i < len/2; i++)
    {
        if(str[i] != str[len-i-1])
        {
            flag = 0;
            break;
        }
    }

    if(flag)
        printf("Palindrome");
    else
        printf("Not a palindrome");
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    palindrome(str);

    return 0;
}
```

### Output
<img width="1223" height="815" alt="image" src="https://github.com/user-attachments/assets/7ac07976-4a13-479d-969a-bb9c94f87d15" />


---

## 4. Write a function to calculate the length of a string manually.

### Code
```c
#include <stdio.h>

int stringLength(char str[])
{
    int len = 0;

    while(str[len] != '\0')
    {
        len++;
    }

    return len;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    printf("Length of string = %d", stringLength(str));

    return 0;
}
```

### Output
<img width="1410" height="787" alt="image" src="https://github.com/user-attachments/assets/f7bff2c0-e46d-40bd-94d6-d0a14dc7650c" />

---

## 5. Write a function to count the number of words in a sentence.

### Code
```c
#include <stdio.h>

int countWords(char str[])
{
    int i, words = 1;

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] == ' ')
        {
            words++;
        }
    }

    return words;
}

int main()
{
    char str[100];

    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);

    printf("Number of words = %d", countWords(str));

    return 0;
}
```

### Output
<img width="1508" height="760" alt="image" src="https://github.com/user-attachments/assets/e5a462be-85dd-403f-b321-7fab99ca1509" />


---


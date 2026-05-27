# 27-5-2026-c-ass

1. Write a program to read a string and count the number of vowels using a separate function.
code:
```
#include <stdio.h>
int countVowels(char str[]) {
    int i = 0, count = 0;
    while(str[i] != '\0') {
        char ch = str[i];

        if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||
           ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U') {
            count++;
        }
        i++;
    }
    return count;
}
int main() {
    char str[100];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    printf("Number of vowels = %d", countVowels(str));
    return 0;
}
```
Output:
```
Enter a string: abc
Number of vowels = 1

=== Code Execution Successful ===
```

2. Write a function to reverse a string without using library functions like strrev().
code:
```
#include <stdio.h>
void reverse(char str[]) {
    int i, len = 0;
    char temp;
    while(str[len] != '\0')
        len++;
    len--;
    if(str[len] == '\n')
        len--;
    for(i = 0; i < len - i; i++) {
        temp = str[i];
        str[i] = str[len - i];
        str[len - i] = temp;
    }
}
int main() {
    char str[100];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    reverse(str);
    printf("Reversed string: %s", str);
    return 0;
}
```
output:
```
Enter a string: abc
Reversed string: cba


=== Code Execution Successful ===
```
3. Write a program to check whether a given string is palindrome or not using functions.
code:
```
#include <stdio.h>
int isPalindrome(char str[]) {
    int i, len = 0;
    while(str[len] != '\0')
        len++;
    len--;
    if(str[len] == '\n')
        len--;
    for(i = 0; i < len - i; i++) {
        if(str[i] != str[len - i])
            return 0;
    }
    return 1;
}
int main() {
    char str[100];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    if(isPalindrome(str))
        printf("Palindrome");
    else
        printf("Not Palindrome");
    return 0;
}
```
output:
```
Enter a string: abc
Not Palindrome

=== Code Execution Successful ===
```
4. Write a function to calculate the length of a string manually.
code:
```
#include <stdio.h>
int stringLength(char str[]) {
    int len = 0;
    while(str[len] != '\0')
        len++;
    return len;
}
int main() {
    char str[100];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    printf("Length = %d", stringLength(str) - 1);
    return 0;
}
```
output:
```
Enter a string: abc
Length = 3

=== Code Execution Successful ===
```
5. Write a function to count the number of words in a sentence.
code:
```
#include <stdio.h>
int countWords(char str[]) {
    int i = 0, words = 0;
    while(str[i] != '\0') {
        if(str[i] == ' ' || str[i] == '\n' || str[i] == '\t')
            words++;
        i++;
    }
    return words + 1;
}
int main() {
    char str[200];
    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);
    printf("Number of words = %d", countWords(str));
    return 0;
}
```
output:
```
Enter a sentence: rite a program to read a string and count the number of 




Number of words = 14

=== Code Execution Successful ===
```

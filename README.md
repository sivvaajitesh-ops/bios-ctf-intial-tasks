# bios-ctf-intial-tasks
1.
s = input()
i = 0

while i < len(s):
    if s[i:i+2] == "ox":
        print("1", end="")
        i += 2
    elif s[i:i+2] == "oo":
        print("2", end="")
        i += 2
    else:
        print("0", end="")
        i += 1
output: 
   xxoxoo
    0012
2.
   a = list(map(int, input().split()))
x = int(input())

for i in range(len(a)):
    for j in range(len(a)-1):
        if a[j] > a[j+1]:
            a[j], a[j+1] = a[j+1], a[j]

print(a)

if x in a:
    print(True)
else:
    print(False)

output:

7 8 9 1 7 8 3
3
[1, 3, 7, 7, 8, 8, 9]
True

3.
  s = input()

result = ""

for ch in s:
    if 'a' <= ch <= 'z':
        result += chr((ord(ch) - ord('a') + 2) % 26 + ord('a'))
    elif 'A' <= ch <= 'Z':
        result += chr((ord(ch) - ord('A') + 2) % 26 + ord('A'))
    else:
        result += ch

print(result)
 
  Input:  abc d1@
Output: cde f1@

4.
    s = input()

frequency = {}

for ch in s:
    if ch in frequency:
        frequency[ch] += 1
    else:
        frequency[ch] = 1

for ch in frequency:
    print(ch, ":", frequency[ch])

print(s[::-1])

output:
        xyzxyzxyzza
        x : 3
        y : 3
        z : 4
        a : 1
5.
#include <stdio.h>

int main()
{
    int n, sum = 0, digit;

    scanf("%d", &n);

    while (n > 0)
    {
        digit = n % 10;
        sum = sum + digit;
        n = n / 10;
    }

    printf("%d", sum);

    return 0;
}

output:
      123
      6

6.
#include <stdio.h>

int main()
{
    int n, a[100], i;
    int min, max;

    scanf("%d", &n);

    for(i = 0; i < n; i++)
    {
        scanf("%d", &a[i]);
    }

    min = a[0];
    max = a[0];

    for(i = 1; i < n; i++)
    {
        if(a[i] < min)
            min = a[i];

        if(a[i] > max)
            max = a[i];
    }

    printf("Minimum: %d\n", min);
    printf("Maximum: %d", max);

    return 0;
}
output:
     5
2 6 4 9 3
   Minimum: 2
Maximum: 9

7.
  #include <stdio.h>

int main()
{
    char s[100];
    int i, vowels = 0, consonants = 0;

    gets(s);

    for(i = 0; s[i] != '\0'; i++)
    {
        if(s[i] == 'a' || s[i] == 'e' || s[i] == 'i' ||
           s[i] == 'o' || s[i] == 'u' ||
           s[i] == 'A' || s[i] == 'E' || s[i] == 'I' ||
           s[i] == 'O' || s[i] == 'U')
        {
            vowels++;
        }
        else if((s[i] >= 'a' && s[i] <= 'z') ||
                (s[i] >= 'A' && s[i] <= 'Z'))
        {
            consonants++;
        }
    }

    printf("Vowels: %d\n", vowels);
    printf("Consonants: %d", consonants);

    return 0;
}
output: 
       bi0s CTF recruitment
  Vowels: 5
Consonants: 12
8.

#include <stdio.h>

int main()
{
    int n, i;
    int fact = 1;
    int *p = &n;

    scanf("%d", p);

    for (i = 1; i <= *p; i++)
    {
        fact = fact * i;
    }

    printf("Factorial: %d", fact);

    return 0;
}
 
output:

   5
factorial:120
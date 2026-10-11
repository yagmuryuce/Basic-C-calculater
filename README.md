# Basic-C-calculater
```
#include <stdio.h>

int main() {

    char operator;
    double num1;
    double num2;
    double result;
    char again;

    do {
        printf("\n Choose an operation (+, -, *, /): ");
        scanf(" %c", &operator);   
        printf("\n enter number 1 = ");
        scanf("%lf", &num1);
        printf("\n enter number 2 = ");
        scanf("%lf", &num2);

        switch(operator)
        {
            case '+':
                result = num1 + num2;
                printf("\n result = %.2lf", result);
                break;

            case '-':
                result = num1 - num2;
                printf("\n result = %.2lf", result);
                break;

            case '*':
                result = num1 * num2;
                printf("\n result = %.2lf", result);
                break;

            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    printf("\n result = %.2lf", result);
                } else {
                    printf("\n error! cannot divide by zero");
                }
                break;

            default:
                printf("\n %c error!", operator);
                break;
        }

        printf("\n\n Do you want to make another calculation? (y/n): ");
        scanf(" %c", &again);

    } while (again == 'y' || again == 'Y');

    return 0;
}


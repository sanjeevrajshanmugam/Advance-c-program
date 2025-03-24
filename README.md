# Advance-c-program stack

```
#include <stdio.h>
#include <string.h>
#define MAX 100
int studentNumber[MAX];
char name[MAX][50];
char department[MAX][50];
int top = -1;
int isEmpty();
int isFull();
void push(int num, char n[], char dept[]);
void pop();
void peek();
int main() {
    push(101, "HARISH", "AIDS");
    push(102, "SANJEEV", "IT");
    push(103, "SURYA PARAKASH", "CYBER SECURITY");

  
    peek();

   
    pop();

    
    peek();

    return 0;
}
int isEmpty() {
    return top == -1;
}

int isFull() {
    return top == MAX - 1;
}

void push(int num, char n[], char dept[]) {
    if (isFull()) {
        printf("Stack is full! Cannot push.\n");
        return;
    }
    top++;
    studentNumber[top] = num;
    strcpy(name[top], n);
    strcpy(department[top], dept);
    printf("Pushed: %d, %s, %s\n", num, n, dept);
}

void pop() {
    if (isEmpty()) {
        printf("Stack is empty! Cannot pop.\n");
        return;
    }
    printf("Popped: %d, %s, %s\n", studentNumber[top], name[top], department[top]);
    top--;
}
void peek() {
    if (isEmpty()) {
        printf("Stack is empty! Nothing to peek.\n");
        return;
    }
    printf("Peek -> %d, %s, %s\n", studentNumber[top], name[top], department[top]);
}

```


# OUTPUT

![Screenshot 2025-03-24 105617](https://github.com/user-attachments/assets/4a470faf-f47e-4a50-8012-a4635f4fd402)

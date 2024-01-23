# Lab1
Implement Matrix manipulation .
Consider the 2D representation for your chosen domain. Perform all data structure operations (insertion, Deletion, linear search) using 2D arrays for any chosen logical data of your domain. 
Implement any two matrix operations

### Code:
```
#include <stdio.h>

#define ROW 3
#define COL 3

// Function to display a matrix
void displayMatrix(int mat[ROW][COL]) {
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++) {
            printf("%d ", mat[i][j]);
        }
        printf("\n");
    }
}

// Function to insert elements into a matrix
void insertElement(int mat[ROW][COL], int row, int col, int value) {
    if (row >= 0 && row < ROW && col >= 0 && col < COL) {
        mat[row][col] = value;
        printf("Element inserted successfully.\n");
    } else {
        printf("Invalid position for insertion.\n");
    }
}

// Function to delete an element from a matrix
void deleteElement(int mat[ROW][COL], int row, int col) {
    if (row >= 0 && row < ROW && col >= 0 && col < COL) {
        mat[row][col] = 0;
        printf("Element deleted successfully.\n");
    } else {
        printf("Invalid position for deletion.\n");
    }
}

// Function for linear search in a matrix
void linearSearch(int mat[ROW][COL], int key) {
    int found = 0;
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++) {
            if (mat[i][j] == key) {
                printf("Element %d found at position [%d][%d]\n", key, i, j);
                found = 1;
            }
        }
    }
    if (!found) {
        printf("Element %d not found in the matrix.\n", key);
    }
}

// Function for matrix addition
void matrixAddition(int mat1[ROW][COL], int mat2[ROW][COL], int result[ROW][COL]) {
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++) {
            result[i][j] = mat1[i][j] + mat2[i][j];
        }
    }
}

// Function for matrix multiplication
void matrixMultiplication(int mat1[ROW][COL], int mat2[ROW][COL], int result[ROW][COL]) {
    int i, j, k;
    for (i = 0; i < ROW; i++) {
        for (j = 0; j < COL; j++) {
            result[i][j] = 0;
            for (k = 0; k < COL; k++) {
                result[i][j] += mat1[i][k] * mat2[k][j];
            }
        }
    }
}

int main() {
    int matrix1[ROW][COL] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int matrix2[ROW][COL] = {{9, 8, 7}, {6, 5, 4}, {3, 2, 1}};
    int resultMatrix[ROW][COL];

    printf("Matrix 1:\n");
    displayMatrix(matrix1);
    printf("\nMatrix 2:\n");
    displayMatrix(matrix2);

    // Insertion
    insertElement(matrix1, 1, 1, 10);
    printf("\nMatrix 1 after insertion:\n");
    displayMatrix(matrix1);

    // Deletion
    deleteElement(matrix2, 0, 2);
    printf("\nMatrix 2 after deletion:\n");
    displayMatrix(matrix2);

    // Linear search
    linearSearch(matrix1, 5);
    linearSearch(matrix2, 11);

    // Matrix addition
    matrixAddition(matrix1, matrix2, resultMatrix);
    printf("\nMatrix Addition Result:\n");
    displayMatrix(resultMatrix);

    // Matrix multiplication
    matrixMultiplication(matrix1, matrix2, resultMatrix);
    printf("\nMatrix Multiplication Result:\n");
    displayMatrix(resultMatrix);

    return 0;
}
```


# Matrix Operations
```
#include <stdio.h>

#define ROW 3
#define COL 3

// Function to display a matrix
void displayMatrix(int mat[ROW][COL]) {
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++) {
            printf("%d ", mat[i][j]);
        }
        printf("\n");
    }
}

// Function to insert elements into a matrix
void insertElement(int mat[ROW][COL], int row, int col, int value) {
    if (row >= 0 && row < ROW && col >= 0 && col < COL) {
        mat[row][col] = value;
        printf("Element inserted successfully.\n");
    } else {
        printf("Invalid position for insertion.\n");
    }
}

// Function to delete an element from a matrix
void deleteElement(int mat[ROW][COL], int row, int col) {
    if (row >= 0 && row < ROW && col >= 0 && col < COL) {
        mat[row][col] = 0;
        printf("Element deleted successfully.\n");
    } else {
        printf("Invalid position for deletion.\n");
    }
}

// Function for linear search in a matrix
void linearSearch(int mat[ROW][COL], int key) {
    int found = 0;
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++) {
            if (mat[i][j] == key) {
                printf("Element %d found at position [%d][%d]\n", key, i, j);
                found = 1;
            }
        }
    }
    if (!found) {
        printf("Element %d not found in the matrix.\n", key);
    }
}

// Function for matrix addition
void matrixAddition(int mat1[ROW][COL], int mat2[ROW][COL], int result[ROW][COL]) {
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++) {
            result[i][j] = mat1[i][j] + mat2[i][j];
        }
    }
}

// Function for matrix multiplication
void matrixMultiplication(int mat1[ROW][COL], int mat2[ROW][COL], int result[ROW][COL]) {
    int i, j, k;
    for (i = 0; i < ROW; i++) {
        for (j = 0; j < COL; j++) {
            result[i][j] = 0;
            for (k = 0; k < COL; k++) {
                result[i][j] += mat1[i][k] * mat2[k][j];
            }
        }
    }
}

int main() {
    int matrix1[ROW][COL] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int matrix2[ROW][COL] = {{9, 8, 7}, {6, 5, 4}, {3, 2, 1}};
    int resultMatrix[ROW][COL];

    printf("Matrix 1:\n");
    displayMatrix(matrix1);
    printf("\nMatrix 2:\n");
    displayMatrix(matrix2);

    // Insertion
    insertElement(matrix1, 1, 1, 10);
    printf("\nMatrix 1 after insertion:\n");
    displayMatrix(matrix1);

    // Deletion
    deleteElement(matrix2, 0, 2);
    printf("\nMatrix 2 after deletion:\n");
    displayMatrix(matrix2);

    // Linear search
    linearSearch(matrix1, 5);
    linearSearch(matrix2, 11);

    // Matrix addition
    matrixAddition(matrix1, matrix2, resultMatrix);
    printf("\nMatrix Addition Result:\n");
    displayMatrix(resultMatrix);

    // Matrix multiplication
    matrixMultiplication(matrix1, matrix2, resultMatrix);
    printf("\nMatrix Multiplication Result:\n");
    displayMatrix(resultMatrix);

    return 0;
}
```

# Lab 2
Implement linked list and its operations
Consider each node as structure representation of data  for your domain. Perform all operations and implement different types of linked list

### Code:
```
#include <stdio.h>
#include <stdlib.h>

// Structure for a node in the linked list
struct Node {
    int data;
    struct Node* next;
};

// Function to create a new node
struct Node* createNode(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    if (newNode == NULL) {
        printf("Memory allocation failed.\n");
        exit(1);
    }
    newNode->data = value;
    newNode->next = NULL;
    return newNode;
}

// Function to insert a node at the beginning of the linked list
void insertAtBeginning(struct Node** headRef, int value) {
    struct Node* newNode = createNode(value);
    newNode->next = *headRef;
    *headRef = newNode;
    printf("Node inserted at the beginning successfully.\n");
}

// Function to insert a node at the end of the linked list
void insertAtEnd(struct Node** headRef, int value) {
    struct Node* newNode = createNode(value);
    struct Node* temp = *headRef;

    if (*headRef == NULL) {
        *headRef = newNode;
        printf("Node inserted at the end successfully.\n");
        return;
    }

    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = newNode;
    printf("Node inserted at the end successfully.\n");
}

// Function to delete a node by value from the linked list
void deleteNode(struct Node** headRef, int value) {
    struct Node* temp = *headRef;
    struct Node* prev = NULL;

    if (temp != NULL && temp->data == value) {
        *headRef = temp->next;
        free(temp);
        printf("Node with value %d deleted successfully.\n", value);
        return;
    }

    while (temp != NULL && temp->data != value) {
        prev = temp;
        temp = temp->next;
    }

    if (temp == NULL) {
        printf("Node with value %d not found in the list.\n", value);
        return;
    }

    prev->next = temp->next;
    free(temp);
    printf("Node with value %d deleted successfully.\n", value);
}

// Function to display the linked list
void displayList(struct Node* head) {
    if (head == NULL) {
        printf("Linked list is empty.\n");
        return;
    }

    printf("Linked list elements: ");
    while (head != NULL) {
        printf("%d ", head->data);
        head = head->next;
    }
    printf("\n");
}

int main() {
    struct Node* head = NULL;

    // Inserting nodes
    insertAtEnd(&head, 5);
    insertAtBeginning(&head, 10);
    insertAtEnd(&head, 15);
    insertAtEnd(&head, 20);

    // Displaying nodes
    displayList(head);

    // Deleting nodes
    deleteNode(&head, 15);
    deleteNode(&head, 10);

    // Displaying updated list
    displayList(head);

    return 0;
}
```


# Lab 3
Application of Stack (convert an infix expression to the postfix form and evaluation of postfix expression) 
Input must be given as an expression using scanf function
Consider any relavant computation to your domain

```
### Code
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>

#define MAX_SIZE 100

// Structure for the stack
struct Stack {
    int top;
    unsigned capacity;
    int* array;
};

// Function to create a stack
struct Stack* createStack(unsigned capacity) {
    struct Stack* stack = (struct Stack*)malloc(sizeof(struct Stack));
    if (!stack) return NULL;
    stack->top = -1;
    stack->capacity = capacity;
    stack->array = (int*)malloc(stack->capacity * sizeof(int));
    if (!stack->array) return NULL;
    return stack;
}

// Function to check if the stack is full
int isFull(struct Stack* stack) {
    return stack->top == stack->capacity - 1;
}

// Function to check if the stack is empty
int isEmpty(struct Stack* stack) {
    return stack->top == -1;
}

// Function to push an element onto the stack
void push(struct Stack* stack, int item) {
    if (isFull(stack)) return;
    stack->array[++stack->top] = item;
}

// Function to pop an element from the stack
int pop(struct Stack* stack) {
    if (isEmpty(stack)) return -1;
    return stack->array[stack->top--];
}

// Function to return the top element of the stack
int peek(struct Stack* stack) {
    if (isEmpty(stack)) return -1;
    return stack->array[stack->top];
}

// Function to check if the character is an operator
int isOperator(char ch) {
    return (ch == '+' || ch == '-' || ch == '*' || ch == '/' || ch == '^');
}

// Function to get the precedence of the operator
int precedence(char ch) {
    if (ch == '^')
        return 3;
    else if (ch == '*' || ch == '/')
        return 2;
    else if (ch == '+' || ch == '-')
        return 1;
    else
        return -1;
}

// Function to convert infix expression to postfix
void infixToPostfix(char* infix, char* postfix) {
    struct Stack* stack = createStack(MAX_SIZE);
    int i, j;
    i = j = 0;

    while (infix[i] != '\0') {
        if (isdigit(infix[i])) {
            postfix[j++] = infix[i++];
        } else if (infix[i] == '(') {
            push(stack, infix[i++]);
        } else if (infix[i] == ')') {
            while (!isEmpty(stack) && peek(stack) != '(') {
                postfix[j++] = pop(stack);
            }
            if (!isEmpty(stack) && peek(stack) != '(') {
                printf("Invalid expression.\n");
                return;
            } else {
                pop(stack);
            }
            i++;
        } else if (isOperator(infix[i])) {
            while (!isEmpty(stack) && precedence(infix[i]) <= precedence(peek(stack))) {
                postfix[j++] = pop(stack);
            }
            push(stack, infix[i++]);
        } else {
            printf("Invalid character in the expression.\n");
            return;
        }
    }

    while (!isEmpty(stack)) {
        postfix[j++] = pop(stack);
    }
    postfix[j] = '\0';
}

// Function to evaluate the postfix expression
int evaluatePostfix(char* postfix) {
    struct Stack* stack = createStack(MAX_SIZE);
    int i, operand1, operand2, result;

    for (i = 0; postfix[i] != '\0'; i++) {
        if (isdigit(postfix[i])) {
            push(stack, postfix[i] - '0');
        } else {
            operand2 = pop(stack);
            operand1 = pop(stack);

            switch (postfix[i]) {
                case '+':
                    push(stack, operand1 + operand2);
                    break;
                case '-':
                    push(stack, operand1 - operand2);
                    break;
                case '*':
                    push(stack, operand1 * operand2);
                    break;
                case '/':
                    push(stack, operand1 / operand2);
                    break;
                case '^':
                    result = 1;
                    for (int j = 0; j < operand2; j++) {
                        result *= operand1;
                    }
                    push(stack, result);
                    break;
            }
        }
    }
    return pop(stack);
}

int main() {
    char infix[MAX_SIZE], postfix[MAX_SIZE];

    printf("Enter an infix expression: ");
    scanf("%s", infix);

    infixToPostfix(infix, postfix);
    printf("Postfix expression: %s\n", postfix);

    int result = evaluatePostfix(postfix);
    printf("Result after evaluation: %d\n", result);

    return 0;
}
```

# Lab 4
Implement Queue Operations and  types  using Linked List using your domain name  with the guidelines as already mentioned

```
### Code
#include <stdio.h>
#include <stdlib.h>

// Structure for a node in the queue (representing a vehicle)
struct Vehicle {
    int vehicleID; // Example: Vehicle ID
    char model[20]; // Example: Vehicle Model
    struct Vehicle* next;
};

// Structure for the Queue
struct Queue {
    struct Vehicle *front, *rear;
};

// Function to create a new vehicle node
struct Vehicle* createVehicle(int vehicleID, const char* model) {
    struct Vehicle* newVehicle = (struct Vehicle*)malloc(sizeof(struct Vehicle));
    if (newVehicle == NULL) {
        printf("Memory allocation failed.\n");
        exit(1);
    }
    newVehicle->vehicleID = vehicleID;
    strncpy(newVehicle->model, model, sizeof(newVehicle->model));
    newVehicle->next = NULL;
    return newVehicle;
}

// Function to create an empty queue
struct Queue* createQueue() {
    struct Queue* queue = (struct Queue*)malloc(sizeof(struct Queue));
    if (queue == NULL) {
        printf("Memory allocation failed.\n");
        exit(1);
    }
    queue->front = queue->rear = NULL;
    return queue;
}

// Function to check if the queue is empty
int isEmpty(struct Queue* queue) {
    return (queue->front == NULL);
}

// Function to enqueue (add) a vehicle to the queue
void enqueue(struct Queue* queue, int vehicleID, const char* model) {
    struct Vehicle* newVehicle = createVehicle(vehicleID, model);

    if (isEmpty(queue)) {
        queue->front = queue->rear = newVehicle;
    } else {
        queue->rear->next = newVehicle;
        queue->rear = newVehicle;
    }
    printf("Vehicle with ID %d and model %s enqueued successfully.\n", vehicleID, model);
}

// Function to dequeue (remove) a vehicle from the queue
void dequeue(struct Queue* queue) {
    if (isEmpty(queue)) {
        printf("Queue is empty. Cannot dequeue.\n");
        return;
    }

    struct Vehicle* temp = queue->front;
    queue->front = queue->front->next;

    if (queue->front == NULL) {
        queue->rear = NULL;
    }

    free(temp);
    printf("Vehicle dequeued successfully.\n");
}

// Function to display the vehicles in the queue
void displayQueue(struct Queue* queue) {
    if (isEmpty(queue)) {
        printf("Queue is empty.\n");
        return;
    }

    struct Vehicle* temp = queue->front;
    printf("Vehicles in the queue:\n");
    while (temp != NULL) {
        printf("Vehicle ID: %d, Model: %s\n", temp->vehicleID, temp->model);
        temp = temp->next;
    }
}

int main() {
    struct Queue* vehicleQueue = createQueue();

    enqueue(vehicleQueue, 1001, "Sedan");
    enqueue(vehicleQueue, 1002, "SUV");
    enqueue(vehicleQueue, 1003, "Hatchback");

    displayQueue(vehicleQueue);

    dequeue(vehicleQueue);
    displayQueue(vehicleQueue);

    dequeue(vehicleQueue);
    dequeue(vehicleQueue);
    displayQueue(vehicleQueue);

    dequeue(vehicleQueue); // Trying to dequeue when the queue is empty

    return 0;
}
```


# Singly Linked List with insertion at beginning, middle and end
```
### Code:
#include <stdio.h>
#include <stdlib.h>

// Node structure for the Linked List
struct Node {
    int data;
    struct Node* next;
};

// Function to create a new node
struct Node* createNode(int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    if (newNode == NULL) {
        printf("Memory allocation failed!\n");
        exit(EXIT_FAILURE);
    }
    newNode->data = data;
    newNode->next = NULL;
    return newNode;
}

// Function to insert a node at the beginning of the Linked List
void insertAtBeginning(struct Node** head, int data) {
    struct Node* newNode = createNode(data);
    newNode->next = *head;
    *head = newNode;
}

// Function to insert a node at the middle of the Linked List
void insertAtMiddle(struct Node* prevNode, int data) {
    if (prevNode == NULL) {
        printf("Previous node cannot be NULL for insertion in the middle!\n");
        return;
    }
    struct Node* newNode = createNode(data);
    newNode->next = prevNode->next;
    prevNode->next = newNode;
}

// Function to insert a node at the end of the Linked List
void insertAtEnd(struct Node** head, int data) {
    struct Node* newNode = createNode(data);
    struct Node* last = *head;

    if (*head == NULL) {
        *head = newNode;
        return;
    }

    while (last->next != NULL) {
        last = last->next;
    }

    last->next = newNode;
}

// Function to print the Linked List
void printList(struct Node* head) {
    while (head != NULL) {
        printf("%d -> ", head->data);
        head = head->next;
    }
    printf("NULL\n");
}

// Function to free memory allocated for the Linked List
void freeList(struct Node* head) {
    struct Node* temp;
    while (head != NULL) {
        temp = head;
        head = head->next;
        free(temp);
    }
}

// Main function to demonstrate the usage of Linked List
int main() {
    struct Node* head = NULL;

    // Inserting nodes
    insertAtEnd(&head, 1);
    insertAtBeginning(&head, 2);
    insertAtBeginning(&head, 3);
    insertAtEnd(&head, 4);
    insertAtMiddle(head->next, 5);

    // Printing the Linked List
    printf("Linked List: ");
    printList(head);

    // Freeing memory allocated for the Linked List
    freeList(head);

    return 0;
}
```

# Doubly Linked List with insertion at beginning, middle and end
```
### Code
#include <stdio.h>
#include <stdlib.h>

// Node structure for the Doubly Linked List
struct Node {
    int data;
    struct Node* prev;
    struct Node* next;
};

// Function to create a new node
struct Node* createNode(int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    if (newNode == NULL) {
        printf("Memory allocation failed!\n");
        exit(EXIT_FAILURE);
    }
    newNode->data = data;
    newNode->prev = NULL;
    newNode->next = NULL;
    return newNode;
}

// Function to insert a node at the beginning of the Doubly Linked List
void insertAtBeginning(struct Node** head, int data) {
    struct Node* newNode = createNode(data);
    if (*head == NULL) {
        *head = newNode;
    } else {
        newNode->next = *head;
        (*head)->prev = newNode;
        *head = newNode;
    }
}

// Function to insert a node at the middle of the Doubly Linked List
void insertAtMiddle(struct Node* prevNode, int data) {
    if (prevNode == NULL) {
        printf("Previous node cannot be NULL for insertion in the middle!\n");
        return;
    }
    struct Node* newNode = createNode(data);
    newNode->prev = prevNode;
    newNode->next = prevNode->next;
    if (prevNode->next != NULL) {
        prevNode->next->prev = newNode;
    }
    prevNode->next = newNode;
}

// Function to insert a node at the end of the Doubly Linked List
void insertAtEnd(struct Node** head, int data) {
    struct Node* newNode = createNode(data);
    struct Node* last = *head;

    if (*head == NULL) {
        *head = newNode;
        return;
    }

    while (last->next != NULL) {
        last = last->next;
    }

    last->next = newNode;
    newNode->prev = last;
}

// Function to print the Doubly Linked List forward
void printForward(struct Node* head) {
    printf("Forward: ");
    while (head != NULL) {
        printf("%d -> ", head->data);
        head = head->next;
    }
    printf("NULL\n");
}

// Function to print the Doubly Linked List backward
void printBackward(struct Node* head) {
    struct Node* last = head;
    if (head == NULL) {
        printf("Backward: NULL\n");
        return;
    }

    while (last->next != NULL) {
        last = last->next;
    }

    printf("Backward: ");
    while (last != NULL) {
        printf("%d -> ", last->data);
        last = last->prev;
    }
    printf("NULL\n");
}

// Function to free memory allocated for the Doubly Linked List
void freeList(struct Node* head) {
    struct Node* temp;
    while (head != NULL) {
        temp = head;
        head = head->next;
        free(temp);
    }
}

// Main function to demonstrate the usage of Doubly Linked List
int main() {
    struct Node* head = NULL;

    // Inserting nodes
    insertAtEnd(&head, 1);
    insertAtBeginning(&head, 2);
    insertAtBeginning(&head, 3);
    insertAtEnd(&head, 4);
    insertAtMiddle(head->next, 5);

    // Printing the Doubly Linked List in forward and backward directions
    printForward(head);
    printBackward(head);

    // Freeing memory allocated for the Doubly Linked List
    freeList(head);

    return 0;
}
```

# Circular Linked List with insertion at beginning, middle and end
### Code
```
#include <stdio.h>
#include <stdlib.h>

// Node structure for the Circular Linked List
struct Node {
    int data;
    struct Node* next;
};

// Function to create a new node
struct Node* createNode(int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    if (newNode == NULL) {
        printf("Memory allocation failed!\n");
        exit(EXIT_FAILURE);
    }
    newNode->data = data;
    newNode->next = NULL;
    return newNode;
}

// Function to insert a node at the beginning of the Circular Linked List
void insertAtBeginning(struct Node** head, int data) {
    struct Node* newNode = createNode(data);
    if (*head == NULL) {
        newNode->next = newNode; // Point to itself to create a circular link
        *head = newNode;
    } else {
        struct Node* temp = *head;
        while (temp->next != *head) {
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->next = *head;
        *head = newNode;
    }
}

// Function to insert a node at the middle of the Circular Linked List
void insertAtMiddle(struct Node* head, int data) {
    if (head == NULL) {
        printf("List is empty, cannot insert in the middle!\n");
        return;
    }
    struct Node* slow = head;
    struct Node* fast = head->next;

    while (fast != head && fast->next != head) {
        slow = slow->next;
        fast = fast->next->next;
    }

    struct Node* newNode = createNode(data);
    newNode->next = slow->next;
    slow->next = newNode;
}

// Function to insert a node at the end of the Circular Linked List
void insertAtEnd(struct Node** head, int data) {
    struct Node* newNode = createNode(data);
    if (*head == NULL) {
        newNode->next = newNode; // Point to itself to create a circular link
        *head = newNode;
    } else {
        struct Node* temp = *head;
        while (temp->next != *head) {
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->next = *head;
    }
}

// Function to print the Circular Linked List
void printList(struct Node* head) {
    struct Node* temp = head;
    if (head != NULL) {
        do {
            printf("%d -> ", temp->data);
            temp = temp->next;
        } while (temp != head);
        printf("Circular\n");
    } else {
        printf("List is empty\n");
    }
}

// Function to free memory allocated for the Circular Linked List
void freeList(struct Node* head) {
    if (head != NULL) {
        struct Node* temp = head;
        struct Node* current = head;
        do {
            current = temp->next;
            free(temp);
            temp = current;
        } while (temp != head);
    }
}

// Main function to demonstrate the usage of Circular Linked List
int main() {
    struct Node* head = NULL;

    // Inserting nodes
    insertAtEnd(&head, 1);
    insertAtBeginning(&head, 2);
    insertAtBeginning(&head, 3);
    insertAtEnd(&head, 4);
    insertAtMiddle(head, 5);

    // Printing the Circular Linked List
    printf("Circular Linked List: ");
    printList(head);

    // Freeing memory allocated for the Circular Linked List
    freeList(head);

    return 0;
}
```

# Lab 5
Implementation of Linear and Binary Search
Include the following::
1. Implement Linear, sentinel and binary search. 
2. Search for any two data types.
3. implement bubble and insertion sort before using binary search. Compute the total number of comparisons, data transfer operations for each sort.
4. calculate the element comparisons, index comparisons for linear search, sentinel and binary search.

### Code
```
#include <stdio.h>

int linearSearch(int arr[], int n, int key)
{
    int comparisons = 0;
    for (int i = 0; i < n; i++)
    {
        comparisons++;
        if (arr[i] == key)
        {
            return comparisons;
        }
    }
    return comparisons;
}

int sentinelSearch(int arr[], int n, int key)
{
    int last = arr[n - 1];
    arr[n - 1] = key;
    int i = 0;
    while (arr[i] != key)
    {
        i++;
    }
    arr[n - 1] = last;
    if (i < n - 1 || arr[n - 1] == key)
    {
        return i + 1;
    }
    return -1;
}

int binarySearch(int arr[], int low, int high, int key)
{
    int comparisons = 0;
    while (low <= high)
    {
        int mid = low + (high - low) / 2;
        comparisons++;
        if (arr[mid] == key)
        {
            return comparisons;
        }
        if (arr[mid] < key)
        {
            low = mid + 1;
        }
        else
        {
            high = mid - 1;
        }
    }
    return comparisons;
}

void bubbleSort(int arr[], int n, int *comparisons, int *dataTransfers)
{
    for (int i = 0; i < n - 1; i++)
    {
        for (int j = 0; j < n - i - 1; j++)
        {
            (*comparisons)++;
            if (arr[j] > arr[j + 1])
            {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                (*dataTransfers)++;
            }
        }
    }
}

void insertionSort(int arr[], int n, int *comparisons, int *dataTransfers)
{
    for (int i = 1; i < n; i++)
    {
        int key = arr[i];
        int j = i - 1;
        (*dataTransfers)++;
        while (j >= 0 && arr[j] > key)
        {
            (*comparisons)++;
            arr[j + 1] = arr[j];
            (*dataTransfers)++;
            j--;
        }
        arr[j + 1] = key;
        (*dataTransfers)++;
    }
}

int main()
{
    int arr[] = {5, 2, 8, 12, 3};
    int n = sizeof(arr) / sizeof(arr[0]);
    int key = 8;

    int bubbleComparisons = 0;
    int bubbleDataTransfers = 0;
    bubbleSort(arr, n, &bubbleComparisons, &bubbleDataTransfers);

    int insertionComparisons = 0;
    int insertionDataTransfers = 0;
    insertionSort(arr, n, &insertionComparisons, &insertionDataTransfers);

    int linearComparisons = linearSearch(arr, n, key);

    int sentinelComparisons = sentinelSearch(arr, n, key);

    int binaryComparisons = binarySearch(arr, 0, n - 1, key);

    printf("Bubble Sort Comparisons: %d\n", bubbleComparisons);
    printf("Bubble Sort Data Transfers: %d\n", bubbleDataTransfers);
    printf("Insertion Sort Comparisons: %d\n", insertionComparisons);
    printf("Insertion Sort Data Transfers: %d\n", insertionDataTransfers);
    printf("Linear Search Comparisons: %d\n", linearComparisons);
    printf("Sentinel Search Comparisons: %d\n", sentinelComparisons);
    printf("Binary Search Comparisons: %d\n", binaryComparisons);

    return 0;
}
```

# Lab 6
Implement Merge sort (or) Quick sort in your domain.
1. Use Rand method to generate for numerical data.
2. Perform Read and Write Operations in files using structures.   
3. comparison of any two sorting techniques with respect to number of comparisons and data transfer operations
```
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

typedef struct
{
    int ticketNumber;
} Ticket;

typedef struct
{
    int comparisons;
    int dataTransfers;
} SortingStats;

void swap(Ticket *a, Ticket *b, SortingStats *stats)
{
    Ticket temp = *a;
    *a = *b;
    *b = temp;
    stats->dataTransfers++;
}

int generateRandomTicketNumber()
{
    return rand() % 1000;
}

void createTicketsFile(const char *fileName, int numOfTickets)
{
    FILE *file = fopen(fileName, "w");
    srand(time(NULL));

    for (int i = 0; i < numOfTickets; i++)
    {
        int randomTicketNumber = generateRandomTicketNumber();
        fprintf(file, "%d\n", randomTicketNumber);
    }

    fclose(file);
}

void readTicketsFromFile(const char *fileName, Ticket tickets[], int *numOfTickets)
{
    FILE *file = fopen(fileName, "r");
    if (file == NULL)
    {
        printf("Error opening file.\n");
        exit(1);
    }

    int index = 0;
    while (fscanf(file, "%d", &tickets[index].ticketNumber) != EOF)
    {
        index++;
    }
    *numOfTickets = index;

    fclose(file);
}

void writeTicketsToFile(const char *fileName, Ticket tickets[], int numOfTickets)
{
    FILE *file = fopen(fileName, "w");
    if (file == NULL)
    {
        printf("Error opening file.\n");
        exit(1);
    }

    for (int i = 0; i < numOfTickets; i++)
    {
        fprintf(file, "%d\n", tickets[i].ticketNumber);
    }

    fclose(file);
}

void merge(Ticket tickets[], int left, int mid, int right, SortingStats *stats)
{
    int n1 = mid - left + 1;
    int n2 = right - mid;

    Ticket L[n1], R[n2];

    for (int i = 0; i < n1; i++)
        L[i] = tickets[left + i];
    for (int j = 0; j < n2; j++)
        R[j] = tickets[mid + 1 + j];

    int i = 0, j = 0, k = left;
    while (i < n1 && j < n2)
    {
        stats->comparisons++;
        if (L[i].ticketNumber <= R[j].ticketNumber)
        {
            tickets[k] = L[i];
            i++;
        }
        else
        {
            tickets[k] = R[j];
            j++;
        }
        k++;
        stats->dataTransfers++;
    }

    while (i < n1)
    {
        tickets[k] = L[i];
        i++;
        k++;
        stats->dataTransfers++;
    }

    while (j < n2)
    {
        tickets[k] = R[j];
        j++;
        k++;
        stats->dataTransfers++;
    }
}

void mergeSort(Ticket tickets[], int left, int right, SortingStats *stats)
{
    if (left < right)
    {
        int mid = left + (right - left) / 2;

        mergeSort(tickets, left, mid, stats);
        mergeSort(tickets, mid + 1, right, stats);

        merge(tickets, left, mid, right, stats);
    }
}

int partition(Ticket tickets[], int low, int high, SortingStats *stats)
{
    int pivot = tickets[high].ticketNumber;
    int i = low - 1;

    for (int j = low; j <= high - 1; j++)
    {
        stats->comparisons++;
        if (tickets[j].ticketNumber < pivot)
        {
            i++;
            swap(&tickets[i], &tickets[j], stats);
        }
    }
    swap(&tickets[i + 1], &tickets[high], stats);
    return (i + 1);
}

void quickSort(Ticket tickets[], int low, int high, SortingStats *stats)
{
    if (low < high)
    {
        int pi = partition(tickets, low, high, stats);

        quickSort(tickets, low, pi - 1, stats);
        quickSort(tickets, pi + 1, high, stats);
    }
}

int main()
{
    const char *initialFileName = "initial_tickets.txt";
    const char *mergeSortFileName = "merge_sort_tickets.txt";
    const char *quickSortFileName = "quick_sort_tickets.txt";
    int numOfTickets = 20;

    createTicketsFile(initialFileName, numOfTickets);

    Ticket tickets[numOfTickets];
    readTicketsFromFile(initialFileName, tickets, &numOfTickets);

    printf("Unsorted Tickets:\n");
    for (int i = 0; i < numOfTickets; i++)
    {
        printf("%d ", tickets[i].ticketNumber);
    }
    printf("\n\n");

    SortingStats mergeSortStats = {0, 0};
    SortingStats quickSortStats = {0, 0};

    Ticket mergeSortTickets[numOfTickets];
    for (int i = 0; i < numOfTickets; i++)
    {
        mergeSortTickets[i] = tickets[i];
    }
    mergeSort(mergeSortTickets, 0, numOfTickets - 1, &mergeSortStats);

    writeTicketsToFile(mergeSortFileName, mergeSortTickets, numOfTickets);
    printf("Tickets after Merge Sort have been written to %s\n", mergeSortFileName);
    printf("Merge Sort Comparisons: %d\n", mergeSortStats.comparisons);
    printf("Merge Sort Data Transfers: %d\n\n", mergeSortStats.dataTransfers);

    Ticket quickSortTickets[numOfTickets];
    for (int i = 0; i < numOfTickets; i++)
    {
        quickSortTickets[i] = tickets[i];
    }
    quickSort(quickSortTickets, 0, numOfTickets - 1, &quickSortStats);

    writeTicketsToFile(quickSortFileName, quickSortTickets, numOfTickets);
    printf("Tickets after Quick Sort have been written to %s\n", quickSortFileName);
    printf("Quick Sort Comparisons: %d\n", quickSortStats.comparisons);
    printf("Quick Sort Data Transfers: %d\n", quickSortStats.dataTransfers);

    return 0;
}
```

# Lab 7
Include the following
1. Creation of binary tree using level order and Depth order.
2. Perform all types of traversals.
3. Create a binary tree using any two traversals.
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *left;
    struct node *right;
};

struct node *new_node(int data)
{
    struct node *node = (struct node *)malloc(sizeof(struct node));
    node->data = data;
    node->left = NULL;
    node->right = NULL;
    return node;
}

struct node *create_tree(int *arr, int start, int end)
{
    if (start > end)
        return NULL;

    int mid = start + (end - start) / 2;
    struct node *root = new_node(arr[mid]);

    root->left = create_tree(arr, start, mid - 1);
    root->right = create_tree(arr, mid + 1, end);

    return root;
}

void level_order_traversal(struct node *root)
{
    if (root == NULL)
        return;

    struct node *queue[100];
    int front = 0, rear = 0;

    queue[rear++] = root;

    while (front < rear)
    {
        struct node *current = queue[front++];
        printf("%d ", current->data);

        if (current->left != NULL)
            queue[rear++] = current->left;

        if (current->right != NULL)
            queue[rear++] = current->right;
    }
}

int maxDepth(struct node *root)
{
    if (root == NULL)
        return 0;
    else
    {
        int leftDepth = maxDepth(root->left);
        int rightDepth = maxDepth(root->right);

        if (leftDepth > rightDepth)
            return (leftDepth + 1);
        else
            return (rightDepth + 1);
    }
}

void printGivenLevel(struct node *root, int level)
{
    if (root == NULL)
        return;
    if (level == 1)
        printf("%d ", root->data);
    else if (level > 1)
    {
        printGivenLevel(root->left, level - 1);
        printGivenLevel(root->right, level - 1);
    }
}

void depth_order_traversal(struct node *root)
{
    int height = maxDepth(root);
    for (int i = 1; i <= height; i++)
    {
        printf("Level %d: ", i);
        printGivenLevel(root, i);
        printf("\n");
    }
}

int main()
{
    int arr[] = {1, 2, 3, 4, 5, 6};
    int n = sizeof(arr) / sizeof(arr[0]);

    struct node *root = create_tree(arr, 0, n - 1);

    printf("Inorder traversal: ");
    inorder_traversal(root);
    printf("\n");
    printf("Postorder traversal: ");
    postorder_traversal(root);
    printf("\n");
    printf("Preorder traversal: ");
    preorder_traversal(root);
    printf("\n");
    printf("Level order traversal: ");
    level_order_traversal(root);
    printf("\n");
    printf("Depth order traversal:\n");
    depth_order_traversal(root);

    return 0;
}
```

# Lab 8
Perform deletion,search,operations
Calculate the  height of the BST
Perform all traversals
## Code
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *left;
    struct Node *right;
};

struct Node *createNode(int data)
{
    struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}

struct Node *insert(struct Node *root, int data)
{
    if (root == NULL)
    {
        return createNode(data);
    }
    if (data < root->data)
    {
        root->left = insert(root->left, data);
    }
    else if (data > root->data)
    {
        root->right = insert(root->right, data);
    }
    return root;
}

struct Node *search(struct Node *root, int data)
{
    if (root == NULL || root->data == data)
    {
        return root;
    }
    if (data < root->data)
    {
        return search(root->left, data);
    }
    return search(root->right, data);
}

struct Node *minValueNode(struct Node *node)
{
    struct Node *current = node;
    while (current && current->left != NULL)
    {
        current = current->left;
    }
    return current;
}

struct Node *deleteNode(struct Node *root, int data)
{
    if (root == NULL)
    {
        return root;
    }
    if (data < root->data)
    {
        root->left = deleteNode(root->left, data);
    }
    else if (data > root->data)
    {
        root->right = deleteNode(root->right, data);
    }
    else
    {
        if (root->left == NULL)
        {
            struct Node *temp = root->right;
            free(root);
            return temp;
        }
        else if (root->right == NULL)
        {
            struct Node *temp = root->left;
            free(root);
            return temp;
        }
        struct Node *temp = minValueNode(root->right);
        root->data = temp->data;
        root->right = deleteNode(root->right, temp->data);
    }
    return root;
}

int height(struct Node *root)
{
    if (root == NULL)
    {
        return -1;
    }
    int leftHeight = height(root->left);
    int rightHeight = height(root->right);
    return (leftHeight > rightHeight) ? leftHeight + 1 : rightHeight + 1;
}

void inorderTraversal(struct Node *root)
{
    if (root != NULL)
    {
        inorderTraversal(root->left);
        printf("%d ", root->data);
        inorderTraversal(root->right);
    }
}

void preorderTraversal(struct Node *root)
{
    if (root != NULL)
    {
        printf("%d ", root->data);
        preorderTraversal(root->left);
        preorderTraversal(root->right);
    }
}

void postorderTraversal(struct Node *root)
{
    if (root != NULL)
    {
        postorderTraversal(root->left);
        postorderTraversal(root->right);
        printf("%d ", root->data);
    }
}

int main()
{
    struct Node *root = NULL;
    root = insert(root, 50);
    root = insert(root, 30);
    root = insert(root, 20);
    root = insert(root, 40);
    root = insert(root, 70);
    root = insert(root, 60);
    root = insert(root, 80);

    printf("Inorder traversal: ");
    inorderTraversal(root);
    printf("\n");

    printf("Preorder traversal: ");
    preorderTraversal(root);
    printf("\n");

    printf("Postorder traversal: ");
    postorderTraversal(root);
    printf("\n");

    int searchData = 40;
    struct Node *searchResult = search(root, searchData);
    if (searchResult != NULL)
    {
        printf("%d found in the BST.\n", searchData);
    }
    else
    {
        printf("%d not found in the BST.\n", searchData);
    }

    int deleteData = 30;
    root = deleteNode(root, deleteData);
    printf("Inorder traversal after deleting %d: ", deleteData);
    inorderTraversal(root);
    printf("\n");

    int bstHeight = height(root);
    printf("Height of the BST: %d\n", bstHeight);

    return 0;
}
```

# Lab 9
Implement both BFT and DFT
Perform search operation using BTF and DFT
```
#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>

typedef struct Node
{
    int data;
    struct Node *next;
} Node;

typedef struct Graph
{
    int numVertices;
    Node **adjacencyList;
} Graph;

Node *createNode(int data)
{
    Node *newNode = (Node *)malloc(sizeof(Node));
    newNode->data = data;
    newNode->next = NULL;
    return newNode;
}

Graph *createGraph(int numVertices)
{
    Graph *graph = (Graph *)malloc(sizeof(Graph));
    graph->numVertices = numVertices;
    graph->adjacencyList = (Node **)malloc(numVertices * sizeof(Node *));

    for (int i = 0; i < numVertices; ++i)
        graph->adjacencyList[i] = NULL;

    return graph;
}

void addEdge(Graph *graph, int src, int dest)
{
    Node *newNode = createNode(dest);
    newNode->next = graph->adjacencyList[src];
    graph->adjacencyList[src] = newNode;
}

void BFT(Graph *graph, int startVertex)
{

    int *queue = (int *)malloc(graph->numVertices * sizeof(int));
    bool *visited = (bool *)malloc(graph->numVertices * sizeof(bool));

    for (int i = 0; i < graph->numVertices; ++i)
        visited[i] = false;

    int front = 0, rear = 0;
    queue[rear++] = startVertex;
    visited[startVertex] = true;

    while (front < rear)
    {
        int currentVertex = queue[front++];
        printf("%d ", currentVertex);

        Node *temp = graph->adjacencyList[currentVertex];
        while (temp != NULL)
        {
            int adjacentVertex = temp->data;
            if (!visited[adjacentVertex])
            {
                queue[rear++] = adjacentVertex;
                visited[adjacentVertex] = true;
            }
            temp = temp->next;
        }
    }

    free(queue);
    free(visited);
}

void DFTUtil(Graph *graph, int vertex, bool visited[])
{
    visited[vertex] = true;
    printf("%d ", vertex);

    Node *temp = graph->adjacencyList[vertex];
    while (temp != NULL)
    {
        int adjacentVertex = temp->data;
        if (!visited[adjacentVertex])
            DFTUtil(graph, adjacentVertex, visited);
        temp = temp->next;
    }
}

void DFT(Graph *graph, int startVertex)
{
    bool *visited = (bool *)malloc(graph->numVertices * sizeof(bool));
    for (int i = 0; i < graph->numVertices; ++i)
        visited[i] = false;

    DFTUtil(graph, startVertex, visited);
    free(visited);
}

bool search(Graph *graph, int startVertex, int targetVertex)
{
    bool *visited = (bool *)malloc(graph->numVertices * sizeof(bool));
    for (int i = 0; i < graph->numVertices; ++i)
        visited[i] = false;

    int *queue = (int *)malloc(graph->numVertices * sizeof(int));
    int front = 0, rear = 0;
    queue[rear++] = startVertex;
    visited[startVertex] = true;

    while (front < rear)
    {
        int currentVertex = queue[front++];
        if (currentVertex == targetVertex)
        {
            return true;
        }

        Node *temp = graph->adjacencyList[currentVertex];
        while (temp != NULL)
        {
            int adjacentVertex = temp->data;
            if (!visited[adjacentVertex])
            {
                queue[rear++] = adjacentVertex;
                visited[adjacentVertex] = true;
            }
            temp = temp->next;
        }
    }

    free(queue);
    free(visited);
    return false;
}

int main()
{
    int numVertices = 5;
    Graph *graph = createGraph(numVertices);

    addEdge(graph, 0, 1);
    addEdge(graph, 0, 2);
    addEdge(graph, 1, 3);
    addEdge(graph, 2, 4);

    bool isFound = search(graph, 0, 4);
    if (isFound)
    {
        printf("Found\n");
    }
    else
    {
        printf("Not Found\n");
    }

    printf("Breadth-First Traversal:\n");
    BFT(graph, 0);

    printf("\nDepth-First Traversal:\n");
    DFT(graph, 0);

    return 0;
}
```

# Lab 10
Create MST using PRIM's and Kruskal's method
## Prims method
```
#include <stdio.h>
#include <stdbool.h>
#define INF 9999999
#define V 5

int minKey(int key[], bool mstSet[])
{
    int min = INF, min_index;
    for (int v = 0; v < V; v++)
    {
        if (mstSet[v] == false && key[v] < min)
        {
            min = key[v];
            min_index = v;
        }
    }
    return min_index;
}

void printMST(int parent[], int graph[V][V])
{
    printf("Edge \tWeight\n");
    for (int i = 1; i < V; i++)
    {
        printf("%d - %d \t%d \n", parent[i], i, graph[i][parent[i]]);
    }
}

void primMST(int graph[V][V])
{
    int parent[V];
    int key[V];
    bool mstSet[V];

    for (int i = 0; i < V; i++)
    {
        key[i] = INF;
        mstSet[i] = false;
    }

    key[0] = 0;
    parent[0] = -1;

    for (int count = 0; count < V - 1; count++)
    {
        int u = minKey(key, mstSet);
        mstSet[u] = true;

        for (int v = 0; v < V; v++)
        {
            if (graph[u][v] && mstSet[v] == false && graph[u][v] < key[v])
            {
                parent[v] = u;
                key[v] = graph[u][v];
            }
        }
    }

    printMST(parent, graph);
}

int main()
{
    int graph[V][V] = {{0, 2, 0, 6, 0},
                       {2, 0, 3, 8, 5},
                       {0, 3, 0, 0, 7},
                       {6, 8, 0, 0, 9},
                       {0, 5, 7, 9, 0}};

    primMST(graph);

    return 0;
}
```

## Kruskal method
```
#include <stdio.h>
#include <stdlib.h>

struct Edge
{
    int src, dest, weight;
};

struct Subset
{
    int parent;
    int rank;
};

int find(struct Subset subsets[], int i)
{
    if (subsets[i].parent != i)
        subsets[i].parent = find(subsets, subsets[i].parent);
    return subsets[i].parent;
}

void unionSets(struct Subset subsets[], int x, int y)
{
    int xroot = find(subsets, x);
    int yroot = find(subsets, y);

    if (subsets[xroot].rank < subsets[yroot].rank)
        subsets[xroot].parent = yroot;
    else if (subsets[xroot].rank > subsets[yroot].rank)
        subsets[yroot].parent = xroot;
    else
    {
        subsets[yroot].parent = xroot;
        subsets[xroot].rank++;
    }
}

int compareEdges(const void *a, const void *b)
{
    struct Edge *edge1 = (struct Edge *)a;
    struct Edge *edge2 = (struct Edge *)b;
    return edge1->weight - edge2->weight;
}

void kruskalMST(struct Edge edges[], int V, int E)
{
    struct Edge result[V];
    int i = 0;
    int e = 0;

    qsort(edges, E, sizeof(struct Edge), compareEdges);

    struct Subset *subsets = (struct Subset *)malloc(V * sizeof(struct Subset));

    for (int v = 0; v < V; v++)
    {
        subsets[v].parent = v;
        subsets[v].rank = 0;
    }

    while (i < V - 1 && e < E)
    {
        struct Edge nextEdge = edges[e++];

        int x = find(subsets, nextEdge.src);
        int y = find(subsets, nextEdge.dest);

        if (x != y)
        {
            result[i++] = nextEdge;
            unionSets(subsets, x, y);
        }
    }

    printf("Minimum Spanning Tree:\n");
    for (int j = 0; j < i; j++)
    {
        printf("%d -- %d\tWeight: %d\n", result[j].src, result[j].dest, result[j].weight);
    }

    free(subsets);
}

int main()
{
    int V, E;
    printf("Enter the number of vertices: ");
    scanf("%d", &V);
    printf("Enter the number of edges: ");
    scanf("%d", &E);

    struct Edge edges[E];
    printf("Enter the source, destination, and weight of each edge:\n");
    for (int i = 0; i < E; i++)
    {
        scanf("%d %d %d", &edges[i].src, &edges[i].dest, &edges[i].weight);
    }

    kruskalMST(edges, V, E);

    return 0;
}
```

# Priority Queue
## Code
```
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 10

struct PriorityQueue {
    int data[MAX_SIZE];
    int priority[MAX_SIZE];
    int size;
};

void initializePriorityQueue(struct PriorityQueue *pq) {
    pq->size = 0;
}

void insert(struct PriorityQueue *pq, int data, int priority) {
    if (pq->size < MAX_SIZE) {
        pq->data[pq->size] = data;
        pq->priority[pq->size] = priority;
        pq->size++;
        printf("Inserted: (%d, %d)\n", data, priority);
    } else {
        printf("Priority Queue is full. Cannot insert.\n");
    }
}

int extractMin(struct PriorityQueue *pq) {
    if (pq->size > 0) {
        int minIndex = 0;
        for (int i = 1; i < pq->size; i++) {
            if (pq->priority[i] < pq->priority[minIndex]) {
                minIndex = i;
            }
        }

        int minData = pq->data[minIndex];

        // Remove the element by shifting remaining elements
        for (int i = minIndex; i < pq->size - 1; i++) {
            pq->data[i] = pq->data[i + 1];
            pq->priority[i] = pq->priority[i + 1];
        }

        pq->size--;

        return minData;
    } else {
        printf("Priority Queue is empty. Cannot extract.\n");
        return -1; // Placeholder for an empty queue
    }
}

void printPriorityQueue(struct PriorityQueue *pq) {
    printf("Priority Queue: ");
    for (int i = 0; i < pq->size; i++) {
        printf("(%d, %d) ", pq->data[i], pq->priority[i]);
    }
    printf("\n");
}

int main() {
    struct PriorityQueue pq;
    initializePriorityQueue(&pq);

    insert(&pq, 5, 2);
    insert(&pq, 8, 1);
    insert(&pq, 3, 4);
    insert(&pq, 1, 7);

    printPriorityQueue(&pq);

    int minElement = extractMin(&pq);
    if (minElement != -1) {
        printf("Extracted min element: %d\n", minElement);
    }

    printPriorityQueue(&pq);

    return 0;
}
```

# Circular Queue with insertion at beginning, middle and end.
## Code
```
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 10

struct CircularQueue {
    int items[MAX_SIZE];
    int front, rear;
};

void initializeQueue(struct CircularQueue *queue) {
    queue->front = -1;
    queue->rear = -1;
}

int isFull(struct CircularQueue *queue) {
    return (queue->front == (queue->rear + 1) % MAX_SIZE);
}

int isEmpty(struct CircularQueue *queue) {
    return (queue->front == -1 && queue->rear == -1);
}

void enqueueBeginning(struct CircularQueue *queue, int data) {
    if (isFull(queue)) {
        printf("Queue is full. Cannot enqueue.\n");
        return;
    }

    if (isEmpty(queue)) {
        queue->front = 0;
        queue->rear = 0;
    } else {
        queue->front = (queue->front - 1 + MAX_SIZE) % MAX_SIZE;
    }

    queue->items[queue->front] = data;
    printf("%d enqueued at the beginning.\n", data);
}

void enqueueMiddle(struct CircularQueue *queue, int data) {
    if (isFull(queue)) {
        printf("Queue is full. Cannot enqueue.\n");
        return;
    }

    if (isEmpty(queue)) {
        queue->front = 0;
        queue->rear = 0;
    } else {
        queue->front = (queue->front - 1 + MAX_SIZE) % MAX_SIZE;
    }

    int mid = (queue->front + queue->rear) / 2;
    int i;

    for (i = queue->rear; i != mid; i = (i - 1 + MAX_SIZE) % MAX_SIZE) {
        queue->items[i] = queue->items[(i - 1 + MAX_SIZE) % MAX_SIZE];
    }

    queue->items[mid] = data;
    queue->rear = (queue->rear + 1) % MAX_SIZE;

    printf("%d enqueued in the middle.\n", data);
}

void enqueueEnd(struct CircularQueue *queue, int data) {
    if (isFull(queue)) {
        printf("Queue is full. Cannot enqueue.\n");
        return;
    }

    if (isEmpty(queue)) {
        queue->front = 0;
        queue->rear = 0;
    } else {
        queue->rear = (queue->rear + 1) % MAX_SIZE;
    }

    queue->items[queue->rear] = data;
    printf("%d enqueued at the end.\n", data);
}

void display(struct CircularQueue *queue) {
    if (isEmpty(queue)) {
        printf("Queue is empty.\n");
        return;
    }

    int i;
    printf("Queue elements: ");
    for (i = queue->front; i != queue->rear; i = (i + 1) % MAX_SIZE) {
        printf("%d ", queue->items[i]);
    }
    printf("%d\n", queue->items[i]);
}

int main() {
    struct CircularQueue queue;
    initializeQueue(&queue);

    enqueueEnd(&queue, 1);
    enqueueEnd(&queue, 2);
    enqueueEnd(&queue, 3);

    display(&queue);

    enqueueBeginning(&queue, 0);
    enqueueMiddle(&queue, 4);

    display(&queue);

    return 0;
}
```

# Double Ended Queue
## Code
```
#include <stdio.h>
#include <stdlib.h>

// Node structure for the doubly linked list
typedef struct Node {
    int data;
    struct Node* prev;
    struct Node* next;
} Node;

// Deque structure
typedef struct Deque {
    Node* front;
    Node* rear;
} Deque;

// Function to create a new node
Node* createNode(int data) {
    Node* newNode = (Node*)malloc(sizeof(Node));
    if (newNode == NULL) {
        printf("Memory allocation failed\n");
        exit(EXIT_FAILURE);
    }
    newNode->data = data;
    newNode->prev = NULL;
    newNode->next = NULL;
    return newNode;
}

// Function to initialize an empty deque
void initializeDeque(Deque* deque) {
    deque->front = NULL;
    deque->rear = NULL;
}

// Function to insert at the beginning of the deque
void insertAtBeginning(Deque* deque, int data) {
    Node* newNode = createNode(data);
    if (deque->front == NULL) {
        deque->front = newNode;
        deque->rear = newNode;
    } else {
        newNode->next = deque->front;
        deque->front->prev = newNode;
        deque->front = newNode;
    }
}

// Function to insert at the end of the deque
void insertAtEnd(Deque* deque, int data) {
    Node* newNode = createNode(data);
    if (deque->rear == NULL) {
        deque->front = newNode;
        deque->rear = newNode;
    } else {
        newNode->prev = deque->rear;
        deque->rear->next = newNode;
        deque->rear = newNode;
    }
}

// Function to insert at the middle of the deque
void insertAtMiddle(Deque* deque, int data) {
    if (deque->front == NULL) {
        insertAtBeginning(deque, data);
    } else {
        Node* middle = deque->front;
        Node* fast = deque->front;

        while (fast != NULL && fast->next != NULL) {
            fast = fast->next->next;
            if (fast != NULL) {
                middle = middle->next;
            }
        }

        Node* newNode = createNode(data);

        if (middle->next != NULL) {
            newNode->next = middle->next;
            middle->next->prev = newNode;
        } else {
            deque->rear = newNode;
        }

        newNode->prev = middle;
        middle->next = newNode;
    }
}

// Function to print the deque
void printDeque(Deque* deque) {
    Node* current = deque->front;
    while (current != NULL) {
        printf("%d ", current->data);
        current = current->next;
    }
    printf("\n");
}

// Function to free memory allocated for the deque
void freeDeque(Deque* deque) {
    Node* current = deque->front;
    while (current != NULL) {
        Node* temp = current;
        current = current->next;
        free(temp);
    }
    deque->front = NULL;
    deque->rear = NULL;
}

int main() {
    Deque deque;
    initializeDeque(&deque);

    // Insert at the beginning
    insertAtBeginning(&deque, 1);
    insertAtBeginning(&deque, 2);

    // Insert at the end
    insertAtEnd(&deque, 3);
    insertAtEnd(&deque, 4);

    // Insert at the middle
    insertAtMiddle(&deque, 5);

    // Print the deque
    printf("Deque: ");
    printDeque(&deque);

    // Free memory
    freeDeque(&deque);

    return 0;
}
```

# Lab exam set 4
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

struct Vehicle
{
    char name[20];
    char regNumber[20];
    int priority;
    struct Vehicle *next;
};

struct Queue
{
    struct Vehicle *front, *rear;
};

struct Vehicle *createVehicle(const char *name, const char *regNumber, int priority)
{
    struct Vehicle *newVehicle = (struct Vehicle *)malloc(sizeof(struct Vehicle));
    if (newVehicle == NULL)
    {
        printf("Memory allocation failed.\n");
        exit(1);
    }
    strncpy(newVehicle->name, name, sizeof(newVehicle->name));
    strncpy(newVehicle->regNumber, regNumber, sizeof(newVehicle->regNumber));
    if (priority < 1 || priority > 20)
    {
        printf("Priority should be between 1 to 20. Vehicle %s not added to the queue.\n", name);
        free(newVehicle);
        return NULL;
    }
    newVehicle->priority = priority;
    newVehicle->next = NULL;
    return newVehicle;
}

struct Queue *createQueue()
{
    struct Queue *queue = (struct Queue *)malloc(sizeof(struct Queue));
    if (queue == NULL)
    {
        printf("Memory allocation failed.\n");
        exit(1);
    }
    queue->front = queue->rear = NULL;
    return queue;
}

int isEmpty(struct Queue *queue)
{
    return (queue->front == NULL);
}

void enqueue(struct Queue *queue, const char *name, const char *regNumber, int priority)
{
    struct Vehicle *newVehicle = createVehicle(name, regNumber, priority);
    if (newVehicle == NULL)
    {
        return;
    }

    if (isEmpty(queue))
    {
        queue->front = queue->rear = newVehicle;
    }
    else
    {
        queue->rear->next = newVehicle;
        queue->rear = newVehicle;
    }
    printf("Vehicle %s enqueued successfully with priority %d.\n", name, priority);
}

void displayQueue(struct Queue *queue)
{
    if (isEmpty(queue))
    {
        printf("Queue is empty.\n");
        return;
    }

    struct Vehicle *temp = queue->front;
    printf("Vehicles in the queue:\n");
    while (temp != NULL)
    {
        printf("Vehicle Name: %s, Registration Number: %s, Priority: %d\n", temp->name, temp->regNumber, temp->priority);
        temp = temp->next;
    }
}

void displayHighestPriority(struct Queue *queue)
{
    if (isEmpty(queue))
    {
        printf("Queue is empty.\n");
        return;
    }

    struct Vehicle *temp = queue->front;
    int highestPriority = 0;
    struct Vehicle *highestVehicle = NULL;

    while (temp != NULL)
    {
        if (temp->priority > highestPriority)
        {
            highestPriority = temp->priority;
            highestVehicle = temp;
        }
        temp = temp->next;
    }

    if (highestVehicle != NULL)
    {
        printf("Vehicle with highest priority:\n");
        printf("Vehicle Name: %s, Registration Number: %s, Priority: %d\n", highestVehicle->name, highestVehicle->regNumber, highestVehicle->priority);
    }
    else
    {
        printf("No vehicle with the highest priority found.\n");
    }
}

void splitQueue(struct Queue *queue, struct Queue *highQ, struct Queue *lowQ)
{
    if (isEmpty(queue))
    {
        printf("Queue is empty. Cannot split.\n");
        return;
    }

    struct Vehicle *temp = queue->front;
    while (temp != NULL)
    {
        if (temp->priority >= 1 && temp->priority <= 10)
        {
            enqueue(highQ, temp->name, temp->regNumber, temp->priority);
        }
        else
        {
            enqueue(lowQ, temp->name, temp->regNumber, temp->priority);
        }
        temp = temp->next;
    }
}

void displayQueueByPriority(struct Queue *queue, const char *queueName)
{
    if (isEmpty(queue))
    {
        printf("%s is empty.\n", queueName);
        return;
    }

    printf("Vehicles in %s:\n", queueName);
    displayQueue(queue);
}

int main()
{
    struct Queue *vehicleQueue = createQueue();
    struct Queue *highQ = createQueue();
    struct Queue *lowQ = createQueue();

    enqueue(vehicleQueue, "Car", "KA39AB36", 15);
    enqueue(vehicleQueue, "Van", "KA39CD37", 13);
    enqueue(vehicleQueue, "Lorry", "KA39EF38", 9);
    enqueue(vehicleQueue, "Jeep", "KA39GH39", 5);
    enqueue(vehicleQueue, "Truck", "KA39IJ40", 17);

    displayQueue(vehicleQueue);

    displayHighestPriority(vehicleQueue);

    splitQueue(vehicleQueue, highQ, lowQ);

    displayQueueByPriority(highQ, "High Priority Queue (1 to 10)");
    displayQueueByPriority(lowQ, "Low Priority Queue (11 to 20)");

    return 0;
}
```

---Lab 3

#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>
#include <ctype.h> // for isalnum()

#define MAX_SIZE 100

// Structure to represent the stack
struct Stack {
    int top;
    unsigned capacity;
    int* array;
};

// Function to create a stack
struct Stack* createStack(unsigned capacity) {
    struct Stack* stack = (struct Stack*)malloc(sizeof(struct Stack));
    stack->capacity = capacity;
    stack->top = -1;
    stack->array = (int*)malloc(stack->capacity * sizeof(int));
    return stack;
}

// Function to check if the stack is full
bool isFull(struct Stack* stack) {
    return stack->top == stack->capacity - 1;
}

// Function to check if the stack is empty
bool isEmpty(struct Stack* stack) {
    return stack->top == -1;
}

// Function to push an element onto the stack
void push(struct Stack* stack, int item) {
    if (isFull(stack))
        return;
    stack->array[++stack->top] = item;
}

// Function to pop an element from the stack
int pop(struct Stack* stack) {
    if (isEmpty(stack))
        return -1;
    return stack->array[stack->top--];
}

// Function to return the top element of the stack without popping it
int peek(struct Stack* stack) {
    if (isEmpty(stack))
        return -1;
    return stack->array[stack->top];
}

// Function to return precedence of operators
int precedence(char op) {
    if (op == '+' || op == '-')
        return 1;
    if (op == '*' || op == '/')
        return 2;
    return -1;
}

// Function to convert infix expression to postfix and print the steps
void infixToPostfix(char* infix, char* postfix) {
    struct Stack* stack = createStack(MAX_SIZE);
    int i, k;
    for (i = 0, k = -1; infix[i]; ++i) {
        if (isalnum(infix[i])) {
            postfix[++k] = infix[i];
            printf("Infix to postfix: %c -> %s\n", infix[i], postfix);
        } else if (infix[i] == '(') {
            push(stack, infix[i]);
        } else if (infix[i] == ')') {
            while (!isEmpty(stack) && peek(stack) != '(')
                postfix[++k] = pop(stack);
            if (!isEmpty(stack) && peek(stack) != '(')
                return; // Invalid expression
            else
                pop(stack);
        } else { // Operator encountered
            while (!isEmpty(stack) && precedence(infix[i]) <= precedence(peek(stack)))
                postfix[++k] = pop(stack);
            push(stack, infix[i]);
        }
    }
    while (!isEmpty(stack))
        postfix[++k] = pop(stack);
    postfix[++k] = '\0';
}

// Function to get the cost for a particular service in INR
int getServiceCost(char service) {
    switch (service) {
        case 'm': // massage
            return 3500; // cost for massage in INR
        case 's': // sauna
            return 2100; // cost for sauna in INR
        case 'f': // facial
            return 5600; // cost for facial in INR
        case 'y': // yoga session cost (total sessions)
            return 1400; // cost per yoga session in INR
        default:
            return -1; // Invalid service code
    }
}

// Function to calculate the total cost of the spa package and print the steps
int calculateSpaCost(char* infix) {
    char postfix[MAX_SIZE];

    // Infix to postfix conversion and print steps
    infixToPostfix(infix, postfix);

    printf("\nFinal Postfix expression: %s\n", postfix);

    struct Stack* stack = createStack(MAX_SIZE);
    int i, result, operand;
    for (i = 0; postfix[i]; ++i) {
        if (isalpha(postfix[i])) {
            operand = getServiceCost(postfix[i]);
            push(stack, operand);
        } else {
            int operand2 = pop(stack);
            int operand1 = pop(stack);
            switch (postfix[i]) {
                case '+':
                    push(stack, operand1 + operand2);
                    break;
                case '-':
                    push(stack, operand1 - operand2);
                    break;
                case '*':
                    push(stack, operand1 * operand2);
                    break;
                case '/':
                    push(stack, operand1 / operand2);
                    break;
            }
            printf("Evaluation of postfix: %d %c %d\n", operand1, postfix[i], operand2);
        }
    }
    result = pop(stack);
    return result;
}

int main() {
    printf("Enter the spa package cost formula using 'm', 's', 'f', and 'y' for massage, sauna, facial, and yoga sessions respectively: ");
    char infix[MAX_SIZE];
    scanf("%s", infix);

    int totalCost = calculateSpaCost(infix);
    if (totalCost == -1) {
        printf("Invalid service code entered!\n");
    } else {
        printf("Total cost of the spa package: ₹%d\n", totalCost); // Output in INR
    }

    return 0;
}

--- Lab 4

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Structure to represent a client in the Spa Management System
struct Client {
  int clientID;
  char name[50];
  struct Client *next;
};

// Structure to represent the Queue
struct Queue {
  struct Client *front, *rear;
};

// Function to create a new client node
struct Client *createClient(int id, const char *name) {
  struct Client *newClient = (struct Client *)malloc(sizeof(struct Client));
  newClient->clientID = id;
  strcpy(newClient->name, name);
  newClient->next = NULL;
  return newClient;
}

// Function to create an empty queue
struct Queue *createQueue() {
  struct Queue *queue = (struct Queue *)malloc(sizeof(struct Queue));
  queue->front = queue->rear = NULL;
  return queue;
}

// Function to schedule an appointment by enqueuing a client into the queue
void scheduleAppointment(struct Queue *queue, int id, const char *name) {
  struct Client *newClient = createClient(id, name);

  if (queue->rear == NULL) {
    queue->front = queue->rear = newClient;
    return;
  }

  queue->rear->next = newClient;
  queue->rear = newClient;
}

// Function to serve the next appointment by dequeuing a client from the queue
void serveNextAppointment(struct Queue *queue) {
  if (queue->front == NULL) {
    printf("No appointments in the queue\n");
    return;
  }

  struct Client *temp = queue->front;
  queue->front = queue->front->next;

  if (queue->front == NULL) {
    queue->rear = NULL;
  }

  printf("Serving Client ID: %d, Name: %s\n", temp->clientID, temp->name);
  free(temp);
}

// Function to display all scheduled appointments in the queue
void displayAppointments(struct Queue *queue) {
  if (queue->front == NULL) {
    printf("No appointments in the queue\n");
    return;
  }

  printf("Scheduled Appointments:\n");
  struct Client *temp = queue->front;
  while (temp != NULL) {
    printf("Client ID: %d, Name: %s\n", temp->clientID, temp->name);
    temp = temp->next;
  }
}

int main() {
  struct Queue *appointmentQueue = createQueue();
  int choice, id;
  char name[50];

  do {
    printf("\nSpa and Wellness Management System:\n");
    printf("1. Schedule Appointment\n");
    printf("2. Serve Next Appointment\n");
    printf("3. Display Scheduled Appointments\n");
    printf("4. Exit\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);

    switch (choice) {
    case 1:
      printf("Enter client ID: ");
      scanf("%d", &id);
      printf("Enter client name: ");
      scanf("%s", name);
      scheduleAppointment(appointmentQueue, id, name);
      printf("Appointment scheduled successfully.\n");
      break;
    case 2:
      serveNextAppointment(appointmentQueue);
      break;
    case 3:
      displayAppointments(appointmentQueue);
      break;
    case 4:
      printf("Exiting Spa and Wellness Management System...\n");
      break;
    default:
      printf("Invalid choice. Please enter a valid option.\n");
    }
  } while (choice != 4);

  return 0;
}

---Lab 5

#include <stdio.h>
#include <string.h>

// Define a structure for Spa Service data
typedef struct {
  int id;
  char name[50];
  int duration; // Duration of the service in minutes
} SpaService;

// Function to display a Spa Service
void displaySpaService(SpaService service) {
  printf("Service ID: %d, Name: %s, Duration: %d minutes\n", service.id,
         service.name, service.duration);
}

// Function to perform linear search for a service by ID
int linearSearchServiceByID(SpaService arr[], int size, int key,
                            int *elementComparisons, int *indexComparisons) {
  *elementComparisons = 0;
  *indexComparisons = 0;

  for (int i = 0; i < size; i++) {
    *elementComparisons += 1; // Increment element comparison count

    if (arr[i].id == key) {
      *indexComparisons = i + 1; // Record index comparison count
      return i;                  // Return index if found
    }
  }
  *indexComparisons = size; // Set index comparison to total size if not found
  return -1;                // Return -1 if not found
}

// Function to perform sentinel search for a service by ID
int sentinelSearchServiceByID(SpaService arr[], int size, int key,
                              int *elementComparisons, int *indexComparisons) {
  *elementComparisons = 0;
  *indexComparisons = 0;

  int last = arr[size - 1].id;
  arr[size - 1].id = key; // Set the last element as sentinel

  int i = 0;
  while (arr[i].id != key) {
    *elementComparisons += 1;
    i++;
  }

  arr[size - 1].id = last; // Restore the original value

  if (i < size - 1 || key == arr[size - 1].id) {
    *indexComparisons = i + 1; // Record index comparison count
    return i;                  // Return index if found
  }

  *indexComparisons = size; // Set index comparison to total size if not found
  return -1;                // Return -1 if not found
}

// Function to perform binary search for a service by ID
int binarySearchServiceByID(SpaService arr[], int left, int right, int key,
                            int *elementComparisons, int *indexComparisons) {
  *elementComparisons = 0;
  *indexComparisons = 0;

  while (left <= right) {
    *elementComparisons += 1;
    int mid = left + (right - left) / 2;

    if (arr[mid].id == key) {
      *indexComparisons = *elementComparisons; // Record index comparison count
      return mid;                              // Return index if found
    }

    if (arr[mid].id < key) {
      left = mid + 1;
    } else {
      right = mid - 1;
    }
  }

  *indexComparisons = *elementComparisons; // Set index comparison to total
                                           // element comparison if not found
  return -1;                               // Return -1 if not found
}

void bubbleSortServicesByID(SpaService arr[], int size, int *comparisons,
                            int *dataTransfers) {
  *comparisons = 0;
  *dataTransfers = 0;
  int swapped;

  for (int i = 0; i < size - 1; i++) {
    swapped = 0; // Reset swapped flag for each pass

    for (int j = 0; j < size - i - 1; j++) {
      *comparisons += 1;

      if (arr[j].id > arr[j + 1].id) {
        // Swap elements
        SpaService temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;

        *dataTransfers += 3; // Count data transfer operations for swapping
        swapped = 1;         // Set swapped flag
      }
    }

    // If no two elements were swapped in the inner loop, array is already
    // sorted
    if (swapped == 0) {
      break;
    }
  }
}

// Function to perform insertion sort for Spa Services based on ID
void insertionSortServicesByID(SpaService arr[], int size, int *comparisons,
                               int *dataTransfers) {
  *comparisons = 0;
  *dataTransfers = 0;

  for (int i = 1; i < size; i++) {
    SpaService key = arr[i];
    int j = i - 1;

    *dataTransfers += 1; // Account for key assignment

    while (j >= 0 && arr[j].id > key.id) {
      *comparisons += 1;

      arr[j + 1] = arr[j];
      *dataTransfers +=
          2; // Count data transfer operations for shifting (2 instead of 1)

      j = j - 1;
    }

    arr[j + 1] = key;
    *dataTransfers += 1; // Count data transfer operation for insertion
  }
}

int main() {
  SpaService services[] = {{101, "Swedish Massage", 60},
                           {102, "Aromatherapy", 45},
                           {103, "Hot Stone Massage", 75},
                           {104, "Facial Treatment", 50},
                           {105, "Sauna Session", 30}};
  int size = sizeof(services) / sizeof(services[0]);

  printf("Available Spa Services:\n");
  for (int i = 0; i < size; ++i) {
    printf("ID: %d, Name: %s, Duration: %d minutes\n", services[i].id,
           services[i].name, services[i].duration);
  }

  int bubbleComparisons, bubbleTransfers;
  bubbleSortServicesByID(services, size, &bubbleComparisons, &bubbleTransfers);

  int insertionComparisons, insertionTransfers;
  insertionSortServicesByID(services, size, &insertionComparisons,
                            &insertionTransfers);

  int searchServiceID, searchMethod;
  printf("\nEnter the Service ID to search: ");
  scanf("%d", &searchServiceID);

  printf("\nSelect Search Method:\n");
  printf("1. Linear Search\n");
  printf("2. Sentinel Search\n");
  printf("3. Binary Search\n");
  printf("Enter your choice: ");
  scanf("%d", &searchMethod);

  int elementComparisons = 0, indexComparisons = 0, searchResult = -1;

  switch (searchMethod) {
  case 1: // Linear Search
    searchResult =
        linearSearchServiceByID(services, size, searchServiceID,
                                &elementComparisons, &indexComparisons);
    break;
  case 2: // Sentinel Search
    searchResult =
        sentinelSearchServiceByID(services, size, searchServiceID,
                                  &elementComparisons, &indexComparisons);
    break;
  case 3: // Binary Search
    searchResult =
        binarySearchServiceByID(services, 0, size - 1, searchServiceID,
                                &elementComparisons, &indexComparisons);
    break;
  default:
    printf("Invalid choice.\n");
    return 1;
  }

  printf("\nSearch Method: ");
  switch (searchMethod) {
  case 1:
    printf("Linear Search");
    break;
  case 2:
    printf("Sentinel Search");
    break;
  case 3:
    printf("Binary Search");
    break;
  }
  printf(" for Service ID %d:\n", searchServiceID);
  printf("Element Comparisons: %d\n", elementComparisons);
  printf("Index Comparisons: %d\n", indexComparisons);
  if (searchResult != -1) {
    printf("Service found:\n");
    displaySpaService(services[searchResult]);
  } else {
    printf("Service not found.\n");
  }

  printf("\nBubble Sort Comparisons: %d\n", bubbleComparisons);
  printf("Bubble Sort Data Transfers: %d\n", bubbleTransfers);

  printf("\nInsertion Sort Comparisons: %d\n", insertionComparisons);
  printf("Insertion Sort Data Transfers: %d\n", insertionTransfers);

  return 0;
}

# Lab 6: Merge sort or quick sort, rand method

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

// Structure to store spa and wellness data
typedef struct {
    char name[50];
    int age;
    float weight;
    float height;
} spa_data;

// Function prototypes
void generate_data(spa_data *data, int n);
void merge_sort(spa_data *data, int n, int *comparisons, int *data_transfers);
void quick_sort(spa_data *data, int n, int *comparisons, int *data_transfers);
void write_data_to_file(spa_data *data, int n);
void read_data_from_file(spa_data *data, int n);
void compare_sorting_techniques(spa_data *data, int n);

// Function to generate random numerical data
void generate_data(spa_data *data, int n) {
    srand(time(NULL));

    for (int i = 0; i < n; i++) {
        char alphabet[26] = "abcdefghijklmnopqrstuvwxyz";
        int name_length = rand() % 10 + 5; // Random length between 5 and 14 characters
        for (int j = 0; j < name_length; j++) {
            data[i].name[j] = alphabet[rand() % 26];
        }
        data[i].name[name_length] = '\0'; // Null-terminate the string

        data[i].age = rand() % 48 + 18; // Random age between 18 and 65
        data[i].weight = (float)(rand() % 76 + 45); // Random weight between 45 and 120 kg
        data[i].height = (float)(rand() % 51 + 150) / 100; // Random height between 1.5 and 2.0 meters
    }
}

// Function to perform merge sort on spa data
void merge_sort(spa_data *data, int n, int *comparisons, int *data_transfers) {
    if (n <= 1) {
        return;
    }

    int mid = n / 2;
    spa_data *left = malloc(sizeof(spa_data) * mid);
    spa_data *right = malloc(sizeof(spa_data) * (n - mid));
    for (int i = 0; i < mid; i++) {
        left[i] = data[i];
    }
    for (int i = mid; i < n; i++) {
        right[i - mid] = data[i];
    }

    merge_sort(left, mid, comparisons, data_transfers);
    merge_sort(right, n - mid, comparisons, data_transfers);

    int i = 0, j = 0, k = 0;
    while (i < mid && j < n - mid) {
        (*comparisons)++;
        if (left[i].age <= right[j].age) {
            data[k] = left[i];
            i++;
        } else {
            data[k] = right[j];
            j++;
        }
        k++;
        (*data_transfers)++;
    }

    while (i < mid) {
        data[k] = left[i];
        i++;
        k++;
    }

    while (j < n - mid) {
        data[k] = right[j];
        j++;
        k++;
    }

    free(left);
    free(right);
}

// Function to perform quick sort on spa data
void quick_sort(spa_data *data, int n, int *comparisons, int *data_transfers) {
    if (n <= 1) {
        return;
    }

    int pivot_index = rand() % n;
    spa_data pivot = data[pivot_index];

    int i = 0, j = n - 1;
    while (i < j) {
        (*comparisons)++;
        while (data[i].age < pivot.age) {
            i++;
            (*comparisons)++;
        }
        while (data[j].age >= pivot.age && j > i) {
            j--;
            (*comparisons)++;
        }
        if (i < j) {
            spa_data temp = data[i];
            data[i] = data[j];
            data[j] = temp;
            (*data_transfers) += 3;
        }
    }

    data[i] = pivot;

    quick_sort(data, i, comparisons, data_transfers);
    quick_sort(data + i + 1, n - i - 1, comparisons, data_transfers);
}

// Function to write spa data to a file
void write_data_to_file(spa_data *data, int n) {
    FILE *fp = fopen("spa_data.txt", "w");
    if (fp == NULL) {
        perror("Error opening file");
        return;
    }

    for (int i = 0; i < n; i++) {
        fprintf(fp, "%s %d %.1f %.2f\n", data[i].name, data[i].age, data[i].weight, data[i].height);
    }

    fclose(fp);
}

// Function to read spa data from a file
void read_data_from_file(spa_data *data, int n) {
    FILE *fp = fopen("spa_data.txt", "r");
    if (fp == NULL) {
        perror("Error opening file");
        return;
    }

    for (int i = 0; i < n; i++) {
        fscanf(fp, "%s %d %f %f", data[i].name, &data[i].age, &data[i].weight, &data[i].height);
    }

    fclose(fp);
}

// Function to compare the number of comparisons and data transfer operations for merge sort and quick sort
void compare_sorting_techniques(spa_data *data, int n) {
    int merge_comparisons = 0, merge_data_transfers = 0;
    int quick_comparisons = 0, quick_data_transfers = 0;

    spa_data *data_merge = malloc(sizeof(spa_data) * n);
    spa_data *data_quick = malloc(sizeof(spa_data) * n);

    for (int i = 0; i < n; i++) {
        data_merge[i] = data[i];
        data_quick[i] = data[i];
    }

    merge_sort(data_merge, n, &merge_comparisons, &merge_data_transfers);
    quick_sort(data_quick, n, &quick_comparisons, &quick_data_transfers);

    printf("Merge Sort:\n");
    printf("Number of comparisons: %d\n", merge_comparisons);
    printf("Number of data transfer operations: %d\n", merge_data_transfers);

    printf("\nQuick Sort:\n");
    printf("Number of comparisons: %d\n", quick_comparisons);
    printf("Number of data transfer operations: %d\n", quick_data_transfers);

    free(data_merge);
    free(data_quick);
}

int main() {
    int n = 10;
    spa_data *data = malloc(sizeof(spa_data) * n);

    generate_data(data, n);
    write_data_to_file(data, n);
    read_data_from_file(data, n);

    compare_sorting_techniques(data, n);

    free(data);
    return 0;
}

# Lab 8: BST and operations

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Structure for Spa Service
struct SpaService {
  int serviceID;
  char serviceName[50];
  float price;
  // You can add more information related to spa services
};

// Node structure for the SpaService BST
struct Node {
  struct SpaService service;
  struct Node *left;
  struct Node *right;
};

// Function to create a new node
struct Node *createNode(struct SpaService service) {
  struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));
  newNode->service = service;
  newNode->left = newNode->right = NULL;
  return newNode;
}

// Function to insert a spa service into the BST
struct Node *insert(struct Node *root, struct SpaService service) {
  if (root == NULL) {
    return createNode(service);
  }

  if (service.serviceID < root->service.serviceID) {
    root->left = insert(root->left, service);
  } else if (service.serviceID > root->service.serviceID) {
    root->right = insert(root->right, service);
  }

  return root;
}

// Function to perform deletion in the BST
struct Node *deleteNode(struct Node *root, int serviceID) {
  if (root == NULL) {
    return root;
  }

  if (serviceID < root->service.serviceID) {
    root->left = deleteNode(root->left, serviceID);
  } else if (serviceID > root->service.serviceID) {
    root->right = deleteNode(root->right, serviceID);
  } else {
    // Node with only one child or no child
    if (root->left == NULL) {
      struct Node *temp = root->right;
      free(root);
      return temp;
    } else if (root->right == NULL) {
      struct Node *temp = root->left;
      free(root);
      return temp;
    }

    // Node with two children
    struct Node *temp = root->right;
    while (temp->left != NULL) {
      temp = temp->left;
    }

    root->service = temp->service;
    root->right = deleteNode(root->right, temp->service.serviceID);
  }

  return root;
}

// Function to perform search in the BST
struct Node *search(struct Node *root, int serviceID) {
  if (root == NULL || root->service.serviceID == serviceID) {
    return root;
  }

  if (serviceID < root->service.serviceID) {
    return search(root->left, serviceID);
  }

  return search(root->right, serviceID);
}

// Function to calculate the height of the BST
int getHeight(struct Node *root) {
  if (root == NULL) {
    return 0;
  } else {
    int leftHeight = getHeight(root->left);
    int rightHeight = getHeight(root->right);

    // Return the height of the taller subtree + 1
    return (leftHeight > rightHeight ? leftHeight : rightHeight) + 1;
  }
}

// Function to perform in-order traversal
void inOrderTraversal(struct Node *root) {
  if (root != NULL) {
    inOrderTraversal(root->left);
    printf("Service ID: %d, Name: %s, Price: %.2f\n", root->service.serviceID,
           root->service.serviceName, root->service.price);
    inOrderTraversal(root->right);
  }
}
// Function to perform pre-order traversal
void preOrderTraversal(struct Node *root) {
  if (root != NULL) {
    printf("Service ID: %d, Name: %s, Price: %.2f\n", root->service.serviceID,
           root->service.serviceName, root->service.price);
    preOrderTraversal(root->left);
    preOrderTraversal(root->right);
  }
}

// Function to perform post-order traversal
void postOrderTraversal(struct Node *root) {
  if (root != NULL) {
    postOrderTraversal(root->left);
    postOrderTraversal(root->right);
    printf("Service ID: %d, Name: %s, Price: %.2f\n", root->service.serviceID,
           root->service.serviceName, root->service.price);
  }
}

int main() {
  struct Node *root = NULL;

  // Example of inserting spa services into the BST
  struct SpaService service1 = {1, "Massage", 60.00};
  struct SpaService service2 = {2, "Facial", 80.00};
  struct SpaService service3 = {3, "Sauna", 40.00};
  struct SpaService service4 = {4, "Pedicure", 50.00};
  struct SpaService service5 = {5, "Manicure", 45.00};

  root = insert(root, service1);
  insert(root, service2);
  insert(root, service3);
  insert(root, service4);
  insert(root, service5);

  // Example of deleting a spa service from the BST
  printf("In-order traversal before deletion:\n");
  inOrderTraversal(root);
  printf("\n");

  root = deleteNode(root, 2);

  printf("In-order traversal after deletion:\n");
  inOrderTraversal(root);
  printf("\n");

  // Example of searching for a spa service in the BST
  int serviceIDToSearch = 1;
  struct Node *result = search(root, serviceIDToSearch);
  if (result != NULL) {
    printf("Service ID %d found in the BST.\n\n", serviceIDToSearch);
  } else {
    printf("Service ID %d not found in the BST.\n\n", serviceIDToSearch);
  }

  // Example of performing pre-order traversal
  printf("Pre-order traversal:\n");
  preOrderTraversal(root);
  printf("\n");

  // Example of performing post-order traversal
  printf("Post-order traversal:\n");
  postOrderTraversal(root);
  printf("\n");

  // Example of calculating the height of the BST
  int height = getHeight(root);
  printf("Height of the BST: %d\n\n", height);

  return 0;
}


## Lab 9: Graph Traversals

#include <stdio.h>
#include <stdlib.h>

// Define the node structure for the spa and wellness management system
typedef struct Node {
  int id;
  char *name;
  char *type;                // Can be "Spa", "Salon", "Wellness" or "Gym"
  struct Node *children[10]; // Assuming each node can have up to 10 children
                             // for simplicity
} Node;

// Initialize the spa and wellness management system with some sample data
Node *initializeSystem() {
  // Create the root node for the system
  Node *root = (Node *)malloc(sizeof(Node));
  root->id = 1;
  root->name = "Main Spa";
  root->type = "Spa";

  // Create child nodes for the root node
  root->children[0] = (Node *)malloc(sizeof(Node));
  root->children[0]->id = 2;
  root->children[0]->name = "Massage Room";
  root->children[0]->type = "Spa";

  root->children[1] = (Node *)malloc(sizeof(Node));
  root->children[1]->id = 3;
  root->children[1]->name = "Facial Room";
  root->children[1]->type = "Spa";

  root->children[2] = (Node *)malloc(sizeof(Node));
  root->children[2]->id = 4;
  root->children[2]->name = "Body Treatment Room";
  root->children[2]->type = "Spa";

  // Create a child node for one of the child nodes
  root->children[0]->children[0] = (Node *)malloc(sizeof(Node));
  root->children[0]->children[0]->id = 5;
  root->children[0]->children[0]->name = "Aromatherapy Massage Room";
  root->children[0]->children[0]->type = "Spa";

  return root;
}

// Function to perform Breadth-First Traversal and print the details of each
// node
void BFT(Node *root) {
  if (root == NULL)
    return;

  Node *queue[100]; // Assuming a queue with a maximum size of 100
  int front = 0, rear = 0;

  queue[rear++] = root;

  while (front < rear) {
    Node *current = queue[front++];

    // Process the current node (e.g., print its details)
    printf("Node ID: %d\n", current->id);
    printf("Node Name: %s\n", current->name);
    printf("Node Type: %s\n", current->type);
    printf("\n");

    // Enqueue children of the current node
    for (int i = 0; i < 10 && current->children[i] != NULL; ++i) {
      queue[rear++] = current->children[i];
    }
  }
}

// Function to perform Depth-First Traversal and print the details of each node
void DFT(Node *root) {
  if (root == NULL)
    return;

  // Process the current node (e.g., print its details)
  printf("Node ID: %d\n", root->id);
  printf("Node Name: %s\n", root->name);
  printf("Node Type: %s\n", root->type);
  printf("\n");

  // Recursively traverse the children
  for (int i = 0; i < 10 && root->children[i] != NULL; ++i) {
    DFT(root->children[i]);
  }
}

// Function to perform Breadth-First Traversal and search for a specific node by
// its ID
Node *BFTWithSearch(Node *root, int targetId) {
  if (root == NULL)
    return NULL;

  Node *queue[100];
  int front = 0, rear = 0;

  queue[rear++] = root;

  while (front < rear) {
    Node *current = queue[front++];

    // Perform search operation
    if (current->id == targetId) {
      // Target node found
      return current;
    }

    // Enqueue children of the current node
    for (int i = 0; i < 10 && current->children[i] != NULL; ++i) {
      queue[rear++] = current->children[i];
    }
  }

  // Target node not found
  return NULL;
}

// Function to perform Depth-First Traversal and search for a specific node by
// its ID
Node *DFTWithSearch(Node *root, int targetId) {
  if (root == NULL)
    return NULL;

  // Perform search operation
  if (root->id == targetId) {
    // Target node found
    return root;
  }

  // Recursively traverse the children
  for (int i = 0; i < 10 && root->children[i] != NULL; ++i) {
    Node *found = DFTWithSearch(root->children[i], targetId);
    if (found != NULL) {
      // Target node found in one of the child subtrees
      return found;
    }
  }

  // Target node not found in the current subtree
  return NULL;
}

// Example usage
int main() {
  // Initialize the spa and wellness management system with some sample data
  Node *root = initializeSystem();

  // Perform Breadth-First Traversal
  printf("Breadth-First Traversal:\n");
  BFT(root);

  // Perform Depth-First Traversal
  printf("\nDepth-First Traversal:\n");
  DFT(root);

  // Perform Breadth-First Traversal with search operation
  int targetNodeId = 5;
  Node *foundNode = BFTWithSearch(root, targetNodeId);
  if (foundNode != NULL) {
    printf("\nNode with ID %d found using Breadth-First Traversal:\n",
           targetNodeId);
    printf("Node Name: %s\n", foundNode->name);
    printf("Node Type: %s\n", foundNode->type);
  } else {
    printf("\nNode with ID %d not found using Breadth-First Traversal\n",
           targetNodeId);
  }

  // Perform Depth-First Traversal with search operation
  targetNodeId = 7;
  foundNode = DFTWithSearch(root, targetNodeId);
  if (foundNode != NULL) {
    printf("\nNode with ID %d found using Depth-First Traversal:\n",
           targetNodeId);
    printf("Node Name: %s\n", foundNode->name);
    printf("Node Type: %s\n", foundNode->type);
  } else {
    printf("\nNode with ID %d not found using Depth-First Traversal\n",
           targetNodeId);
  }

  return 0;
}

#---Circular Linked list--


#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Structure to represent customer information
struct Customer {
    int id;
    char name[50];
    char service[50];
    struct Customer* next;
};

// Function to create a new customer node
struct Customer* createCustomer(int id, const char* name, const char* service) {
    struct Customer* newCustomer = (struct Customer*)malloc(sizeof(struct Customer));
    newCustomer->id = id;
    strcpy(newCustomer->name, name);
    strcpy(newCustomer->service, service);
    newCustomer->next = NULL;
    return newCustomer;
}

// Function to insert a new customer at the beginning of the circular linked list
struct Customer* insertBeginning(struct Customer* head, int id, const char* name, const char* service) {
    struct Customer* newCustomer = createCustomer(id, name, service);

    if (head == NULL) {
        // If the list is empty, make the new customer the head
        head = newCustomer;
        head->next = head;  // Point back to itself
    } else {
        // Traverse the list to find the last customer
        struct Customer* temp = head;
        while (temp->next != head) {
            temp = temp->next;
        }

        // Insert the new customer at the beginning
        newCustomer->next = head;
        head = newCustomer;
        temp->next = head;  // Update the last node to point to the new head
    }

    return head;
}

// Function to insert a new customer at the middle of the circular linked list
struct Customer* insertMiddle(struct Customer* head, int id, const char* name, const char* service) {
    struct Customer* newCustomer = createCustomer(id, name, service);

    if (head == NULL) {
        // If the list is empty, make the new customer the head
        head = newCustomer;
        head->next = head;  // Point back to itself
    } else {
        // Traverse the list to find the middle (approximate middle in case of an even number of nodes)
        struct Customer* slow = head;
        struct Customer* fast = head;

        while (fast->next != head && fast->next->next != head) {
            slow = slow->next;
            fast = fast->next->next;
        }

        // Insert the new customer at the middle
        newCustomer->next = slow->next;
        slow->next = newCustomer;
    }

    return head;
}

// Function to insert a new customer at the end of the circular linked list
struct Customer* insertEnd(struct Customer* head, int id, const char* name, const char* service) {
    struct Customer* newCustomer = createCustomer(id, name, service);

    if (head == NULL) {
        // If the list is empty, make the new customer the head
        head = newCustomer;
        head->next = head;  // Point back to itself
    } else {
        // Traverse the list to find the last customer
        struct Customer* temp = head;
        while (temp->next != head) {
            temp = temp->next;
        }

        // Insert the new customer at the end
        temp->next = newCustomer;
        newCustomer->next = head;  // Point back to the head
    }

    return head;
}

// Function to find the smallest ID in the circular linked list
int findSmallestID(struct Customer* head) {
    if (head == NULL) {
        return -1;  // Return -1 for an empty list (or another appropriate value)
    }

    int smallestID = head->id;
    struct Customer* current = head->next;

    // Traverse the circular linked list and find the smallest ID
    do {
        if (current->id < smallestID) {
            smallestID = current->id;
        }

        current = current->next;
    } while (current != head);

    return smallestID;
}

// Function to display the customer details in the circular linked list
void displayCustomers(struct Customer* head) {
    if (head == NULL) {
        printf("No customers in the Spa.\n");
        return;
    }

    struct Customer* current = head;

    // Traverse the circular linked list and display each customer's information
    do {
        printf("Customer ID: %d\n", current->id);
        printf("Name: %s\n", current->name);
        printf("Service: %s\n", current->service);
        printf("\n");

        current = current->next;
    } while (current != head);
}

// Function to free the memory allocated for the circular linked list of customers
void freeCustomers(struct Customer* head) {
    if (head == NULL) {
        return;
    }

    struct Customer* current = head;
    struct Customer* nextCustomer;

    // Traverse the circular linked list and free each customer node
    do {
        nextCustomer = current->next;
        free(current);
        current = nextCustomer;
    } while (current != head);
}

// Example usage
int main() {
    struct Customer* spaCustomers = NULL;

    // Add customers to the Spa and Wellness Management System
    spaCustomers = insertEnd(spaCustomers, 101, "Alice", "Massage");
    spaCustomers = insertEnd(spaCustomers, 102, "Bob", "Facial");
    spaCustomers = insertEnd(spaCustomers, 103, "Charlie", "Sauna");

    // Display the customers in the Spa
    printf("Customers in the Spa:\n");
    displayCustomers(spaCustomers);

    // Insert a customer at the beginning
    spaCustomers = insertBeginning(spaCustomers, 100, "NewCustomer", "Yoga");

    // Insert a customer in the middle
    spaCustomers = insertMiddle(spaCustomers, 104, "David", "Meditation");

    // Display the updated customers in the Spa
    printf("Updated Customers in the Spa:\n");
    displayCustomers(spaCustomers);

    // Find the smallest ID
    int smallestID = findSmallestID(spaCustomers);
    printf("Smallest Customer ID: %d\n", smallestID);

    // Free the memory allocated for the circular linked list of customers
    freeCustomers(spaCustomers);

    return 0;
}

#-------DE Queue----

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Structure to represent customer information
struct Customer {
    int id;
    char name[50];
    char service[50];
};

// Structure to represent a node in the deque
struct DequeNode {
    struct Customer customer;
    struct DequeNode* prev;
    struct DequeNode* next;
};

// Structure to represent the deque
struct Deque {
    struct DequeNode* front;
    struct DequeNode* rear;
};

// Function to create a new customer node
struct DequeNode* createNode(int id, const char* name, const char* service) {
    struct DequeNode* newNode = (struct DequeNode*)malloc(sizeof(struct DequeNode));
    newNode->customer.id = id;
    strcpy(newNode->customer.name, name);
    strcpy(newNode->customer.service, service);
    newNode->prev = newNode->next = NULL;
    return newNode;
}

// Function to initialize a deque
void initializeDeque(struct Deque* deque) {
    deque->front = deque->rear = NULL;
}

// Function to check if the deque is empty
int isEmpty(struct Deque* deque) {
    return (deque->front == NULL);
}

// Function to insert a customer at the front of the deque
void insertFront(struct Deque* deque, int id, const char* name, const char* service) {
    struct DequeNode* newNode = createNode(id, name, service);

    if (isEmpty(deque)) {
        deque->front = deque->rear = newNode;
    } else {
        newNode->next = deque->front;
        deque->front->prev = newNode;
        deque->front = newNode;
    }
}

// Function to insert a customer at the rear of the deque
void insertRear(struct Deque* deque, int id, const char* name, const char* service) {
    struct DequeNode* newNode = createNode(id, name, service);

    if (isEmpty(deque)) {
        deque->front = deque->rear = newNode;
    } else {
        newNode->prev = deque->rear;
        deque->rear->next = newNode;
        deque->rear = newNode;
    }
}

// Function to delete a customer from the front of the deque
struct Customer deleteFront(struct Deque* deque) {
    struct Customer emptyCustomer = { -1, "", "" };

    if (isEmpty(deque)) {
        printf("Deque is empty. Cannot delete from front.\n");
        return emptyCustomer;
    }

    struct DequeNode* temp = deque->front;
    struct Customer deletedCustomer = temp->customer;

    if (deque->front == deque->rear) {
        // If there's only one node in the deque
        deque->front = deque->rear = NULL;
    } else {
        deque->front = deque->front->next;
        deque->front->prev = NULL;
    }

    free(temp);
    return deletedCustomer;
}

// Function to delete a customer from the rear of the deque
struct Customer deleteRear(struct Deque* deque) {
    struct Customer emptyCustomer = { -1, "", "" };

    if (isEmpty(deque)) {
        printf("Deque is empty. Cannot delete from rear.\n");
        return emptyCustomer;
    }

    struct DequeNode* temp = deque->rear;
    struct Customer deletedCustomer = temp->customer;

    if (deque->front == deque->rear) {
        // If there's only one node in the deque
        deque->front = deque->rear = NULL;
    } else {
        deque->rear = deque->rear->prev;
        deque->rear->next = NULL;
    }

    free(temp);
    return deletedCustomer;
}

// Function to display the customers in the deque
void displayDeque(struct Deque* deque) {
    if (isEmpty(deque)) {
        printf("Deque is empty.\n");
        return;
    }

    struct DequeNode* current = deque->front;

    while (current != NULL) {
        printf("Customer ID: %d\n", current->customer.id);
        printf("Name: %s\n", current->customer.name);
        printf("Service: %s\n", current->customer.service);
        printf("\n");

        current = current->next;
    }
}

// Function to free the memory allocated for the deque
void freeDeque(struct Deque* deque) {
    while (!isEmpty(deque)) {
        deleteFront(deque);
    }
}

// Example usage
int main() {
    struct Deque customerDeque;
    initializeDeque(&customerDeque);

    // Insert customers into the deque
    insertFront(&customerDeque, 101, "Alice", "Massage");
    insertRear(&customerDeque, 102, "Bob", "Facial");
    insertFront(&customerDeque, 103, "Charlie", "Sauna");

    // Display the customers in the deque
    printf("Customers in the Deque:\n");
    displayDeque(&customerDeque);

    // Delete a customer from the front
    struct Customer deletedFrontCustomer = deleteFront(&customerDeque);
    if (deletedFrontCustomer.id != -1) {
        printf("Deleted Customer from Front:\n");
        printf("Customer ID: %d\n", deletedFrontCustomer.id);
        printf("Name: %s\n", deletedFrontCustomer.name);
        printf("Service: %s\n", deletedFrontCustomer.service);
    }

    // Delete a customer from the rear
    struct Customer deletedRearCustomer = deleteRear(&customerDeque);
    if (deletedRearCustomer.id != -1) {
        printf("Deleted Customer from Rear:\n");
        printf("Customer ID: %d\n", deletedRearCustomer.id);
        printf("Name: %s\n", deletedRearCustomer.name);
        printf("Service: %s\n", deletedRearCustomer.service);
    }

    // Display the updated customers in the deque
    printf("Updated Customers in the Deque:\n");
    displayDeque(&customerDeque);

    // Free the memory allocated for the deque
    freeDeque(&customerDeque);

    return 0;
}

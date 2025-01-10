![](https://giphy.com/stickers/thecodingspacerd-technology-thecodingspace-codingspace-Tgw604MyLJnDtbi4t0)

---
### **1️⃣ Array** 

| **LA[]** | **<font color="#f79646"><u>Your Array</u></font>**                            |
| -------- | ----------------------------------------------------------------------------- |
| **i**    | **<font color="#f79646"><u>Counter</u></font>**                               |
| **K**    | **<font color="#f79646"><u>Position We need To Insert element</u></font>**    |
| **N**    | **<font color="#f79646"><u>Number Of Elements</u></font>**                    |
| **Item** | **<font color="#f79646"><u>Elements We Need To Insert into Array</u></font>** |

---
##### **Insertion Operation ** 
```cpp
#include <iostream>

using namespace std;

int main()

{

    int LA[] = {1, 3, 5, 7, 8};
    int k = 3, n = 4, item = 10;
    int i = 0, j = n - 1;

    cout << endl;
    cout << "________ The Original Array _______" << endl;
    cout << endl;

    for (int i = 0; i < 5; i++)

    {
        cout << " The Index => " << i << " " << " The Elements = " << LA[i] << endl;
    }

    cout << endl;

    cout << "_______ The Array After Insertion _____ " << endl;

    cout << endl;

    n = n + 1;

    while (j >= k)
    {
        LA[j + 1] = LA[j];
        j = j - 1;
    }

    LA[k] = item;
    for (int i = 0; i < n; i++)
    {
        cout << "The Index => " << i << " " << " The Elements = " << LA[i] << endl;
    }

}
```
---
###### **Deletion Operation  **
```cpp
#include <iostream>
using namespace std;
int main()
{
    int LA[] = {2, 4, 6, 8, 10, 11};

    int k = 8, n = 6;

    int i, j = k;

    cout << "___________ The Orginal Array ___________" << endl;
    cout << endl;
    
    for (int i = 0; i < 6; i++)
    {
        cout << " The Index =>  " << i << " " << " The Element =   " << LA[i] << endl;
    }
    
    cout << endl;
    cout << "__________ After Deletion ______________" << endl;
    cout << endl;
    
    while (j < n)

    {
        LA[j - 1] = LA[j];
        j = j - 1;
    }
   
    n = n - 1;
    for (int i = 0; i < n; i++)
    {
        cout << " The Index => " << i << " " << " The New Elements  = " << LA[i] << endl;
    }
}

```
---
###### **Search Operation **
```cpp
#include <iostream>
using namespace std;

// Search Operation
int main()

{

    int LA[] = {1, 3, 5, 7, 8};
    int item = 5, n = 5;
    int i, j = 0;

    cout << endl;

    cout << "_________ The Original Array __________ " << endl;

    cout << endl;

    for (int i = 0; i < 5; i++)
    {

        cout << " The Index => " << i << " " << " The Elements =  " << LA[i] << endl;
    }

    cout << endl;

    cout << " __________  Out Put After Search  ________ " << endl;

    cout << endl;

    while (j < n)

    {
        if (LA[j] == 8)

        {
            cout << " Found The Elements  = " << 8 << j + 1;
            break;
        }
        j = j + 1;
    }
    
    if (j == n)
    {
        cout << " Item Not Fond in Array " << endl;
    }

    return 0;

}
```

---
###### **Update Operation **

```cpp
#include <iostream>
using namespace std;
// Update  Operation

int main()

{

    int LA[] = {1, 3, 5, 7, 8};
    int k = 3, n = 5, item = 10;
    int i, j;

    cout << endl;

    cout << "_______ The Original Array ________ " << endl;

    cout << endl;

    for (int i = 0; i < 4; i++)
    {
        cout << " The Index = " << i << " " << " The Elemnats  " << LA[i] << endl;
    }
    
    cout << endl;

    cout << "________ The Array After Update ________ " << endl;

    cout << endl;
    
    LA[k - 1] = item;
    for (int i = 0; i < n; i++)

    {
        cout << " The Index => " << i << " " << " The Elemnats  " << LA[i] << endl;
    }
}
```

---
###### **Linear Search** 
```cpp
#include <iostream>

using namespace std;

int main()

{
    int array[100], search, c, n;
    cout << "Enter number of elements in array \n";
    cin >> n;

    cout << "Enter integer(s) \n"
         << n;

    for (c = 0; c < n; c++)

    {

        cin >> array[c];

        cout << "Enter a number to search \n";

        cin >> search;

        for (c = 0; c < n; c++)

        {
            if (array[c] == search)

            {
                cout << search << " is present at location " << c + 1;

                break;

            }

        }
        if (c == n)

            cout << search << " isn't present in the array. \n";

        return 0;

    }

}

```

---
###### **Binary Searching**
```cpp
#include <iostream>

using namespace std;

// Binary Search

int main()

{

    cout << "____ Welcome in Binary Search Programme ____ " << endl;
    
    // Variable We need

    int c, first, middel, last, n, search, LA[100];
    cout << endl;

    cout << "_______ Enter The Element _______ " << endl;

    cout << endl;

    cin >> n;

    cout << " The  Number of (n)  =>  " << n;
    
    for (int c = 0; c < n; c++)

    {

        cin >> LA[c];

        cout << "Enter Value To Find The Element  ";

        cin >> search;

        first = 0;

        last = n - 1;

        middel = (first + last) / 2;

    }

    while (first <= last)

    {

        if (LA[middel] < search)

        {

            first = middel + 1;

        }

        else if (LA[middel] == search)

        {

            cout << " The Location :  " << search << middel + 1 << endl;

            break;

        }

        else

        {

            last = middel - 1;

            middel = (first + last) / 2;

        }

        if (first > last)

        {

            cout << "The Element Not Found : " << search << endl;

        }

  

        return 0;

    }

}
```

---
###### **Bubble Sort** 
```cpp
#include <iostream>

#define MAXSIZE 10

using namespace std;

int main()
{
    int array[MAXSIZE];
    int i, j, num, temp;

    cout << "Enter the value of num \n";

    cin >> num;

    cout << "Enter the elements one by one \n";

    for (i = 0; i < num; i++)

    {

        cin >> array[i];

    }

    for (i = 0; i < (num - i - 1); i++)

    {

        for (j = 0; j < (num - i - 1); j++)

        {

            if (array[j] > array[j + 1])

            {

                temp = array[j];

                array[j] = array[j + 1];

                array[i + 1] = temp;

            }

        }

    }

    cout << "Sorted arrau is ...\n";

    for (i = 0; i < num; i++)

    {

        cout << array[i] << "\n";

    }

}
```
---
###### **Selection Sort** 
```cpp
#include <iostream>

using namespace std;

void selectionSort(int arr[], int size);
void swap(int *a, int *b);
void selectionSort(int arr[], int size)
{
    int i, j;
    for (i = 0; j < size;i++)
    {

        for (i = 0; i < size;i++)

        {

            for (j = i; j < size;j++)

            {

                if (arr[i] > arr[j])

                    swap(&arr[i], &arr[j]);

            }

        }

    }

}

void swap(int *a, int *b)

{

    int temp;

    temp = *a;

    *a = *b;

    *b = temp;

}

int main()

{

    int array[10], i, size;

    cout << "How many numbers you want to sort : ";

    cin >> size;

    cout << "\n Enter " << size << "numbers \t";

    cout << "\n";

    for (i = 0; i < size;i++)

        cin >> array[i];

    selectionSort(array, size);

    cout << "\n SOrted array is ";

    for (i = 0; i < size;i++)

        cout << array[i];

    int mm;

    cin >> mm;

    return 0;

}
```
---
###### **Insertion Sort** 

```cpp
#include <iostream>

using namespace std;

int main(void)

{

    int n, i, j, temp;

    int arr[64];

    cout << "Enter number of elements \n";

    cin >> n;

    cout << "Enter" << n << "integers";

    for (i = 0; i < n; i++)

    {

        cin >> arr[i];

    }

    for (i = 1; i < n; i++)

    {

        j = i;

        while (j > 0 && arr[j - 1] > arr[j])

        {

            temp = arr[j];

            arr[j] = arr[j - 1];

            arr[j - 1] = temp;

            j--;

        }

    }

    cout << "Sorted List in ascending order :\n";

    for (i = 0; i < n; i++)

    {

        cout << "\n"

             << arr[i];

    }

    return 0;

}

```
---
## **2️⃣ Stack 🤖**
###### **Structure**
```cpp
#include <iostream>
using namespace std ;

struct emp // create of strucut emp
{
    char name[25];
    int age;
    float salary;
};

int main() 
{
    struct emp e; //
    cout << "\n Enter the name , age and salary " ;
    cin >> e.name ;
    cin >> e.age >> e.salary ;
    cout << "\n Name is " << e.name << "\n age is " << e.age << "\n salary is " << e.salary ;
}
```
---
```cpp
int Peek() 
{
    return stack[top];
}
```
---
##### **push**
```cpp
تضيف عنصرًا إلى المكدس إذا كان هناك مكان متاح

void push(int value) {
    if (top == 5) {  // إذا كان المكدس ممتلئًا (الحد الأقصى للعناصر هو 5)
        cout << "Error: Overflow\n";  // رسالة خطأ إذا حاولنا إضافة عنصر في مكدس ممتلئ
    } else {
        stack[top] = value;  // إضافة القيمة إلى المكدس في الموقع الحالي الذي يشير إليه "top"
        top++;  // زيادة قيمة "top" لتحديد مكان العنصر التالي في المكدس
    }
}
```
---
###### **Pop** 
```cpp
تقوم بحذف العنصر العلوي من المكدس وإرجاعه

int pop() {
    if (top == 0) {  // إذا كان المكدس فارغًا (الـ "top" يساوي 0)
        cout << "Error: Underflow.\n";  // رسالة خطأ إذا حاولنا حذف عنصر من مكدس فارغ
        return -1;  // إرجاع قيمة غير صحيحة للدلالة على وجود خطأ
    } else {
        top--;  // تقليل قيمة "top" لتحديد الموقع الذي سيتم حذفه
        return stack[top];  // إرجاع العنصر الذي كان في أعلى المكدس
    }
}
```
---
######  **Stack_implementation**
```cpp
#include <iostream>  
using namespace std; 

int stack[5];  // تعريف مصفوفة مكدس (Stack) بسعة 5 عناصر
int top = 0;  // تعريف المتغير top الذي يشير إلى الموضع الحالي في المكدس

// تعريف دوال المكدس
void push(int value);  // Stack دالة لإدخال قيمة إلى ال 
int pop();  // دالة لإزالة العنصر العلوي من المكدس
void traverse();  // دالة لعرض كل العناصر في المكدس
int is_empt();  // دالة للتحقق إذا كان المكدس فارغًا
int top_element();  // دالة لإرجاع العنصر العلوي في المكدس

int main() {
    int element, choice;  // تعريف متغيرات لاستقبال المدخلات من المستخدم

    // التكرار اللانهائي لاستقبال المدخلات وتنفيذ العمليات
    for (;;) {
        // عرض الخيارات المتاحة للمستخدم
        cout << "1. Insert into stack (Push operation).\n";
        cout << "2. Delete from stack (Pop operation).\n";
        cout << "3. Print top element of stack.\n";
        cout << "4. Check if stack is empty.\n";
        cout << "5. Traverse stack.\n";
        cout << "6. Exit.\n";
        cout << "Enter your choice: ";
        cin >> choice;  // استقبال الخيار من المستخدم

        switch (choice)  // التحقق من الخيار الذي اختاره المستخدم
        {
        case 1:
            // إذا كان المكدس ممتلئًا
            if (top == 5) {
                cout << "Error: Overflow\n\n";  // المكدس ممتلئ
            }
            else {
                cout << "Enter a value to insert: ";
                cin >> element;  // استقبال العنصر لإضافته إلى المكدس
                push(element);  // إضافة العنصر إلى المكدس
            }
            break;
        case 2:
            // إذا كان المكدس فارغًا
            if (top == 0) {
                cout << "Error: Underflow.\n";  // المكدس فارغ
            }
            else {
                element = pop();  // إزالة العنصر العلوي من المكدس
                cout << "Element removed from the stack is: " << element << "\n";  // عرض العنصر الذي تم إزالته
            }
            break;
        case 3:
            // إذا لم يكن المكدس فارغًا
            if (!is_empt()) {
                element = top_element();  // الحصول على العنصر العلوي
                cout << "Element at the top of the stack is: " << element << "\n";  // عرض العنصر العلوي
            }
            else {
                cout << "The stack is empty.\n\n";  // إذا كان المكدس فارغًا
            }
            break;
        case 4:
            // التحقق إذا كان المكدس فارغًا
            if (is_empt()) {
                cout << "The stack is empty.\n\n";  // المكدس فارغ
            }
            else {
                cout << "The stack isn't empty.\n\n";  // المكدس يحتوي على عناصر
            }
            break;
        case 5:
            traverse();  // عرض العناصر في المكدس
            break;
        case 6:
            exit(0);  // إيقاف البرنامج
            break;
        default:
            cout << "Invalid choice. Please try again.\n";  // خيار غير صحيح
        }
    }
}

// دالة لإدخال عنصر إلى المكدس
void push(int value) {
    stack[top] = value;  // إضافة القيمة إلى المكان الحالي في المصفوفة
    top++;  // زيادة قيمة top للإشارة إلى العنصر التالي في المكدس
}

// دالة لإزالة العنصر العلوي من المكدس وإرجاعه
int pop() {
    top--;  // تقليل قيمة top للإشارة إلى العنصر الذي سيتم إزالته
    return stack[top];  // إرجاع العنصر الذي كان في أعلى المكدس
}

// دالة لعرض كل العناصر في المكدس
void traverse() {
    int d;
    // إذا كان المكدس فارغًا
    if (top == 0) {
        cout << "The stack is empty.\n\n";  // إذا كان المكدس فارغًا
        return;
    }
    // إذا كان المكدس يحتوي على عناصر، عرض كل العناصر من الأعلى إلى الأسفل
    cout << "There are " << top << " elements in the stack:\n";
    for (d = top - 1; d >= 0; d--) {  // التكرار من أعلى المكدس إلى أسفله
        cout << stack[d] << "\n";  // عرض العنصر في المكدس
    }
}

// دالة للتحقق إذا كان المكدس فارغًا
int is_empt() {
    return top == 0;  // إرجاع 1 إذا كان المكدس فارغًا، و0 إذا كان يحتوي على عناصر
}

// دالة لإرجاع العنصر الموجود في أعلى المكدس
int top_element() {
    return stack[top - 1];  // إرجاع العنصر الذي في أعلى المكدس
}
```
---
## **3️⃣ Linked List**
```cpp
#include <iostream> // تضمين مكتبة الإدخال والإخراج
using namespace std;

// تعريف هيكلية العقدة
struct node {
    int data;             // تخزين البيانات
    int key;              // المفتاح الفريد للعقدة
    struct node* next;    // مؤشر للعقدة التالية
};

// تعريف رأس القائمة
struct node* head = NULL; // الرأس يبدأ كـ NULL لأن القائمة فارغة

// وظيفة لإضافة عقدة جديدة في بداية القائمة
void insertFirst(int key, int data) {
    struct node* link = new node; // إنشاء عقدة جديدة باستخدام "new"
    link->key = key;             // تعيين المفتاح
    link->data = data;           // تعيين البيانات
    link->next = head;           // الإشارة إلى الرأس الحالي
    head = link;                 // تحديث الرأس ليشير إلى العقدة الجديدة
}

// وظيفة لطباعة القائمة
void printList() {
    struct node* ptr = head;     // البدء من الرأس
    cout << "\n[ ";
    while (ptr != NULL) {        // التنقل عبر القائمة حتى الوصول إلى النهاية
        cout << ptr->key << " , " << ptr->data << "\t"; // طباعة المفتاح والبيانات
        ptr = ptr->next;         // الانتقال إلى العقدة التالية
    }
    cout << " ]";
}

// وظيفة لحذف العقدة الأولى
struct node* deleteFirst() {
    if (head == NULL) {          // التحقق إذا كانت القائمة فارغة
        cout << "List is empty." << endl;
        return NULL;
    }
    struct node* tempLink = head; // حفظ العقدة الحالية ليتم حذفها
    head = head->next;            // تحديث الرأس ليشير إلى العقدة التالية
    delete tempLink;              // تحرير ذاكرة العقدة المحذوفة
    return head;
}

// وظيفة للتحقق مما إذا كانت القائمة فارغة
bool isEmpty() {
    return head == NULL;          // إذا كان الرأس NULL، القائمة فارغة
}

// وظيفة لحساب طول القائمة
int length() {
    int length = 0;               // عداد الطول
    struct node* current = head;  // البدء من الرأس
    while (current != NULL) {     // التنقل عبر القائمة
        length++;                 // زيادة العداد
        current = current->next;  // الانتقال إلى العقدة التالية
    }
    return length;                // إرجاع الطول
}

// وظيفة للبحث عن عقدة باستخدام المفتاح
struct node* find(int key) {
    struct node* current = head;  // البدء من الرأس
    if (head == NULL) {           // إذا كانت القائمة فارغة
        return NULL;
    }
    while (current->key != key) { // البحث عن المفتاح
        if (current->next == NULL) { // إذا لم يتم العثور على المفتاح
            return NULL;
        }
        current = current->next;  // الانتقال إلى العقدة التالية
    }
    return current;               // إرجاع العقدة التي تحتوي على المفتاح
}

// وظيفة لحذف عقدة باستخدام المفتاح
struct node* delet(int key) {
    struct node* current = head;  // البدء من الرأس
    struct node* previous = NULL; // عقدة مؤقتة للعقدة السابقة
    if (head == NULL) {           // إذا كانت القائمة فارغة
        return NULL;
    }
    while (current->key != key) { // البحث عن المفتاح
        if (current->next == NULL) { // إذا لم يتم العثور على المفتاح
            return NULL;
        }
        previous = current;       // تحديث العقدة السابقة
        current = current->next;  // الانتقال إلى العقدة التالية
    }
    if (current == head) {        // إذا كانت العقدة هي الرأس
        head = head->next;        // تحديث الرأس ليشير إلى العقدة التالية
    } else {
        previous->next = current->next; // تجاوز العقدة المحذوفة
    }
    delete current;               // تحرير ذاكرة العقدة المحذوفة
    return head;
}

// وظيفة لترتيب القائمة بناءً على البيانات
void sort() {
    int tempKey, tempData;        // متغيرات مؤقتة لتبديل البيانات
    struct node* current;
    struct node* next;
    int size = length();          // حساب طول القائمة
    for (int i = 0; i < size - 1; i++) { // دورة خارجية للمرور عبر القائمة
        current = head;           // البدء من الرأس
        next = head->next;        // العقدة التالية
        while (next != NULL) {    // التنقل عبر القائمة
            if (current->data > next->data) { // إذا كانت البيانات غير مرتبة
                // تبديل البيانات
                tempData = current->data;
                current->data = next->data;
                next->data = tempData;

                tempKey = current->key;
                current->key = next->key;
                next->key = tempKey;
            }
            current = next;       // الانتقال إلى العقدة التالية
            next = next->next;
        }
    }
}

// الدالة الرئيسية
int main() {
    // إضافة عقد إلى القائمة
    insertFirst(1, 10);
    insertFirst(2, 20);
    insertFirst(3, 30);

    // طباعة القائمة
    cout << "Initial List: ";
    printList();

    // حذف العقدة الأولى
    cout << "\nDeleting first node." << endl;
    deleteFirst();
    printList();

    // البحث عن عقدة بمفتاح معين
    cout << "\nFinding node with key 2." << endl;
    struct node* found = find(2);
    if (found != nullptr) { // إذا تم العثور على العقدة
        cout << "Found node: (" << found->key << ", " << found->data << ")" << endl;
    } else {
        cout << "Node not found." << endl;
    }

    // ترتيب القائمة
    cout << "\nSorting the list." << endl;
    sort();
    printList();

    return 0;
}
```
---
## 4️⃣**Tree** 
```cpp
#include <iostream>  
using namespace std; 

/* تعريف هيكل الشجرة (Node structure) */
struct node {
    int value;  // قيمة العقدة (بيانات العقدة)
    struct node* left_child, * right_child;  // مؤشرات للعقدة اليسرى والعقدة اليمنى
};

// دالة لإنشاء عقدة جديدة في الشجرة
struct node* new_node(int value) {
    struct node* tmp = new struct node;  // تخصيص ذاكرة لعقدة جديدة باستخدام "new" بدلاً من malloc (طريقة أكثر أمانًا في C++)
    tmp->value = value;  // تعيين القيمة للعقدة
    tmp->left_child = tmp->right_child = NULL;  // تعيين المؤشرات للعقدة اليسرى واليمنى إلى NULL (بداية الشجرة تكون فارغة)
    return tmp;  // إرجاع المؤشر إلى العقدة الجديدة
}

// دالة للطباعة (التجول في الشجرة بنمط الترتيب التزايدي Inorder)
void print(struct node* root_node) {
    if (root_node != NULL) {  // إذا كانت العقدة غير فارغة
        print(root_node->left_child);  // أولاً، طباعة الشجرة اليسرى
        cout << " " << root_node->value;  // ثم طباعة قيمة العقدة
        print(root_node->right_child);  // أخيرًا، طباعة الشجرة اليمنى
    }
}

// دالة لإدخال قيمة جديدة في الشجرة الثنائية
struct node* insert_node(struct node* node, int value) {
    if (node == NULL) return new_node(value);  // إذا كانت الشجرة فارغة (أو عقدة فارغة)، قم بإنشاء عقدة جديدة بالقيمة المعطاة

    if (value < node->value) {  // إذا كانت القيمة أصغر من قيمة العقدة الحالية، أدخل القيمة في الشجرة اليسرى
        node->left_child = insert_node(node->left_child, value);
    }
    else if (value > node->value) {  // إذا كانت القيمة أكبر من قيمة العقدة الحالية، أدخل القيمة في الشجرة اليمنى
        node->right_child = insert_node(node->right_child, value);
    }
    
    // لا نفعل شيء إذا كانت القيمة مكررة (يمكنك إضافة check هنا إذا أردت منع القيم المكررة)

    return node;  // إرجاع العقدة الحالية بعد إضافة القيمة
}

int main() {
    cout << "Tech Vidvan Tutorial : Implementation of a Binary Tree in C++! \n\n";  // طباعة رسالة توضيحية للمستخدم

    struct node* root_node = NULL;  // بداية الشجرة فارغة
    root_node = insert_node(root_node, 10);  // إضافة القيمة 10 في الشجرة
    insert_node(root_node, 10);  // إضافة قيمة مكررة 10 (سيتم قبولها في الكود الحالي)
    insert_node(root_node, 30);  // إضافة القيمة 30 في الشجرة
    insert_node(root_node, 25);  // إضافة القيمة 25 في الشجرة
    insert_node(root_node, 36);  // إضافة القيمة 36 في الشجرة
    insert_node(root_node, 56);  // إضافة القيمة 56 في الشجرة
    insert_node(root_node, 78);  // إضافة القيمة 78 في الشجرة

    print(root_node);  // طباعة الشجرة بعد إضافة القيم
    return 0;  
}
```
---
## **5️⃣ Graph** 
###### **BFS**
```cpp
#include <stdio.h>  // تضمين مكتبة الإدخال/الإخراج لطباعة النصوص
#include <stdlib.h>  // تضمين مكتبة العمليات العامة مثل تخصيص الذاكرة
#include <stdbool.h>  // تضمين مكتبة القيم البوليانية (true/false)
#define MAX 5  // تعريف الحد الأقصى لعدد الرؤوس في الرسم البياني

// تعريف هيكل Vertex الذي يمثل الرأس في الرسم البياني
struct Vertex {
    char label;  // تسمية الرأس (مثل 'S', 'A', 'B' ...)
    bool visited;  // علم يشير إذا كان الرأس قد تم زيارته أثناء البحث
};

// تعريف مصفوفة لحفظ عناصر الصف
int queue[MAX];  // مصفوفة للصف بحد أقصى MAX
int rear = -1;  // مؤشر نهاية الصف
int front = 0;  // مؤشر بداية الصف
int queueItemCount = 0;  // عدد العناصر في الصف

// مصفوفة لتخزين رؤوس الرسم البياني
struct Vertex* lstVertices[MAX];  // مصفوفة تحتوي على مؤشرات للرؤوس

// مصفوفة الجوار التي تمثل الرسم البياني
int adjMatrix[MAX][MAX];  // مصفوفة لتمثيل العلاقات بين الرؤوس (مصفوفة الجوار)

int vertexCount = 0;  // عداد الرؤوس في الرسم البياني

// دالة لإدراج عنصر في الصف
void insert(int data) {
    queue[++rear] = data;  // إضافة عنصر في نهاية الصف
    queueItemCount++;  // زيادة عدد العناصر في الصف
}

// دالة لإزالة عنصر من الصف
int removeData() {
    queueItemCount--;  // تقليل عدد العناصر في الصف
    return queue[front++];  // إزالة العنصر من بداية الصف
}

// دالة للتحقق مما إذا كان الصف فارغًا
bool isQueueEmpty() {
    return queueItemCount == 0;  // إذا كان عدد العناصر صفرًا فإن الصف فارغ
}

// دالة لإضافة رأس إلى الرسم البياني
void addVertex(char label) {
    struct Vertex* vertex = (struct Vertex*)malloc(sizeof(struct Vertex));  // تخصيص ذاكرة لرأس جديد
    vertex->label = label;  // تعيين التسمية للرأس
    vertex->visited = false;  // تعيين أن الرأس لم يُزر بعد
    lstVertices[vertexCount++] = vertex;  // إضافة الرأس إلى المصفوفة وزيادة عداد الرؤوس
}

// دالة لإضافة حافة بين رأسين
void addEdge(int start, int end) {
    adjMatrix[start][end] = 1;  // تعيين قيمة 1 في المصفوفة لتشير إلى وجود حافة بين الرأسين
    adjMatrix[end][start] = 1;  // لأن الرسم البياني غير موجه
}

// دالة لعرض رأس معين
void displayVertex(int vertexIndex) {
    printf("%c ", lstVertices[vertexIndex]->label);  // طباعة التسمية الخاصة بالرأس
}

// دالة لإيجاد رأس غير مزار في الجوار
int getAdjUnvisitedVertex(int vertexIndex) {
    int i;
    for (i = 0; i < vertexCount; i++) {
        if (adjMatrix[vertexIndex][i] == 1 && lstVertices[i]->visited == false) {
            return i;  // إذا كان هناك حافة ولم يتم زيارة الرأس بعد، إرجاع المؤشر
        }
    }
    return -1;  // إذا لم توجد رؤوس غير مزارة في الجوار
}

// دالة تنفيذ البحث باستخدام العرض الأول (BFS)
void breadthFirstSearch() {
    int i;
    lstVertices[0]->visited = true;  // تعيين الرأس الأول كمزار
    displayVertex(0);  // عرض الرأس الأول
    insert(0);  // إضافة الرأس الأول إلى الصف

    int unvisitedVertex;
    while (!isQueueEmpty()) {  // طالما أن الصف ليس فارغًا
        int tempVertex = removeData();  // إزالة رأس من الصف
        while ((unvisitedVertex = getAdjUnvisitedVertex(tempVertex)) != -1) {  // العثور على رأس غير مزار في الجوار
            lstVertices[unvisitedVertex]->visited = true;  // تعيين الرأس كمزار
            displayVertex(unvisitedVertex);  // عرض الرأس
            insert(unvisitedVertex);  // إضافة الرأس إلى الصف
        }
    }

    // إعادة تعيين كافة الرؤوس كغير مزارة بعد انتهاء البحث
    for (i = 0; i < vertexCount; i++) {
        lstVertices[i]->visited = false;
    }
}

// دالة main لتنفيذ البرنامج
int main() {
    int i, j;
    for (i = 0; i < MAX; i++) {
        for (j = 0; j < MAX; j++) {
            adjMatrix[i][j] = 0;  // تهيئة مصفوفة الجوار لتكون كلها 0 (لا توجد حواف في البداية)
        }
    }

    // إضافة الرؤوس إلى الرسم البياني
    addVertex('S');
    addVertex('A');
    addVertex('B');
    addVertex('C');
    addVertex('D');

    // إضافة الحواف بين الرؤوس
    addEdge(0, 1);
    addEdge(0, 2);
    addEdge(0, 3);
    addEdge(1, 4);
    addEdge(2, 4);
    addEdge(3, 4);

    // تنفيذ البحث باستخدام العرض الأول (BFS)
    printf("Breadth First Search: ");
    breadthFirstSearch();

    return 0; 
}
```
###### **DFS**
```cpp
#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>
#define MAX 5

// تعريف هيكل يمثل العقدة (Vertex) في الرسم البياني
struct Vertex {
    char lable;   // الحرف الذي يمثل العقدة
    bool visited; // لمعرفة إذا تمت زيارة هذه العقدة أثناء البحث
};

// تعريف stack (مكدس) لتتبع العقد أثناء البحث
int stack[MAX];
int top = -1; // مؤشر أعلى عنصر في المكدس

// قائمة لحفظ كل العقد في الرسم البياني
struct Vertex* lstVertices[MAX];

// مصفوفة التلاصق لتمثيل العلاقات بين العقد
int adjMatrix[MAX][MAX];

// عدد العقد الموجودة في الرسم البياني
int vertexCount = 0;

// دالة لدفع عنصر جديد إلى المكدس
void push(int item) {
    stack[++top] = item;
}

// دالة لإزالة العنصر العلوي من المكدس
int pop() {
    return stack[top--];
}

// دالة للحصول على العنصر العلوي من المكدس دون إزالته
int peek() {
    return stack[top];
}

// دالة للتحقق إذا كان المكدس فارغًا
bool isStackEmpty() {
    return top == -1;
}

// دالة لإضافة عقدة جديدة إلى الرسم البياني
void addVertex(char lable) {
    struct Vertex* vertex = new Vertex; // تخصيص ذاكرة للعقدة الجديدة
    vertex->lable = lable;              // تعيين الحرف الذي يمثل العقدة
    vertex->visited = false;            // لم يتم زيارتها بعد
    lstVertices[vertexCount++] = vertex; // إضافتها إلى قائمة العقد
}

// دالة لإضافة حافة (Edge) بين عقدتين
void addEdge(int start, int end) {
    adjMatrix[start][end] = 1; // تعيين 1 في مصفوفة التلاصق لتمثيل وجود علاقة
    adjMatrix[end][start] = 1; // تمثيل العلاقة في الاتجاه الآخر لأن الرسم ثنائي الاتجاه
}

// دالة لطباعة العقدة بناءً على الفهرس
void displayVertex(int vertexIndex) {
    printf("%c", lstVertices[vertexIndex]->lable);
}

// دالة للحصول على العقدة المجاورة غير المزارة
int getAdjUnvisitedVertex(int vertexIndex) {
    int i;
    for (i = 0; i < vertexCount; i++) {
        // تحقق إذا كانت هناك علاقة ولم تتم زيارة العقدة
        if (adjMatrix[vertexIndex][i] == 1 && lstVertices[i]->visited == false) {
            return i;
        }
    }
    return -1; // إذا لم توجد عقدة مجاورة غير مزارة
}

// دالة للبحث المتعمق (Depth First Search)
void depthFirstSearch() {
    int i;
    lstVertices[0]->visited = true; // بدء البحث من العقدة الأولى
    displayVertex(0);               // طباعة العقدة الأولى
    push(0);                        // إضافتها إلى المكدس

    // أثناء وجود عناصر في المكدس
    while (!isStackEmpty()) {
        int unvisitedVertex = getAdjUnvisitedVertex(peek()); // احصل على العقدة المجاورة غير المزارة
        if (unvisitedVertex == -1) {
            pop(); // إذا لم توجد عقدة، أزل العقدة من المكدس
        }
        else {
            lstVertices[unvisitedVertex]->visited = true; // علم العقدة كمزارة
            displayVertex(unvisitedVertex);               // طباعة العقدة
            push(unvisitedVertex);                        // أضفها إلى المكدس
        }
    }

    // إعادة تعيين كل العقد كغير مزارة بعد البحث
    for (i = 0; i < vertexCount; i++) {
        lstVertices[i]->visited = false;
    }
}

int main() {
    int i, j;

    // تهيئة مصفوفة التلاصق إلى 0
    for (i = 0; i < MAX; i++) {
        for (j = 0; j < MAX; j++) {
            adjMatrix[i][j] = 0;
        }
    }

    // إضافة العقد إلى الرسم البياني
    addVertex('S'); // العقدة S
    addVertex('A'); // العقدة A
    addVertex('B'); // العقدة B
    addVertex('C'); // العقدة C
    addVertex('D'); // العقدة D

    // إضافة الحواف بين العقد
    addEdge(0, 1); // حافة بين S و A
    addEdge(0, 2); // حافة بين S و B
    addEdge(0, 3); // حافة بين S و C
    addEdge(1, 4); // حافة بين A و D
    addEdge(2, 4); // حافة بين B و D
    addEdge(3, 4); // حافة بين C و D

    // بدء البحث المتعمق
    printf("Depth First Search : ");
    depthFirstSearch();

    return 0;
}
```

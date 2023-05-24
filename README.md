#include <stdio.h>
 main() {
    int a[] = {1, 2, 3};
    int b[] = {10, 20, 30};
    int size_a = sizeof(a) / sizeof(a[0]);
    int size_b = sizeof(b) / sizeof(b[0]);
    int size_c = size_a + size_b;
    int c[size_c];
    int i, j;
    for (i = 0; i < size_a; i++) {
        c[i] = a[i];
    }
    for (j = 0; j < size_b; j++) {
        c[i++] = b[j];
    }
    printf("Merged array: ");
    for (i = 0; i < size_c; i++) {
        printf("%d ", c[i]);
    }
    return 0;
}

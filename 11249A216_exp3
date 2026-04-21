#include <stdio.h>
#define MAX 50
int main()
{
    int n, i, j;
    int weight[MAX], bin[MAX];
    int capacity;
    printf("Enter number of items: ");
    scanf("%d", &n);
    printf("Enter weights of items:\n");
    for(i = 0; i < n; i++)
    {
        scanf("%d", &weight[i]);
    }
    printf("Enter capacity of each bin: ");
    scanf("%d", &capacity);
    int bin_count = 0;
    // Initialize bins
    for(i = 0; i < n; i++)
        bin[i] = capacity;
    // First Fit Algorithm
    for(i = 0; i < n; i++)
    {
        for(j = 0; j < bin_count; j++)
        {
            if(bin[j] >= weight[i])
            {
                bin[j] -= weight[i];
                break;
            }
        }
        // If item not placed in any bin
        if(j == bin_count)
        {
            bin[bin_count] = capacity - weight[i];
            bin_count++;
        }
    }

    printf("\nNumber of bins required: %d\n", bin_count);

    return 0;
}

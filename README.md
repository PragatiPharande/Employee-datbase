# Employee-datbase
Employee database of college cleaning  staff
PROGRAM CODE:
#include <stdio.h>

struct CleaningStaff {
    char name[30];
    char work_type[30];
    int working_hours;
    int extra_work_days;
    int off_days;
    int basic_salary;
};

int main() {
    int i, j, n;

    printf("Enter number of cleaning staff: ");
    scanf("%d", &n);

    struct CleaningStaff S1[n], temp;

    // Input data
    for(i = 0; i < n; i++) {
        printf("\n--- Enter Details for Staff %d ---\n", i+1);

        printf("Enter Name: ");
        scanf("%s", S1[i].name);

        printf("Enter Work Type (Floor/Washroom/Classroom): ");
        scanf("%s", S1[i].work_type);

        printf("Enter Working Hours per Day: ");
        scanf("%d", &S1[i].working_hours);

        printf("Enter Extra Working Days: ");
        scanf("%d", &S1[i].extra_work_days);

        printf("Enter Off Days: ");
        scanf("%d", &S1[i].off_days);

        printf("Enter Basic Salary: ");
        scanf("%d", &S1[i].basic_salary);
    }

   
    for(i = 0; i < n - 1; i++) {
        for(j = 0; j < n - i - 1; j++) {
            if(S1[j].basic_salary < S1[j+1].basic_salary) {
                temp = S1[j];
                S1[j] = S1[j+1];
                S1[j+1] = temp;
            }
        }
    }


    printf("\n================ STAFF DETAILS (Sorted by Salary DESCENDING) ================\n");

    for(i = 0; i < n; i++) {
        printf("\nStaff %d\n", i+1);
        printf("Name: %s\n", S1[i].name);
        printf("Work Type: %s\n", S1[i].work_type);
        printf("Working Hours: %d hrs/day\n", S1[i].working_hours);
        printf("Extra Working Days: %d\n", S1[i].extra_work_days);
        printf("Off Days: %d\n", S1[i].off_days);
        printf("Basic Salary: %d\n", S1[i].basic_salary);
    }

    return 0;
}

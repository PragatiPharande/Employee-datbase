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
    int i, n;

    printf("Enter number of cleaning staff: ");
    scanf("%d", &n);

    struct CleaningStaff S1[3];
    for(i = 1; i <= 3; i++) {
        printf("\n--- Enter Details for Staff %d ---\n", i);

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
    printf("\n================ STAFF DETAILS ================\n");
    for(i = 1; i <=3; i++) {
        printf("\nStaff %d\n",i);
        printf("Name: %s\n", S1[i].name);
        printf("Work Type: %s\n", S1[i].work_type);
        printf("Working Hours: %d hrs/day\n", S1[i].working_hours);
        printf("Extra Working Days: %d\n", S1[i].extra_work_days);
        printf("Off Days: %d\n", S1[i].off_days);
        printf("Basic Salary: %d\n",S1[i].basic_salary);
    
    }

    return 0;
}





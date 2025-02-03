# Details-of-the-person

#include <stdio.h>
#include <string.h>
struct person{
    char name[50];
    int age;
    char city[50];
};
int main() {
    struct person people[5]={
        {"Shiva",25,"India"},
        {"Ram",35,"America"},
        {"Lakshman",30,"Australia"},
        {"Rishi",22,"Europe"},
        {"Megha",20,"Italy"}
    };
    char searchname[50];
    int i,found=0;
    printf("Enter the name to search:");
    scanf("%[^\n]",searchname);
    for(i=0;i<5;i++){
        if(strcmp(people[i].name,searchname)==0) {
            printf("\nDetails of %s: \n",people[i].name);
            printf("Age: %d\n",people[i].age);
            printf("City: %s\n",people[i].city);
            found =1;
            break;
        }
    }
    if(!found) {
        printf("\nPerson with name '%s' not found in the list.\n",searchname);
    }
    return 0;
    }
            

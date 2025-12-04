# -Saving-uploading-data-in-file
#include<stdio.h>
int main(){
    char name[500];
    int i,j,p,n;
    
    FILE*f;
     f=fopen("my_file.txt","w");
    printf("enter number of names you want to add in file:");
    scanf("%d",&i);
    for(j=0;j<i;j++){
        
      printf("enter name%d:",j+1);
      scanf("%s",&name);
      
      fprintf(f,"%s\n",name);
    }
    
    
   
    
    fclose(f);
    printf("\n-----------------------\n");
    printf("names in the lists are:\n");
     f=fopen("my_file.txt","r");
     for(p=0;p<i;p++){
     fscanf(f,"%s",&name);
     
     printf("%s\n",name);
     }
    return 0;
}

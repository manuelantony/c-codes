//c-codes
//A simple sorting algorith using Selection Sort
//Here while loops are used for reading and printing elements

#include<stdio.h>
/*	Selection Sort
  	Author --> Manuel Antony
*/
void main()
{		
	printf("Selection Sort-------->\n");
	printf("-----------------------\n");
	
	int list[100];
	int i,j,h,flaf=0,com,len,count=0;        //variables for for loop compare and swaping
	int temp,m;                               //while loop variables
	printf("Enter the range of inputs :: ");
        scanf("%d",&len);
      
  int fun(int temp)                         //this used for making the temp value constant
  	{                                       //so whenever this function is called it returns a value of temp == len  
 		return(len);
    }


	printf("Enter the elemnts :: \n");
	
	temp = fun(temp);
	m = 0;
        while(m != temp){
		          scanf("%d",&list[m]);  
		          m++;
	      }

	printf("\nOrdering ::\n");
	
	for(j=0;j<len-1;j++){
		
		com = list[j];
		for(i=j+1;i<len;i++){
			count ++;
			if(list[i]<com){
				com = list[i];
				h = i;
				flaf = 1;	
			}
		}
    if(flaf == 1){
			 int swap = list[h]; 
			 list[h] = list[j];
		   list[j] = swap;
		}

	flaf = 0;

		temp = fun(temp);
        	m = 0;
        	while(m != temp){
        	        printf("%d ",list[m]);
        	        m++;
        	}
		printf("\n");
	}
        
	printf("\n\nSorted Out Put :: ");
	
	temp = fun(temp);
        m = 0;
        while(m != temp){
                printf("%d ",list[m]);
                m++;
        }
	printf("\n");
	
  printf("Number Of Comparissions :: %d \n\n",count);

}

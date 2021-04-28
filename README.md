# Assignment_1
#Quession(1)
(1)To create a directory in your home directory having 2 subdirectories:

![1](https://user-images.githubusercontent.com/82906996/116477411-dc473f80-a87c-11eb-8d23-4030e0c7e783.png)

(2)n the first sub directory create 3 different files with different content in each of 
 them.
 ![2](https://user-images.githubusercontent.com/82906996/116477535-0c8ede00-a87d-11eb-97f9-985bf1c3307d.png)
 
 (3)Copy the first file from the first subdirectory to the second subdirectory:
 ![3](https://user-images.githubusercontent.com/82906996/116477616-27615280-a87d-11eb-8997-34524a751509.png)
 
 (4)Copy the first file from the first subdirectory to the second subdirectory:
 ![4-1](https://user-images.githubusercontent.com/82906996/116477785-6099c280-a87d-11eb-8098-4a8bcfa9b223.png)
 
 (5)To list all the files which starts with either a or A:
 ![4-2](https://user-images.githubusercontent.com/82906996/116477869-7e672780-a87d-11eb-8ce3-a9c8317c999c.png)
(6)To count the number of files in the current directory:
![5](https://user-images.githubusercontent.com/82906996/116478113-df8efb00-a87d-11eb-9494-4ba2b086885d.png)

Quession(2)
(1)Execute the following commands in sequence: i) date ii) ls iii ) pwd:
![6](https://user-images.githubusercontent.com/82906996/116478247-12d18a00-a87e-11eb-8898-599b9b182499.png)

#Quession(3)
Write a C program to simulate wc command to count number of characters, words 
 and lines in a file.
 The Code:
 #include <stdio.h>
#define MAX_LEN 1024

int main() {
  /*Read the file.*/

  char ch;
  int char_count = 0, word_count = 0, line_count = 0;
  int in_word = 0;
  char file_name[MAX_LEN];
  FILE *fp;

  printf("Enter a file name: ");
  scanf("%s", file_name);

  fp = fopen(file_name, "r");

  if(fp == NULL) {
    printf("Could not open the file %s\n", file_name);
    return 1;
  }

  while ((ch = fgetc(fp)) != EOF) {
    char_count++;

    if(ch == ' ' || ch == '\t' || ch == '\0' || ch == '\n') {
      if (in_word) {
        in_word = 0;
        word_count++;
      }

      if(ch = '\0' || ch == '\n') line_count++;

    } else {
      in_word = 1;
    }
  }

  printf("In the file %s:\n", file_name);
  printf("Number of characters: %d.\n", char_count);
  printf("Number of words: %d.\n", word_count);
  printf("Number of lines: %d.\n", line_count);

  return 0;
}
![8](https://user-images.githubusercontent.com/82906996/116478557-87a4c400-a87e-11eb-9027-81107d67ad87.png)

 




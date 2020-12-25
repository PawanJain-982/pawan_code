import java.io.BufferedReader;
import java.io.File;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;
public class Code1
{
public static void main(String[]args)
{
Scanner sc=new Scanner(System.in);
System.out.println("Enter no of string to be Replaced");
int t=sc.nextInt();
String[]wordsToReplace=new String[t];
String[]wordsToReplaceWith=new String[t];
for(int i=0;i<t;i++){
System.out.println("enter word which you want to replace");
wordsToReplace[i] = sc.next();
System.out.println("enter word with you want to replace");
wordsToReplaceWith[i] = sc.next();}
long count=replaceWords("D:\\StudentFile.txt", wordsToReplace, wordsToReplaceWith);
System.out.println(count);
}
public static long replaceWords(String filePath, String[] wordsToReplace, String[] wordsToReplaceWith)
{
String[] words=null;                                                                                    
long count=0;
for(int i=0;i<wordsToReplace.length;i++){

try{
    FileReader fri = new FileReader(filePath);
    String str;
    String totalStr = "";

    try (BufferedReader br = new BufferedReader(fri)) {

        while ((str = br.readLine()) != null) {
            words=str.split(" ");  //Split the word using space
            totalStr += str;
          for (String word : words) 
          {
                 if (word.equals(wordsToReplace[i]))   //Search for the given word
                 {
                     totalStr = totalStr.replace(wordsToReplace[i], wordsToReplaceWith[i]);
                   count++;    //If Present increase the count by one
                 }
          }
            
        }
         
         
        
        FileWriter fw = new FileWriter(filePath);
    fw.write(totalStr);

   fw.close();
}

}catch(Exception e){
    e.printStackTrace();
}
}
return count;

}
}

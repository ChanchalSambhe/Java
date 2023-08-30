package Number_Game;
import java.util.Scanner;
import java.util.Random;

public class Number_Game {
   public static void main(String args[]){
        int attempt =0;
        final int Max = 100;
        int score = 0;
        Scanner sc = new Scanner(System.in);
       
        Random rn = new Random();
        int ans = rn.nextInt(Max)+1;

         int round = 0;
         
         jump : while(round!=4){
               attempt = attempt +1;
             for(int i=1 ; i<=4; i++){
                 
               System.out.println("Enter A Guess Number :---");
               int guess = sc.nextInt();
               
            if(guess > ans){
                System.out.println("Opps!!! sorry.. Guesss number is TOO HIGHT  than random number....");
            } 
            else if(guess < ans){
                System.out.println(" Ohhhhh!!! again guess number  TOO LOW  try again ...");
            }
            else if(guess == ans ){
                System.out.println("WOW!!! Congrats.... Now it's a correct Guesss..");
                score = score + 1;
                }
            round++;
           }
            System.out.println("Do You Want to continue this game then please type 'Y' for yes & 'N' for No");
            String Y = "Y" ;
            String c = sc.next(); 
            
            
            
            if((c.compareTo(Y)) == 0){
                 round++;
                 continue jump; 
                
             }
             else{
                 System.out.println("Number of Attempt are :--- " +attempt);
                System.out.println("This is your scores :--- " +score);
                System.out.println("Thanks for play game.... ");
               
            }
              
         }
    }
}

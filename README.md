# Number_Guezzing_Game_Using_Java
import java.util.Random;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("Welcome To Random Number Picking Game!!!");
        Scanner input = new Scanner(System.in);
        System.out.print("Enter Your name : ");
        String name = input.next();
        System.out.println("Hello! "+name);

        System.out.print("If you like to begin the game press true else false : ");
        var opinion = input.nextBoolean();
        if(opinion==true)
        {
            System.out.println("Let's begin the game");
            Random random = new Random();
            int ques = random.nextInt(20);

            for(int i =1;i<=5;i++)
            {
                System.out.print("enter the number you guess " +i+" Chance :");
                int ans = input.nextInt();
                if(ques == ans)
                {
                    System.out.println("Your ans is correct!!!");
                    break;
                }
                else
                {
                    System.out.println("try the another chance");
                    if(ques > ans)
                    {
                        System.out.println("Hint : enter the ans greater than What you typed not less");
                    }
                    else
                    {
                        System.out.println("Hint : enter the ans lesser than What you typed not greater");
                    }
                    if(i==5)
                    {
                        System.out.println("Game Over");
                        System.out.println("The correct Ans is : " + ques);
                    }
                }
            }

        }


        else
        {
            System.out.println("Thankyou");
        }



    }
}

# MINMAXAV
import java.util.Scanner;

public class Nuberavminmax
{
    public static void main (String args[]){
        int total = 0;
        int counter = 0;
        int max = -1000000;
        int min = 1000000;
        String cont = "yes";
        Scanner test = new Scanner (System.in);

        while (cont.equals("yes")){ 
            Scanner input = new Scanner (System.in);
            System.out.println ("Please input number");
            int number = input.nextInt();

            while (number > 1000000 | number < -1000000){
                System.out.println ("Please enter number between -1000000 and 1000000");
            }
            if (number > max){
                max = number; }
            if (number < min){
                min = number; }

            total = (number + total);
            counter = (counter +1);
            float average = (total / counter);

            System.out.println ("Max = " + max);
            System.out.println ("Min = " + min);
            System.out.println ("Average = " + average);
            System.out.println ("Do you wish to continue?");
            cont = test.nextLine();
        }

    }
}


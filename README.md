import java.util.Scanner;
class Guesser
{
    int gnum;
    int guessingNum()
    {
        System.out.println("guesser,kindly guess a number!");
        Scanner scan=new Scanner(System.in);
        gnum=scan.nextInt();
        return gnum;
    }
}
class Player
{
    int pnum;
    int predictingNum()
    {
         System.out.println("player,kindly predicted a number!");
        Scanner scan = new Scanner(System.in);
        pnum=scan.nextInt();
        return pnum;
    }
}
class Umpire
{
    int numFromGuesser;
    int numFromPlayer1;
    int numFromPlayer2;
    int numFromPlayer3;
    void collectingNumFromGuesser()
    {
        Guesser g=new Guesser();
        numFromGuesser=g.guessingNum();
    }
    void collectingNumFromPlayers()
    {
        Player p1=new Player();
        Player p2=new Player();
        Player p3=new Player();
        numFromPlayer1=p1.predictingNum();
        numFromPlayer2=p2.predictingNum();
        numFromPlayer3=p3.predictingNum();
    }
    Void comparing()
    {
        if(numFromPlayer1==numFromGuesser)
        {
          System.out.println("player1 has won the the game!");  
        }
        else if(numFromPlayer2==numFromGuesser)
        {
          System.out.println("player2 has won the the game!");  
        }
        else if(numFromPlayer3==numFromGuesser)
        {
          System.out.println("player3 has won the the game!");  
        }
        else
        {
            System.out.println("Game host,Try agian!");
        }
    }
}
class GuesserGameApp 
{
    public static void main(String[] args) 
    {
        Umpire u=new Umpire();
        u.collectingNumFromGuesser();
        u.collectingNumFromPlayers();
        u.comparing();
        }
}

# Ex.No:3(D)    INTERFACE 

## QUESTION:

Each judge uses different criteria to score fighters. Based on points, the judge will declare “WIN”, “LOSE” or “DRAW”.</BR>
LenientJudge: WIN if diff ≥ 5, DRAW if < 5</BR>
StrictJudge: WIN if diff ≥ 10, DRAW if < 10</BR>
Input Format: player1Score, player2Score, judgeType, player1Score, player2Score: integers, judgeType: 1 for LenientJudge, 2 for StrictJudge. Output Format: WIN / LOSE / DRAW.

## AIM:

To write a Java program demonstrating method overriding using a base class Judge that evaluates fighters based on different scoring rules. Two subclasses LenientJudge and StrictJudge override the evaluation logic and declare the result as WIN, LOSE, or DRAW.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read player1Score and player2Score.
4. Read judgeType (1 = LenientJudge, 2 = StrictJudge).
5. Create a base class Judge with a method decideResult().
6. Create subclasses:</BR>
     - LenientJudge:</BR>
         - diff = |player1Score – player2Score|</BR>
         - If diff ≥ 5 → WIN</BR>
         - If diff < 5 → DRAW</BR>
      - StrictJudge:</BR>
         - If diff ≥ 10 → WIN</BR>
         - If diff < 10 → DRAW</BR>
7. For both judges:</BR>
      - If player1Score < player2Score → result is LOSE</BR>
      - If scores equal → DRAW</BR>
8. Print the final result.
9. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
interface Judge
{
    String decide(int p1, int p2);
}

class LenientJudge implements Judge
{
    public String decide(int p1, int p2)
    {
        int diff = p1 - p2;
        if (diff >= 5)
            return "WIN";
        else if (diff <= -5)
            return "LOSE";
        else 
            return "DRAW";
    }
}

class StrictJudge implements Judge
{
    public String decide(int p1, int p2)
    {
        int diff = p1 - p2;
        if (diff >= 10)
            return "WIN";
        else if (diff <= -10)
            return "LOSE";
        else
            return "DRAW";
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int p1 = sc.nextInt(), p2 = sc.nextInt(), type = sc.nextInt();
        Judge j = (type == 1) ? new LenientJudge() : new StrictJudge();
        System.out.println(j.decide(p1, p2));
    }
}
```

## OUTPUT:

<img width="336" height="231" alt="image" src="https://github.com/user-attachments/assets/40524a8f-a5f0-470b-9bd3-bb01750e9b30" />

## RESULT:

The program successfully demonstrates method overriding, where the decision-making logic differs between LenientJudge and StrictJudge. Based on the score difference and judge type, the final output displays WIN, LOSE, or DRAW.

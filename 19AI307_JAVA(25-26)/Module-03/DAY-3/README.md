# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create abstract class GameScore with method finalScore().
Subclasses:</BR>
ArcadeGame: score = baseScore + (level × 100)</BR>
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500</BR>
Input Format: First line: 1 or 2 , Second line: base, level (or attempts). Output Format: Final score (int)

## AIM:

To write a Java program using abstract classes where GameScore defines the abstract method finalScore().
Two subclasses, ArcadeGame and PuzzleGame, implement different scoring formulas based on user input and display the final score.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class GameScore with:
    - An abstract method finalScore() returning an integer.
4. Create the subclass ArcadeGame that stores: baseScore , level
    - Implements: score = baseScore + (level × 100)
4. Create the subclass PuzzleGame that stores:attempts
    - Implements: If attempts ≤ 3 → score = 1000 - (attempts × 100) , Else → score = 500
5. In the main() method:
    - Read user selection (1 for Arcade, 2 for Puzzle).
    - Read corresponding inputs.
    - Create the appropriate subclass object.
    - Call finalScore() and print the result.
6. End the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
abstract class GameScore
{
    abstract int finalScore();
}

class ArcadeGame extends GameScore
{
    int base, level;
    ArcadeGame(int b, int l)
    {
        base = b;
        level = l;
    }
    int finalScore()
    {
        return base + (level * 100);
    }
}

class PuzzleGame extends GameScore
{
    int attempts;
    PuzzleGame(int a)
    {
        attempts = a;
    }
    int finalScore()
    {
        return (attempts <= 3) ? (1000 - attempts * 100) : 500;
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        if (type == 1)
        {
            int base = sc.nextInt();
            int level = sc.nextInt();
            ArcadeGame ag = new ArcadeGame(base, level);
            System.out.println(ag.finalScore());
        }
        else
        {
            int attempts = sc.nextInt();
            PuzzleGame pg = new PuzzleGame(attempts);
            System.out.println(pg.finalScore());
        }
    }
}
```

## OUTPUT:

<img width="308" height="139" alt="image" src="https://github.com/user-attachments/assets/8895839a-c7ff-4d69-aa7f-933d8de829ff" />

## RESULT:

The program successfully demonstrates the use of abstract classes and method overriding by calculating the final score for two game types based on different scoring rules and user input.

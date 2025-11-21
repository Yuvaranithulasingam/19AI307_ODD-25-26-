# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## AIM:

To develop a simple Air Traffic Control (ATC) system using the Mediator Pattern, where multiple Airplane objects communicate with a central mediator to request landing. The mediator controls and manages the landing permissions instead of airplanes communicating with each other directly.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface ATCMediator with a method requestLanding(Airplane plane).
4. Create a concrete class ControlTower that implements ATCMediator.
     - Maintain a boolean flag runwayFree = true.
     - If runway is free → grant landing permission and mark runway busy.
     - If runway is busy → ask the plane to wait.
5. Create an Airplane class with attributes: name and a reference to the mediator.
     - Include a method requestLanding() that forwards the request to mediator.
     - Include methods land() and waitForLanding().
6. In main():
     - Create one ControlTower object.
     - Create 2–3 Airplane objects.
     - Each airplane calls requestLanding().
7. Display messages showing mediator decisions.
8. Stop the program.

#### Developed by: YUVARANI T
#### RegisterNumber:  212222110057

## SOURCE CODE:
```
import java.util.*;
class AirTrafficControl
{
    public void grantLanding(Airplane plane)
    {
        System.out.println(plane.getName() + " granted landing.");
        System.out.println(plane.getName() + " landed successfully.");
    }
    public void denyLanding(Airplane plane)
    {
        System.out.println(plane.getName() + " denied landing. Runway busy.");
    }
}
class Airplane
{
    private String name;
    private AirTrafficControl atc;
    public Airplane(String name, AirTrafficControl atc)
    {
        this.name = name;
        this.atc = atc;
    }
    public String getName()
    {
        return name;
    }
    public void requestGrant()
    {
        atc.grantLanding(this);
    }

    public void requestDeny() {
        atc.denyLanding(this);
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextInt()) {
            int n = sc.nextInt();
            if (!sc.hasNext()) break;
            boolean runwayFree = sc.nextBoolean();
            sc.nextLine(); 

            AirTrafficControl atc = new AirTrafficControl();
            List<Airplane> planes = new ArrayList<>();

            for (int i = 0; i < n; i++) {
                if (!sc.hasNextLine()) break;
                String name = sc.nextLine().trim();
                planes.add(new Airplane(name, atc));
            }

            if (runwayFree) {
                for (Airplane p : planes) {
                    p.requestGrant();
                }
            } else {
                for (int i = 0; i < planes.size(); i++) {
                    Airplane p = planes.get(i);
                    if (i == 0) {
                        p.requestGrant();
                    } else {
                        p.requestDeny();
                    }
                }
            }
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="981" height="477" alt="image" src="https://github.com/user-attachments/assets/96921c83-1362-4104-a9ec-6c035ee29bcc" />

## RESULT:

The program successfully demonstrates the Mediator design pattern by coordinating landing requests from multiple airplanes through a central Air Traffic Control mediator. It ensures organized communication and prevents direct interaction between airplanes.

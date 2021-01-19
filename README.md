# InheritanceChallenge
package academy.learnprogrmming;

class Vehicle {
    int gears;
    int speed;

    public Vehicle(int gears, int speed) {
        this.gears = gears;
        this.speed = speed;
    }

    public int accelerate(int speed) {
        if (speed < 60) {
            System.out.println("speed up");

        }
        return gears += speed;
    }
    public int deccelerate(int speed){
        if (speed > 60) {
            System.out.println("slow down");

        }
        return gears -= speed;
    }
}

class Car extends Vehicle {
    int move;
    int steering;



    public Car(int gears, int speed) {
        super(gears, speed);
        this.move = move;
        this.steering = steering;

    }

    public int turningVehicle(int move){
        if(move == 15) {
            System.out.println("You made a safe turn Batman");
        }
        else if(move > 15){
            System.out.println("You are driving too fast Batman");
        }
        return move -= steering;
    }

  }
  class Batmobile extends Car{

    public Batmobile(int move, int steering){
        super(move, steering);

    }

    @Override
    public int turningVehicle(int move){
        if(move == 15) {
            System.out.println("You made a safe turn Batman");
        }
        else if(move > 15){
            System.out.println("You are driving too fast Batman");
            autoPilot();
        }
        return move -= steering;
    }


    public void autoPilot(){
        System.out.println("Would You Like To Use Auto Pilot Batman?");
    }
  }



public class Main {

    public static void main(String[] args) {

       Batmobile test = new Batmobile( 5, 65);

       test.accelerate(65);
       test.deccelerate(65);
       test.turningVehicle(20);







    }

}
"C:\Program Files\Java\jdk-15.0.1\bin\java.exe" "-javaagent:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\lib\idea_rt.jar=50290:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\bin" -Dfile.encoding=UTF-8 -classpath C:\Users\nadiy\IdeaProjects\InheritanceChallenge\out\production\InheritanceChallenge academy.learnprogrmming.Main
slow down
You are driving too fast Batman
Would You Like To Use Auto Pilot Batman?

Process finished with exit code 0

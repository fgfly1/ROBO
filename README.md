# ROBO
PROJETO ROBO CODE
import robocode.*;

public class MeuRobozinho extends Robot {

    public void run() {
        
        setColors(java.awt.Color.blue, java.awt.Color.blue, java.awt.Color.green);

        
        while (true) {
            
            ahead(100);

             
            turnRight(90);

            
            ahead(100);

             
            turnRight(90);
        }
    }

    public void onScannedRobot(ScannedRobotEvent e) {
        
        double distancia = e.getDistance();
        
        
        turnGunRight(getHeading() - getGunHeading() + e.getBearing());

        
        if (distancia < 200) {
            fire(3); 
        } else {
            fire(1); 
        }
    }
}

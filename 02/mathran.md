public class Puzzle {
    private int value;
    int low;
    int high;
    public Puzzle(int low, int high) {
        high-=low+1;
        value= (int) (Math.random()*high)+low;
    }
    public int getValue(){
        return value;
    }

}

public class UtillTest {
    public static void main(String[] args) {
        int i=0;
        while(i<=100){
            Puzzle puzzle =new Puzzle(-20,21);
         //   Puzzle puzzle1 =new Puzzle(0,100);
            System.out.println(puzzle.getValue()+" eiei");
           // System.out.println(puzzle1.getValue());
            i++;
        }
}
}


package int101.geometry;

/**
 *
 * @author Baimon
 */
public class Box3D {
    private double width;
    private double hight;
    private static double length;
    private static String color ;
    public Box3D(double width, double hight) {
        this.width = width;
        this.hight = hight;
    }

    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        this.width = width;
    }

    public double getHight() {
        return hight;
    }

    public void setHight(double hight) {
        this.hight = hight;
    }

    public static double getLength() {
        return length;
    }

    public static void setLength(double length1) {
        length = length1;
    }

    public static String getColor() {
        return color;
    }

    public static void setColor(String color) {
        Box3D.color = color;
    }
   
   public double computeVolume(){
   return width * hight * length;
   } 
   public boolean canCover(Box3D b){
   boolean n ;
   if  (n = (b.width  >= this.width) && (b.hight >= this.hight)) n = true ;
   //return (b.width  >= this.width) && (b.hight >= this.hight);
   return n;
   }  

    @Override
    public String toString() {
        return "Box3D{" + "width=" + width + ", hight=" + hight + ", length=" + length + ", color=" + color + '}';
    }
  

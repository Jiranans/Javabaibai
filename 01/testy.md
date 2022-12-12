package review.main;
import review.int101.ReviewStatic;
import int101.geometry.Sphere; 
import int101.geometry.Box3D; 
public class ReviewMain {
    public static void main(String[] args) {
        double radius = 2;
//        double width = 2;
//        double heigth =3 ;
//        double depth = 4;
       double v1 = 3;
       double v2 = 5;
//        double v3 = 4;
//        double v4 = 4;
        int step = 1;
        System.out.printf("computeSphareVolume of %.2f = %.2f%n ", radius ,ReviewStatic.computeSphareVolume(radius));
//         System.out.printf("computeBoxVolume of %.2f ,%.2f ,%.2f= %.2f%n ", width,heigth,depth,ReviewStatic.computeBoxVolume(width, heigth, depth));
//       // System.out.println("computeSphareVolume" + ReviewStatic.computeSphareVolume(radius));  
//        System.out.println("findMax " + ReviewStatic.findMax(v1, v2, v3));
//        System.out.println("positiveSum " + ReviewStatic.positiveSum(v1, v2, v3, v4));
        System.out.printf("product of %.2f ,%.2f ,%d = %.2f%n" ,v1 ,v2 , step ,ReviewStatic.product(v1, v2, step));
        System.out.println("eei");
//        testSphere();
        testBox3D();
    }
//    public static void testSphere(){
//    Sphere s1 = new Sphere(5.0);
//    Sphere s2 = new Sphere(5.0);
//    System.out.println("s1's radius = " + s1.getRadius());
//    System.out.println("s2's radius = " + s2.getRadius());
//    System.out.println("s1's volume = " + s1.computeVolume());
//    System.out.println("s2's volume = " + s2.computeVolume());
//    System.out.println("s1's surface = " + s1.computeSurface());
//    System.out.println("s2's surface = " + s2.computeSurface());
//    System.out.println("s2's volume / s1's volume =" + s1.compereSurVolume(s2));
//    s1.setRadius(2.5);
//    System.out.println("s2's volume / s1's volume =" + s1.compereSurVolume(s2));
//    }
    public static void testBox3D(){
    Box3D b1 = new Box3D(2.0,3.0);
    Box3D b2 = new Box3D(4.0,3.0); 
    Box3D.setColor("RED");
    System.out.println("All Box color is " + Box3D.getColor());
    Box3D.setLength(5.0);
    System.out.println("All Box Length is " + Box3D.getLength());
    System.out.println("b1 computeVolume = " + b1.computeVolume());
    System.out.println("b2 canCover b1 ? = " + b1.canCover(b2));
    System.out.println(b1);
    System.out.println(b2.toString());
   
    }
}

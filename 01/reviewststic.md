package review.int101;

public class ReviewStatic {

    public static double computeSphareVolume(double radius) {
        return Math.PI * 4.0 / 3.0 * Math.pow(radius, 3);
    }

    public static double computeBoxVolume(double width, double heigth, double depth) {
        return width * heigth * depth;
    }

    public static double findMax(double v1, double v2, double v3) {
        double max =0;
        if(v1>=v2 && v1>=v3){
            max = v1;
        } 
        else if(v2>=v1 && v2>=v3){
            max = v2;
        }
        else if(v3>=v1 && v3>=v2){
            max = v3;
        }       
        return max ;
    }
    public static double positiveSum(double v1, double v2, double v3,double v4) {
        double sum=0;
        if(v1>=5){
        sum +=v1;
        }
        if(v2>=5){
        sum += v2;
        }
        if(v3>=5){
        sum += v3;
        }
        if(v4>=5){
        sum += v4;
        }
        return sum;
    }
    public static double product(double v1, double v2, int step) {
        double multiply = 1;
        for (double v=v1;v<=v2;v+=step){
         multiply*=v;
        }
        return multiply;  
    }

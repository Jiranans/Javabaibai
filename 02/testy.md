package int101.test;
import int101.array.Student;
public class StudentTest {
    public static void main(String[] args) {
      
     testStudent();   
    }

//    private static void testStudent() {
//        final int size = 10;
//     Student[] student = new Student [size];
//        for (Student student1 : student) {
//            System.out.println(student1);
//        }
//    }
    private static void testStudent() {
        final int size = 10;
        Student[] students = new Student[size];
        for (int i = 0; i < size; i++) {
            students[i] = new Student("No." + i);
        }
        for (Student student : students) {
            System.out.println(student);
        }
    }
}

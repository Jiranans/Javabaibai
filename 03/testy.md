
import exam.Department;
import exam.Person;
import java.util.Arrays;

public class ProjectDriver {

   public static void main(String[] args) {
        testPerson();
        testDepartment();
    }

    public static void testPerson() {
        System.out.println("\n# Person # ===========");
        
        // Constructor: Person(firstname, lastname, type)
        System.out.println("\n# Constructor: Person(firstname, lastname, type) -----------------");
        System.out.println("new Person(null,null,-1) => " + new Person(null, null, -1));
        System.out.println("new Person(\"FirstName\",\"  \", 0) => " + new Person("FirstName", "  ", 0));
        System.out.println("new Person(\"\",\"LastName\", 2) => " + new Person("", "LastName", 2));

        // Constructor: Person (firstname, lastname)
        System.out.println("\n# Constructor: Person(firstname, lastname) -----------------");
        System.out.println("new Person(\"First\",\"Last\") => " + new Person("First", "Last"));
        System.out.println("new Person(null,\"Surname\") => " + new Person(null, "Surname"));

        // Getters: getCode(), getFirstname(), getLastname(), getType()
        System.out.println("\n# Getters -----------------");
        var p = new Person("GivenName", "FamilyName", 9);
        System.out.println(p);
        System.out.println("p.getCode(): " + p.getCode());
        System.out.println("p.getFirstname(): " + p.getFirstname());
        System.out.println("p.getLastname(): " + p.getLastname());
        System.out.println("p.getType(): " + p.getType());

        // Setters: setFirstname(), setLastname()
        System.out.println("\n# Setters -----------------");
        p.setFirstname("  ");
        p.setLastname("LASTname");
        System.out.println("firstname=blank, lastname=LASTname => " + p);
        p.setFirstname("FIRSTname");
        p.setLastname(null);
        System.out.println("firstname=FIRSTname, lastname=null => " + p);
        
        // toString()
        System.out.println("\n# toString() -----------------");
        System.out.println(p.toString());
        
        // equals()
        System.out.println("\n# equals() -----------------");
        var q = p;
        var r = new Person("FIRSTname", "LASTname", 9);
        System.out.println("p = " + p);
        System.out.println("q = " + q);
        System.out.println("r = " + r);
        System.out.println("p == q ? " + (p==q));
        System.out.println("p == r ? " + (p==r));
    }

    public static void testDepartment() {
        System.out.println("\n# Department # ===========");
        
        // Constructor: Department(title)
        System.out.println("\n# Constructor: Department(title) -----------------");
        System.out.println("new Departmet(null) => " + new Department(null));
        System.out.println("new Departmet(\"\") => " + new Department(""));
        System.out.println("new Departmet(\"Dept\") => " + new Department("Dept"));

        // Getters: getCode(), getTitle(), getCount()
        var d = new Department("DepartmentTitle");
        System.out.println(d);
        System.out.println("d.getCode(): " + d.getCode());
        System.out.println("d.getTitle(): " + d.getTitle());
        System.out.println("d.getCount(): " + d.getCount());

        // addStaff(firstname, lastname, type)
        System.out.println("d.addStaff(\"  \", \"LAST\", 2): " + d.addStaff("  ", "LAST", 2));
        System.out.println("d.addStaff(\"FIRST\", null, 4): " + d.addStaff("LAST", null, 4));
        System.out.println("d.addStaff(\"FIRST\", \"LAST\",-6): " + d.addStaff("FIRST", "LAST", -6));
        final int type = 7;
        for (int i = 0; i < 12; i++) {
            System.out.println(i + " d.addStaff(..., ..., ...): "
                    + d.addStaff("F" + i, "L" + (100 + i), (int) (Math.random()*type)) + " ... count=" + d.getCount());
            if (Math.random() < 0.5) new Person(null,null); // for skipping some Person.code
            if (Math.random() < 0.5) new Person(null,null); // for skipping some Person.code
            if (Math.random() < 0.5) new Person(null,null); // for skipping some Person.code
        }

        // getTypeCount(type)
        for (int i = 0; i < type; i++) 
            System.out.println("d.getTypeCount(" + i + ") = " + d.getTypeCount(i));

        // getAllCodes()
        System.out.println("d.getAllCodes(): " + Arrays.toString(d.getAllCodes()));

        // getStaff(code)
        for (int i = 0; i < 19; i++) {
            int x = (int) (Math.random() * 25) + 5;
            System.out.println("d.getStaff(" + x + ") = " + d.getStaff(x));
        }

        // toString()
        System.out.println("d.toString(): " + d.toString());
        
        // getAllTypes() 
        System.out.println("d.getAllType(): " + Arrays.toString(d.getAllTypes()));
    }
}


package exam;

public class Person {
    private final int code;
    private final int type;
    private final int defaulttype = 1;
    private   String firstname;
    private  String lastname;
    private static int nextcode = 010;
    
    public Person( String firstname, String lastname,int type) {
        this.code=nextcode++;
        this.type = type;
      
        if (type < 0) {
           type = defaulttype; 
        }
        if (firstname == null || firstname.isBlank()) {this.firstname = "Jiranan";} else {this.firstname = firstname;}
        if (lastname == null || lastname.isBlank()) {this.lastname = "Yenlab";} else {this.lastname = lastname;}
    }
   public Person(String firstname, String lastname) {
         if (firstname == null || firstname.isBlank()) {this.firstname = "Jiranan";} else {this.firstname = firstname;}
        if (lastname == null || lastname.isBlank()) {this.lastname = "Yenlab";} else {this.lastname = lastname;}
        this.code=defaulttype;
        this.type = defaulttype;
     }

 

    public int getCode() {
        return code;
    }

    public int getType() {
        return type;
    }

    public String getFirstname() {
        return firstname;
    }

    public String getLastname() {
        return lastname;
    }
    
    public void setFirstname(String firstname) {
        if (firstname == null || firstname.isBlank()) {this.firstname = "Jiranan";} else {this.firstname = firstname;}

    }

    public void setLastname(String lastname) {
        if (lastname == null || lastname.isBlank()) {this.lastname = "Yenlab";} else {this.lastname = lastname;}
    }

    @Override
    public String toString() {
        return "Person{" + "code=" + code + "( " + firstname + lastname + " )" +", type=" + type +  '}';
    }

    @Override
    public int hashCode() {
        int hash = 7;
        return hash;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }
        if (obj == null) {
            return false;
        }
        if (getClass() != obj.getClass()) {
            return false;
        }
        final Person other = (Person) obj;
       }
       }

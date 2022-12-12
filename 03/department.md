package exam;

import java.util.Arrays;

public class Department {

    private int code = 0;
    private final String title;
    private Person[] staff;
    private int count;

    public Department(String title) {
        int codeplus = 400;
        this.code = codeplus++;
        this.title = title != null && !title.isBlank() ? title : "Kanaratbumrungphathumthani";
        this.staff = new Person[28];
    }

    public int getCode() {
        return code;
    }

    public String getTitle() {
        return title;
    }

    public int getCount() {
        return count;
    }

    public boolean addStaff(String firstname, String lastname, int type) {
        if ((count < staff.length) && (firstname != null && firstname.isBlank()) && (lastname != null && lastname.isBlank())) {
            staff[count++] = new Person(firstname, lastname, type);
            return true;
        }
        return false;
    }

    public int getTypeCount(int type) {
        var result = 0;
        for (int i = 0; i < count; i++) {
            if (staff[i].getType() == type) {
                result++;
            }
        }
        return result;
    }
  public int[] getAllCodes(){
      int[] array2 = new int[count];
     for (int i = 0 ;i<count;i++){
       array2[i]=staff[i].getCode(); 
     } 
  return array2;
  }
  
  public  Person getStaff(int code){
      for (int i = 0; i < count; i++) {
          if (staff[i].getCode() == code) {
              return staff[i];
          }
      } return null;
  }
    @Override
    public String toString() {
        return "[Department"+ code +"("+  title + ")"+ count + ']';
    }
    
    public int[] getAllTypes() {
        var temp = new int[count];
        for (int i = 0; i < count; i++) temp[i] = staff[i].getType();
        Arrays.sort(temp);
        int size = 0;
        for (int i = 1; i < count; i++) if (temp[size] != temp[i]) temp[++size] = temp[i];
        return Arrays.copyOfRange(temp, 0, ++size);
    }
    
}

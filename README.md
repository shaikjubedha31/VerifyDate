# VerifyDate
import java.text.*;
import java.util.*;

public class Main {
   public static boolean check(String date)
   {
      // Set the preferred date format
      SimpleDateFormat format = new SimpleDateFormat("MM/dd/yyyy");
      format.setLenient(false);
      try
      {
          Date d = format.parse(date); 
          System.out.println(date+" is a valid date");
      }
      // Invalid date
      catch (ParseException e)
      {
          System.out.println(date+" is an invalid date");
          return false;
      }
      // Returns true if the date is valid
      return true;
   }
   
   public static void main(String args[]){
    check("07/25/2020");
    check("07/25/0000");
    check("07,25,2020");
   }
}

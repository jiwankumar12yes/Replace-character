# Replace-character
package recursion2;
import java.lang.Character.Subset;
import java.util.*;
public class replace_character {
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        System.out.println("enter a string");
        String str=s.nextLine();
        System.out.println("enter a character to replace");
        char x=s.next().charAt(0);
        System.out.println("enter a character that you want");
        char a=s.next().charAt(0);
        System.out.println(Replace(str,x,a));
    }
    public static String Replace(String str,char x,char a){
        if(str.length()==0){
            return str;
        }
        String ans="";
        if(str.charAt(0)==x){
            ans=ans+a;
        }
        else{
            ans=ans+str.charAt(0);
        }
        String smallans=Replace(str.substring(1), x, a);
        return ans+smallans;
    }
    
}

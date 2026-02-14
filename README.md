
class Restaurant extends Thread{
    public void run(){
        
            System.out.println("Restaurant is making a your food");
             try{

               Thread.sleep(1000);
             }catch(Exception e){
    
               System.out.println(e);
             }
        System.out.println("the food is ready");
             
        
    }
}
class Delivary extends Thread{
    public void run(){
        System.out.println("delivary boy is coming...");
        try{
          Thread.sleep(1000);
        }catch(Exception e){
          System.out.println(e);
        }
         System.out.println("delivary boy received the place order..");

          System.out.println("Food was delivared");
    }
}
public class Main{
    public static void main(String[] args){
        Restaurant res=new Restaurant();
        Delivary del= new Delivary();
        res.start();
        del.start();
       
    }
}

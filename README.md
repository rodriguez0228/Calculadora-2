# Calculadora-2
public class Operacion {
    
    double n1;
    double n2;
    double res;
    char operacion;

    
    public Operacion(double n1, double n2, char operacion) {
        
        this.n1 = n1;
        this.n2 = n2;
        this.operacion = operacion;
    }
    
        
    public void mostrarResultado(){
        
        System.out.println(this.n1+" "+this.operacion+" "+this.n2+" = "+this.res);
        
    }
}
public class Suma extends Operacion{
    
    double suma;
       
    public Suma(double n1, double n2) {
             
        super(n1, n2, '+');
        this.suma = n1 + n2;
        this.setRes(this.suma);
    }
}
public class Resta extends Operacion{
    
    double resta;
       
    public Resta(double n1, double n2) {
             
        super(n1, n2, '-');
        this.resta = n1 - n2;
        this.setRes(this.resta);
    }
}
public class Multiplicacion extends Operacion{
    
    double multi;
       
    public Multiplicacion(double n1, double n2) {
             
        super(n1, n2, '*');
        this.multi = n1 * n2;
        this.setRes(this.multi);
    }
}
public class Division extends Operacion{
    
    double div = 0;
       
    public Division(double n1, double n2) {
             
        super(n1, n2, '/');
        if(n2==0) System.out.println("No se puede dividir entre cero");
        else this.div = n1 / n2;
        this.setRes(this.div);
    }    
}
double n1 = 10;
double n2 = 5;
        
//suma
Suma sum = new Suma(n1,n2);
sum.mostrarResultado();

        
//resta
Resta res = new Resta(n1,n2);
res.mostrarResultado();
        
        
//multiplicacion
Multiplicacion mul = new Multiplicacion(n1,n2);
mul.mostrarResultado();

        
//division
Division div = new Division(n1,n2);
div.mostrarResultado();

# POO
Actividades de la materia Programacion Orientada A Objetos

public class CuentaBancaria {
    private double saldo;


   //Con este metodo se deposita el dinero en la cuenta bancaria, hacemos que el monto sea si o si positivo y se realiza la suma.
    public void depositar(double monto) {
        if (monto > 0) {
            saldo += monto;
        } else {
            System.out.println("El monto a depositar debe ser positivo.");
        }
    }

    //Ahora con este metodo retiramos el dinero de la cuenta, tambien que no se pueda retirar mas de lo que hay en la cuenta
    public void retirar(double monto) {
        if (monto > saldo) {
            System.out.println("No se puede retirar más de lo disponible.");
        } else if (monto <= 0) {
            System.out.println("El monto a retirar debe ser positivo.");
        } else {
            saldo -= monto;
        }
    }

    // Metodo para ver o consultar nuestro saldo
    public double getSaldo() {
        return saldo;
    }

    // Ahora con el metodo main probamos los anteriores
    public static void main(String[] args) {
        CuentaBancaria cuenta = new CuentaBancaria();
        cuenta.depositar(700);
        cuenta.retirar(200);
        System.out.println("Saldo: " + cuenta.getSaldo()); // deberia imprimir 500 si esta bien
    }
}

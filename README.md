# POO  
Actividades de la materia Programación Orientada a Objetos  

```java
public class CuentaBancaria {
    private double saldo;

    // Con este metodo se deposita el dinero en la cuenta bancaria
    public void depositar(double monto) {
        if (monto > 0) {
            saldo += monto;
        } else {
            System.out.println("El monto a depositar debe ser positivo.");
        }
    }

    // Metodo para retirar dinero de la cuenta
    public void retirar(double monto) {
        if (monto > saldo) {
            System.out.println("No se puede retirar más de lo disponible.");
        } else if (monto <= 0) {
            System.out.println("El monto a retirar debe ser positivo.");
        } else {
            saldo -= monto;
        }
    }

    // Metodo para consultar saldo
    public double getSaldo() {
        return saldo;
    }

    // Metodo main para probar
    public static void main(String[] args) {
        CuentaBancaria cuenta = new CuentaBancaria();
        cuenta.depositar(700);
        cuenta.retirar(200);
        System.out.println("Saldo: " + cuenta.getSaldo());
    }
}


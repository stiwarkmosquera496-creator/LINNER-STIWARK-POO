class Persona {
public:
    string nombre;
    int edad;

    void mostrarDatos() {
        cout << "Nombre: " << nombre << endl;
        cout << "Edad: " << edad << " años" << endl;
    }
};

int main() {
    Persona persona1;

    persona1.nombre = "Carlos";
    persona1.edad = 20;

    persona1.mostrarDatos();

    return 0;
}



class Estudiante {
public:
    string nombre;
    float nota1, nota2, nota3;

    float calcularPromedio() {
        return (nota1 + nota2 + nota3) / 3;
    }

    void mostrarResultado() {
        cout << "Estudiante: " << nombre << endl;
        cout << "Promedio: " << calcularPromedio() << endl;
    }
};

int main() {
    Estudiante estudiante1;

    estudiante1.nombre = "Andres";
    estudiante1.nota1 = 4.0;
    estudiante1.nota2 = 3.5;
    estudiante1.nota3 = 4.5;

    estudiante1.mostrarResultado();

    return 0;
}




class Vehiculo {
public:
    string marca;
    string modelo;
    int velocidad;

    void acelerar(int cantidad) {
        velocidad += cantidad;
    }

    void mostrarDatos() {
        cout << "Marca: " << marca << endl;
        cout << "Modelo: " << modelo << endl;
        cout << "Velocidad: " << velocidad << " km/h" << endl;
    }
};

int main() {
    Vehiculo carro;

    carro.marca = "Toyota";
    carro.modelo = "Corolla";
    carro.velocidad = 0;

    carro.acelerar(60);
    carro.mostrarDatos();

    return 0;
}



class CuentaBancaria {
private:
    float saldo;

public:
    CuentaBancaria() {
        saldo = 0;
    }

    void depositar(float cantidad) {
        if (cantidad > 0) {
            saldo += cantidad;
            cout << "Deposito realizado." << endl;
        } else {
            cout << "Cantidad no valida." << endl;
        }
    }

    void retirar(float cantidad) {
        if (cantidad > 0 && cantidad <= saldo) {
            saldo -= cantidad;
            cout << "Retiro realizado." << endl;
        } else {
            cout << "No se puede realizar el retiro." << endl;
        }
    }

    void consultarSaldo() {
        cout << "Saldo actual: $" << saldo << endl;
    }
};

int main() {
    CuentaBancaria cuenta;

    cuenta.depositar(500000);
    cuenta.retirar(100000);
    cuenta.consultarSaldo();

    return 0;
}



class Empleado {
public:
    string nombre;
    float salarioBase;
    float bonificacion;

    float calcularSalario() {
        return salarioBase + bonificacion;
    }

    void mostrarInformacion() {
        cout << "Empleado: " << nombre << endl;
        cout << "Salario base: $" << salarioBase << endl;
        cout << "Bonificacion: $" << bonificacion << endl;
        cout << "Salario total: $" << calcularSalario() << endl;
    }
};

int main() {
    Empleado empleado1;

    empleado1.nombre = "Juan";
    empleado1.salarioBase = 1500000;
    empleado1.bonificacion = 200000;

    empleado1.mostrarInformacion();

    return 0;
}




class Perro : public Animal {
public:
    void hacerSonido() override {
        cout << "El perro dice: Guau guau." << endl;
    }
};

class Gato : public Animal {
public:
    void hacerSonido() override {
        cout << "El gato dice: Miau." << endl;
    }
};

int main() {
    Perro perro1;
    Gato gato1;

    perro1.nombre = "Max";
    gato1.nombre = "Michi";

    cout << perro1.nombre << ": ";
    perro1.hacerSonido();

    cout << gato1.nombre << ": ";
    gato1.hacerSonido();

    return 0;
}






class Producto {
public:
    string nombre;
    float precio;
    int cantidad;

    float calcularTotal() {
        return precio * cantidad;
    }

    void mostrarProducto() {
        cout << "Producto: " << nombre << endl;
        cout << "Precio: $" << precio << endl;
        cout << "Cantidad: " << cantidad << endl;
        cout << "Total: $" << calcularTotal() << endl;
    }
};

int main() {
    Producto producto1;

    producto1.nombre = "Arroz";
    producto1.precio = 3000;
    producto1.cantidad = 5;

    producto1.mostrarProducto();

    return 0;
}

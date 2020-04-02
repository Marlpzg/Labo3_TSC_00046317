# Laboratorio 3
Técnicas de Simulación en Computadoras: Tercera práctica de laboratorio 

## Contenido

<p align="center"> Método de los elementos finitos para el problema de transferencia de calor
en una dimensión con funciones de forma lineales y con peso de Galerkin </p>

## Cambios en math_tools.h

```cpp
//Agregada la función para calcular la Inversa de una Matriz
void inverseMatrix(Matrix M, Matrix &Minv){
    Matrix Cof, Adj;
    float det = determinant(M);
    if(det == 0) 
        exit(EXIT_FAILURE);
    cofactors(M,Cof);
    transpose(Cof,Adj);
    productRealMatrix(1/det,Adj,Minv);
}
```

## Cambios en display_tools.h

```cpp
//Agregada una función para mostrar los vectores b
void showbs(vector<Vector> bs){
    for(int i=0;i<bs.size();i++){
        cout << "b del elemento "<< i+1 << ":\n";
        showVector(bs.at(i));
        cout << "*************************************\n";
    }
}

//Agregada una función para mostrar las matrices K
void showKs(vector<Matrix> Ks){
    for(int i=0;i<Ks.size();i++){
        cout << "K del elemento "<< i+1 << ":\n";
        showMatrix(Ks.at(i));
        cout << "*************************************\n";
    }
}
```

## Crear sel y tools
## Convertir tarea 2 en tools.h

<hr>
<p align="center">Para servirles, <strong>Equipo de Instructores</strong> </p>


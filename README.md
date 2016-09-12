# Coursera
//: Playground - noun: a place where people can play

import UIKit



enum Velocidades :Int{
   case Apagado = 0, VelocidadBaja = 20, VelocidadMedia = 50, VelocidadAlta = 120
    init(velocidadInicial : Velocidades){
    self = velocidadInicial
    }
    
}


class Auto{
    var velocidad : Velocidades
    init (){
        velocidad = Velocidades(velocidadInicial: . Apagado)
    
    }


    func  cambioDeVelocidad( ) -> ( actual : Int, velocidadEnCadena: String){
     var tipoDeVelocidad = ""
        let actual = velocidad.rawValue
        
        switch velocidad {
        case .Apagado:
            velocidad = .VelocidadBaja
            tipoDeVelocidad = "Apagado"
        case .VelocidadBaja:
            velocidad = .VelocidadMedia
            tipoDeVelocidad = "Velocidad Baja"
        case .VelocidadMedia:
            velocidad = .VelocidadAlta
            tipoDeVelocidad = "Velocidad Media"
        case .VelocidadAlta:
            velocidad = .VelocidadBaja
            tipoDeVelocidad = "Velocidad Alta"
            
        }
        return (actual,tipoDeVelocidad)
    }
    
    
}

Velocidades.VelocidadAlta.rawValue
Velocidades.VelocidadMedia.rawValue

Velocidades.Apagado.hashValue
Velocidades.Apagado.rawValue


let tablero = Auto()
for v in 1...20 {
let velocimetro = tablero.cambioDeVelocidad()
    print("\(v)\t\(velocimetro.actual)\t\(velocimetro.velocidadEnCadena)")

}


---
layout: post
category: blog
published: true
splash: "http://placehold.it/1600x500"
title: Phaser 1
---

Phaser es un framework en javascript/Typescript basado en pixi.js (para renderizar webgl) y muy inspirado en Flixel, el excelente framework para juegos de Flash.  Lo mas importante alrededor de Phaser es su activa comunidad y el poder de HTML5 que hay detràs.
La primera funcionalidad importante de toda herramienta para juegos es la opcion de la transicion de estados, por ejemplo la transicion entre el menu de inicio y el juego propiamente dicho.
El ciclo de ejecucion basico de phaser como en la mayoria de motores consiste en un ciclo infinito con dos eventos principales update)( y render().  En el primero se actualiza todo el escenario lògico (captura de teclado, colisiones, fisicas) y en el segundo se controla la forma de pintar los elementos en la pantalla.
 Si consideramos la pantalla del menu inicial y la comparamos con la del juego, podemos concluir que deben tratarse de ciclos de ejecuciòn diferentes.  Phaser permite esto mediante las escenas.  Cada escena puede tener su propio bloque de logica y render y ademas ofrece la transicion a nuevas escenas.  Ya existe un template que es el que vamos a usar en esta entrada.
 
 [Template]
 
 Para el actual proyecto voy a utilizar los muy completos recursos graficos bajo licencia cc de Kenney.
 Poder vincular una imagen en el juego tiene dos momentos, la carga, que es la que consume mas tiempo y se realiza en la precarga del juego.  Y la puesta en escena que sucede en el ciclo de ejecuciòn, definiendo sus coordenadas.
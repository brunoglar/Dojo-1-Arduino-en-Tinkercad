# **Documentación de Arduino en Tinkercad**

![Arduino](https://d1e4pidl3fu268.cloudfront.net/1e27d448-be48-4a6a-97e9-855e2321ad37/images.crop_222x168_38,0.preview.png)

##     **Integrantes**:
---
* ### Bruno Gaston Luna
* ### Carlos Ariel Martinez

## **Proyecto Dojo 1**
---

![Tinkercad](image.png "Vista previa, esquema en Tinkercad")


## **Consigna:**
---
El gobierno de la cuidad quiere actualizar los semáforos que tiene instalados. La empresa
“ScaraRobotics” gano la licitación y ahora les toca a los desarrolladores de la empresa generar
un proyecto low cost que cumpla con las especificaciones que el gobierno de la cuidad nos
impone, a saber las especificaciones son las siguientes:

1- El semáforo tiene que tener 2 leds de cada color como minimo, en caso de que uno se
rompa, lo ideal serian 3.

2- Tiene que implementar los tiempos correctos como se detallan a continuación.

3- El verde dura 45 segundos.

4- El amarillo dura 5 segundos.

5- Rojo dura 30 segundos.

6- Tiene que tener señalización para personas no videntes como se detalla a
continuación.

7- Durante el verde: No sonar.

8- Durante el amarillo: Tiene que sonar 1 vez cada 2 segundos en un tono suave.

9- Durante el rojo: Tiene que sonar 1 vez por segundo en un tono fuerte.

---


## **Función principal**
La **funcionalidad** del código a continuación, es la encargada de encender los **leds** y el **buzzer** tal como pide la consigna.

>**LED_ROJO1, LEDROJO2, LEDAMARILLO1, LEDAMARILLO2, LEDVERDE1, LEDVERDE2, BUZZER**



Son **#define** que utilizamos para asignar los leds y buzzer a cada pin en la placa de Arduino, a continuación una breve parte del código. Si desea ver el código completo en su totalidad, acceda mediante el link brindado al final del proyecto.

# 👨‍💻
```
#define LEDROJO1 12
#define LEDROJO2 11
#define LEDAMARILLO1 7
#define LEDAMARILLO2 6
#define LEDVERDE1 4
#define LEDVERDE2 3
#define	BUZZER 10

void encenderRojo(int led1, int led2, int buzzer);

void setup()
{
	pinMode(LEDROJO1, OUTPUT);
}
void loop()
{
 	  encenderRojo(LEDROJO1, LEDROJO2, BUZZER);
}

void encenderRojo(int led1, int led2, int buzzer){
	
  	digitalWrite(led1, HIGH);
  	digitalWrite(led2, HIGH);
  	for(int i = 0; i < 15; i++){
    	tone(buzzer, 1000);
      	delay(1000);
      	noTone(buzzer);
      	delay(1000);
  	}
  	digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);

}
```


# 🤖 *ENLACES A GDB Y TINKERCAD*
>**Apreta en el link para acceder al código en 
[GDB](https://onlinegdb.com/sfFZTfVYhX)**
---
>**Apreta en el link para acceder al proyecto y visualizar su funcionamiento en 
[TinkerCad](https://www.tinkercad.com/things/hTzddfy4eMr-copy-of-ingenious-jarv/editel?sharecode=XMAkSj8YNhMUiLO-ekCLCINNLASEASIpMq-K4fyIjj4)**
# sysa-smarthome

ein Home Automation System drinnen mehrere Actoren.
Environment simulieren mittles Actor in System und einen eignen Simulator im System und umschalten können.
Evnironment machen wir extra gibt in FH server der Wetter simuliert.
MQTT Server und System verbinden.
gRPC mal angucken, Fridge mit externe Ordersystem verbinden.

3 Hauptmerkmale der Actoren:
State
Behaviour also Logik
API

Akka Framework hat mqtt

UI: Webinterface empfohlen aber man kann auch CLI aber nicht empfohlen

Order System eine Applikation und das ganze SmartHome auch eine Applikation und Environment externes System einfach.

Wer schickt wem die Nachrichten kann man interne-Methodenaufrufe machen einfach halten. Und AC macht logik für temp die er von temp actor kriegt. Fridge hat eigene logik zb orderprocessing. Persistierung keine nur zur Luafzeitvariable und so.



![IMG_6983](https://github.com/user-attachments/assets/b2024388-99d6-4c84-920c-0b421f70ae94)

# Seminar:
* Fride hat Actoren wie Weight Space OrderProcessor, OrderPorcessor ist sowas wie die Validierung und die Nachricht an einem externen OrderSystem schickt. OrderProcessor fragt bei Weight und Space nach was der Zustand ist, wenn man bestellen kann... anhand einer Liste von Prdoukten die jeweils weight und space eigenschaften haben, wird weitergemacht.
* OrderSystem schickt die Nachricht zurück an OrderProcessor und der ändert den Zustand von der Fridge.

# Nombre del personaje 

 Árbol de Navidad y Chucky
# Creador 
Valeria Guadalupe Calvillo Mendoza
# Explicación de funcionamiento
Para crear un árbol navideño interactivo, necesitarás varios componentes electrónicos y materiales de construcción. El Arduino Uno será el cerebro del proyecto, controlando las luces LED RGB que decorarán el árbol y creando patrones de iluminación festivos. Un sensor de ultrasonido HC-SR04 detectará la proximidad de las personas, activando un motor servo que moverá un gorrito navideño en la parte superior del árbol. Además, un módulo de sonido reproducirá villancicos para añadir un toque musical. Todos estos componentes se montarán en una estructura hecha de cartulina o cartón, con una base sólida para mantener el árbol estable. Con el código adecuado, el árbol encenderá las luces, reproducirá música y moverá el gorrito cuando alguien se acerque, creando una experiencia navideña interactiva y divertida.

# Materiales a utilizar

![Captura de pantalla 2024-09-27 191515](https://github.com/user-attachments/assets/5781de0f-f037-40f0-96aa-b89066d11128)

![Captura de pantalla 2024-09-27 191522](https://github.com/user-attachments/assets/b2c0935c-7ee7-4932-8258-bbe11642822c)

# Materiales Para Chuky
![Captura de pantalla 2024-12-04 211619](https://github.com/user-attachments/assets/c5a9f9f7-eff9-41d5-8e57-72f2715f0550)
![Captura de pantalla 2024-12-04 211633](https://github.com/user-attachments/assets/71a7e6eb-d0c8-4185-afcd-09c29327318c)

# Software a utilizar
Thonny, Arduino,Node Red
# Dibujo de los  personajes

![Captura de pantalla 2024-09-27 192701](https://github.com/user-attachments/assets/01f83635-6659-4527-8eae-a9db2df7d7f0)

![Captura de pantalla 2024-12-04 212158](https://github.com/user-attachments/assets/b49d8221-0db4-4711-aaf3-c9ea9bcc9ee1)
# Programas en thonny

[ChukyPrograma.zip](https://github.com/user-attachments/files/18016988/ChukyPrograma.zip)
# Dode-Red
[
    {
        "id": "99f69a53d5120295",
        "type": "tab",
        "label": "Flow 13",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "6df1a4cf99279737",
        "type": "mqtt out",
        "z": "99f69a53d5120295",
        "name": "",
        "topic": "gds0642/buzzer_control",
        "qos": "2",
        "retain": "false",
        "respTopic": "",
        "contentType": "",
        "userProps": "",
        "correl": "",
        "expiry": "",
        "broker": "a8c30e5fff300a8a",
        "x": 470,
        "y": 140,
        "wires": []
    },
    {
        "id": "1af9091d2769806a",
        "type": "mqtt out",
        "z": "99f69a53d5120295",
        "name": "",
        "topic": "gds0642/led_control",
        "qos": "2",
        "retain": "false",
        "respTopic": "",
        "contentType": "",
        "userProps": "",
        "correl": "",
        "expiry": "",
        "broker": "a8c30e5fff300a8a",
        "x": 470,
        "y": 240,
        "wires": []
    },
    {
        "id": "145e6fda8d7b2d45",
        "type": "ui_switch",
        "z": "99f69a53d5120295",
        "name": "Switch Buzzer",
        "label": "Buzzer",
        "tooltip": "",
        "group": "6b889b2b8236553a",
        "order": 0,
        "width": "6",
        "height": "1",
        "passthru": true,
        "decouple": "false",
        "topic": "gds0642/buzzer_control",
        "topicType": "str",
        "style": "",
        "onvalue": "0",
        "onvalueType": "str",
        "onicon": "",
        "oncolor": "",
        "offvalue": "1",
        "offvalueType": "str",
        "officon": "",
        "offcolor": "",
        "animate": true,
        "className": "",
        "x": 250,
        "y": 140,
        "wires": [
            [
                "6df1a4cf99279737"
            ]
        ]
    },
    {
        "id": "5bd986aa10f473fa",
        "type": "ui_switch",
        "z": "99f69a53d5120295",
        "name": "Switch LEDs",
        "label": "LEDs",
        "tooltip": "",
        "group": "6b889b2b8236553a",
        "order": 1,
        "width": "6",
        "height": "1",
        "passthru": true,
        "decouple": "false",
        "topic": "gds0642/led_control",
        "topicType": "str",
        "style": "",
        "onvalue": "0",
        "onvalueType": "str",
        "onicon": "",
        "oncolor": "",
        "offvalue": "1",
        "offvalueType": "str",
        "officon": "",
        "offcolor": "",
        "animate": true,
        "className": "",
        "x": 250,
        "y": 240,
        "wires": [
            [
                "1af9091d2769806a"
            ]
        ]
    },
    {
        "id": "a8c30e5fff300a8a",
        "type": "mqtt-broker",
        "name": "",
        "broker": "broker.emqx.io",
        "port": "1883",
        "clientid": "",
        "autoConnect": true,
        "usetls": false,
        "protocolVersion": "4",
        "keepalive": "60",
        "cleansession": true,
        "autoUnsubscribe": true,
        "birthTopic": "",
        "birthQos": "0",
        "birthRetain": "false",
        "birthPayload": "",
        "birthMsg": {},
        "closeTopic": "",
        "closeQos": "0",
        "closeRetain": "false",
        "closePayload": "",
        "closeMsg": {},
        "willTopic": "",
        "willQos": "0",
        "willRetain": "false",
        "willPayload": "",
        "willMsg": {},
        "userProps": "",
        "sessionExpiry": ""
    },
    {
        "id": "6b889b2b8236553a",
        "type": "ui_group",
        "name": "Control",
        "tab": "c9f69c4b3b3cfea9",
        "order": 1,
        "disp": true,
        "width": "6",
        "collapse": true
    },
    {
        "id": "c9f69c4b3b3cfea9",
        "type": "ui_tab",
        "name": "Tablero",
        "icon": "dashboard",
        "order": 1,
        "disabled": false,
        "hidden": false
    }
]

# Programa para conectar a Node-Red el Arbol
[árbol_bien.zip](https://github.com/user-attachments/files/18017086/arbol_bien.zip)

# Coevaluación
Para mi y mi compañera Pao, fue un reto difícil pero no imposible, ya que pudimos trabajar bajo estrés y superar los errores que iban ocurriendo, como el problema con un sensor que se quemó y nos impedía avanzar. A pesar de los obstáculos, logramos mantener la calma y buscar soluciones juntos, lo que nos permitió seguir adelante con el proyecto. La experiencia fue un buen ejercicio de perseverancia y colaboración.


# Imagen de los examenes de cisco

# Módulo 1
![Captura de pantalla 2024-12-04 212859](https://github.com/user-attachments/assets/c1a249fb-657c-4eb9-a002-48a187a44311)
# Módulo 2
![Captura de pantalla 2024-12-04 213130](https://github.com/user-attachments/assets/5b232049-08c2-4cc0-9d8c-559c04284177)



# Módulo 3
![Captura de pantalla 2024-12-04 213231](https://github.com/user-attachments/assets/63403eeb-2c37-4503-94b1-e4eacdac4275)



# Módulo 4
![Captura de pantalla 2024-12-04 213409](https://github.com/user-attachments/assets/21f04e23-3f3a-4016-bbbc-ae8a5f139335)
# Módulo 5

![Captura de pantalla 2024-12-04 213548](https://github.com/user-attachments/assets/964a15ed-5678-44e8-9859-f966834f49c7)

# Módulo 6
![Captura de pantalla 2024-12-04 213812](https://github.com/user-attachments/assets/6adb7d1e-f6ce-4019-a2d4-58c69f3771b5)
# Examen Final
![Captura de pantalla 2024-12-04 213933](https://github.com/user-attachments/assets/470cfa4d-af49-40f0-bda3-d0caa0374b65)





































































































# 
# 
# 
# 

graph TD;
    VCC(5V) --> HC-SR04;
    GND --> HC-SR04;
    
    HC-SR04 -->|TRIG| Arduino_Digital(Arduino Pin Digital);
    HC-SR04 -->|ECHO (5V)| R1[1kΩ];
    
    R1 --> Nodo;
    Nodo -->|3.3V Seguro| Arduino_Entrada(Arduino Entrada);
    Nodo --> R2[2kΩ];
    
    R2 --> GND;

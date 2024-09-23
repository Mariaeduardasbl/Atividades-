# Atividades-
const int buttonPin = 2;
const int ledPin = LED_BUILTIN; // LED embutido

// contador para o número de pressionamentos do botão
int buttonPushCounter = 0;
// estado atual do botão
int buttonState = 0;
// estado anterior do botão
int lastButtonState = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  // lê o pino de entrada do botão
  buttonState = digitalRead(buttonPin);
  
  // verifica se o estado do botão mudou
  if (buttonState != lastButtonState) {
    if (buttonState == HIGH) {
      buttonPushCounter++;
      Serial.println("on");
      Serial.print("Número de pressionamentos do botão: ");
      Serial.println(buttonPushCounter);
    } else {
      Serial.println("off");
    }
    // pequena espera para evitar bouncing
    delay(50);
  }
  
  // salva o estado atual do botão
  lastButtonState = buttonState;
}

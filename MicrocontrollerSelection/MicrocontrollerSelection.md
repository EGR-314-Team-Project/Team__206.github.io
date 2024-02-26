# Microcontroller Selection

## Microcontroller Selection Table

The team went through a process to select the most suitable microcontroller for their project, beginning with the identification of project-specific requirements derived from problem definition and block diagram analysis. With a focus on GPIO pins, ADC channels, PWM channels, and communication interfaces like I2C, SPI, and UART, the team aimed to ensure compatibility with their project's needs. Following this, they researched and evaluated three potential microcontrollers, namely PIC18LF26K22, PIC16F18124, and PIC16F18855, by utilizing datasheets, product pages, application notes, code examples, and external resources. They also considered factors such as production unit cost, supply voltage range, maximum current, architecture, available IC packages, and programming capabilities. Each microcontroller was assessed for its strengths and weaknesses, including pros like code examples and ample I/O pins, and cons such as limited program memory or processing power. After thorough deliberation, they ranked the options based on how well they met the project requirements, ultimately selecting PIC Option 1 as the most suitable choice.
***
### 1. Project Specific Requirments and Datasheet Specifications

| Design Considerations  | Team Project Requirments | PIC Option 1 | PIC Option 2 | PIC Option 3 |
| ---------------------- | ------------------------ | ------------ | ------------ | ------------ |
| How many GPIO Pins?  | Need at least 10  | 27 | 28 | 36 |
| Built-in Analog to Digital Converter? How many?  | Need at least 2  | 20 | 19 | 29 |
| Built-in Hardware PWM? How many? | Need at least 1 | 10 | 3 | 4 |
|Built-in I2C? SPI? How many? | Need at least 2 I2C and 1 SPI | (2,2) | (2,2) | (2,2) |
| Built-in UART? How many? | Need at least 2 pins | 2 | 2 | 2 |
|Additional considerations specific to your project specifications (optional)| Since our project will be outside it must be able to operate from 0C-45C minimum | -40℃ to 85℃ | -40℃ to 85℃ | -40℃ to 85℃ |
***
### 2. Microcontroller Information and Part Details

| Microcontroller Considerations  | Instructions | PIC Option 1 | PIC Option 2 | PIC Option 3 |
| ------------------------------- | ------------ | ------------ | ------------ | ------------ |
| Part Number | Entire Part Number | PIC18LF26K22 | PIC16F18124 | PIC16F18855 |
| Link (URL) to Product Page | Do not paste links directly into the table. Instead, like them using a short URL command | [Link](https://www.microchip.com/en-us/product/pic18f26k22#document-table) | [Link](https://www.microchip.com/en-us/product/PIC18F24Q24#purchase-from-store) | [Link](https://www.microchip.com/en-us/product/pic16f18855) |
| Link (URL) to Data |  | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18%28L%29F2X-4XK22-Data-Sheet-40001412H.pdf) | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18F24-25Q24-Microcontroller-Data-Sheet-DS40002517.pdf) | [Link](https://ww1.microchip.com/downloads/en/DeviceDoc/400001802D.pdf) |
| Programming Hardware, Cost, and URL | Find on the Microcontroller Product Page | MPLAB® X, Free, [Link](https://www.microchip.com/development-tools/) | MPLAB® ICD 5 In-Circuit Debugger/Programmer,$399.99, [Link](https://www.microchip.com/en-us/development-tool/DV164055) | MPAB X, MPAB ICD, ICE, [Link](https://www.microchip.com/en-us/development-tool/dv244140) |
| Works with MPLAB® X Integrated Development Environment (IDE)? | Required | Yes | Yes | Yes |
| Works with Microchip Code Configurator? | Required | Yes | Yes | Yes |
***
### 3. Overall Pros, Cons, and Rankings for chosen Microcontrollers 

| Overall Pros, Cons, and Rankings | Two for each | PIC Option 1 | PIC Option 2 | PIC Option 3 |
| -------------------------------- | -------------| -------------| -------------| -------------|
| Overall Pros                     | Two Each     | 1. Plenty of Code examples provided. 2. Contains 3 PWM Channels to implement additional features. | 1. Meets all requirements with redundancy on necessary features. 2. Cost-effective | 1. Has an ample amount of I/O pins 2. Enhanced core features with multiple PWM and EUSART modules for serial communication |
| Overall Cons                     | Two Each     | 1. Lacking in Safety Features. 2. Few/Limited code examples | 1. Few/Limited Code Examples. 2. Not many External Resources. | 1. Limited processing power. 2. Limited program memory |
| Rankings                         | First Choice = 1, Second Choice = 2, Third Choice = 3 | 1 | 2 | 3 |

***
### 4. Final Microcontroller Choice and Rationale

**Choice:** Option 1

**Rationale:**
PIC18LF26K22 is going to be our first option due to various reasons.  It offers a wide range of features suitable for various applications. These features include a high-performance RISC CPU, numerous I/O pins, analog peripherals, communication interfaces like SPI, I2C, and UART, timers, and PWM modules. The "LF" in its name signifies its low power consumption characteristics, making it suitable for battery-powered or low-power applications. This is crucial for devices that need to operate for extended periods without external power sources. In addition, The PIC 18LF26K22 is versatile, capable of handling diverse tasks across different applications, from simple control tasks to more complex embedded systems. Its rich set of peripherals and memory options contribute to this versatility. Considering its array of features, the PIC 18LF26K22 emerges as the most convenient choice, offering ample I/O pins alongside the capability for simultaneous communication via both SPI and I2C interfaces and low power requirments which is best suited for our project.

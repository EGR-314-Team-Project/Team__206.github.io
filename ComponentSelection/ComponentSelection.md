# Component Selection

Embedded systems design demands a nuanced approach to selecting major components, encompassing both electrical blocks and critical mechanical elements. This report delves into the evaluation of potential solutions for each component, considering off-the-shelf and custom options while adhering to EGR 314 specifications.

With a focus on providing three viable alternatives for each major component, this analysis aims to illuminate the decision-making process behind our design choices. The rationale for each selection is intricately tied to project specifications, ensuring that our design is not only optimized for performance and efficiency but also aligns seamlessly with the project's unique requirements. This report lays the groundwork for an insightful exploration into the key aspects of our embedded systems design.

## Major Component Selection

**Component Tables in Appendix ...**


### Motor Driver

**Choice:** Option 3

**Rationale:** The IFX9201SGAUMA1 is the most suitable option mainly due to its high current handling limit, and protection, alongside a higher PWM frequency support over the DRV8835. The addition of a sleep mode during the inactive phases allows for efficient power management in the IFX9201SGAUMA1 by minimizing current consumption. Having this feature being absent in the TB6612FNG and DRV8835 DSSR is profoundly advantageous for the IFX9201SGAUMA1 motor driver, integrated into a mobile weather station powered by batteries, helping to conserve energy and extend battery life. These factors collectively contribute to the suitability of the IFX9201SGAUMA1 for the specific requirements of the mobile weather station project.

***
### Motor

**Choice:** Option 1

**Rationale:** Selecting a standard DC motor for our project presents several key benefits. The bidirectional rotation capability eliminates the necessity for two motors operating in opposite directions, streamlining the design. DC motors are renowned for their durability, ensuring a longer operational life, a crucial factor for the sustained functionality of our mobile weather station.
Moreover, the inherent characteristic of DC motors to operate at lower noise levels aligns perfectly with our project's requirements. By opting for a DC motor, we not only ensure reliable bidirectional motion but also prioritize a quieter operation, contributing to the overall effectiveness and acceptance of our mobile weather station among its environmental surroundings.

***
### Temperature Sensor

**Choice:** Option 3

**Rationale:** As a requirement our sensors need to communicate with I2C. While Option 2 offers us the greatest range of temperature sensing, we are unable to select it due to its output being PWM. Additionally, it was the most expensive option. That left Options 1 and 2. 
At first Option 1 seemed like a good pick during our research. It had a stronger price, a decent temperature operating range and communicated in I2C. However, when we discovered Option 3 it was better in every way compared to Option 1. It had multiple communication types (our group found flexibility a positive), had a greater temperature range than Option 1 and it did all of this for only $0.45 compared to Option 1’s $4.50. For our team the choice became clear at that point. 

***
### Humidity Sensor

**Choice:** Option 1

**Rationale:** The SHT40-AD1B-R2 is the preferred sensor due to its cost-effectiveness compared to the other humidity sensors available on the market. The sensor offers high precision and accuracy which is crucial for the successful operation of the weather station. The sensor also provides a digital output and supports standard communication interfaces like SPI or I2C and can be easily integrated into microcontroller based systems.

***
### Non-Inverting Op-Amp

**Choice:** Option 1

**Rationale:** The LM324D op-amp is the preferred choice due to the team’s budget constraints and its wide availability makes it a good reliable choice. The fact that it comes in a package of 4 makes it all the more convenient and flexible for the user. The LM324D also has very straightforward usage and has uncomplicated specifications. This simplicity makes it suitable for our project where an easy-to-implement op-amp is required.

***
### Switching Regulator

**Choice:** Option 2

**Rationale:** Our first option was to explore Option 1. Our team is very comfortable with the LM2575T and it met our requirements. However, it is unfortunately through-hole, so it had to be eliminated. This left us with Options 2 and 3. For our project we have a system that runs on 3.3V. However, there is one component that operates outside that range at 9V. So this regulator has to be able to meet those requirements. Since both were the same in price, we decided to focus on this. Option 3 maxes out at 7V when it comes to V output while the can go way beyond that (max 29V). It is possible that the 500mA output could be a source of problems for option 2 but a preliminary investigation of current requirements seems to suggest that current demand will not be that high. Therefore our team decided to go with the one within the Voltage rating of our motor which was option 2.

***
### Rechargable Power Source

**Choice:** Option 3

**Rationale:** To begin with we started out with option 2. While really good for our overall system because it is near the system voltage (3.3V), we found it limited us when it came to picking our op amps and upon further investigation of our motors, it can’t apply enough voltage for it to function. 
Between Options 1 and 3, there were a few things to take into consideration. First 7V and 9.6V are all pretty common V ratings for batteries and all worked with our chosen Regulators. For our selected motor, it is rated at 9V. We wanted to get as close to that Voltage as possible to ensure that we reduce the potential problems we might encounter. Option 3 is the best for this. In addition to this, Option 3 was a lot closer to 9V for a more cost effective price. Lastly, we found that the current for Option 1 was a bit excessive for what we needed in our project. This all lead to us selecting Option 3

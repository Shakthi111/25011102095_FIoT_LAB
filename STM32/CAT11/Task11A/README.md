# CAT 11 – ESP8266 Wi-Fi and TCP Server Configuration

**EXP CAT:** CAT 11  
**TASK:** TASK 11A  
**NAME:** ESP8266 Wi-Fi Connection and TCP Server Setup

## Objective
To configure the ESP8266/Wemos module with AT commands, join a Wi-Fi access point and start a TCP server.

## Hardware and Software Requirements
- STM32F4 microcontroller board
- ESP8266 / Wemos module
- STM32CubeMX
- Keil uVision

## Pin Connections

| STM32F4 Pin | Wemos / ESP8266 |
|---|---|
| PC6 (USART6_TX) | RX |
| PC7 (USART6_RX) | TX |
| GND | GND |

## Circuit Diagram

![Circuit Diagram](circuit.png)

## UART Configuration

| Parameter | Configuration |
|---|---|
| UART Peripheral | USART6 |
| Baud Rate | 115200 |
| Word Length | 8 Bits |
| Stop Bits | 1 |
| Parity | None |
| Mode | Transmitter and Receiver |

## Working Principle
- The STM32 sets up USART6 to talk to the Wemos module.
- It waits for the Wemos module to finish starting up.
- It sends AT commands and reads the replies.
- The ESP8266 is put into Wi-Fi station mode.
- It joins the specified Wi-Fi access point.
- Multiple connections are enabled.
- A TCP server is started on port 80.
- The Wemos module's IP address is then requested.

## AT Commands Used

| Purpose | AT Command |
|---|---|
| Test communication | `AT` |
| Set Wi-Fi station mode | `AT+CWMODE=1` |
| Connect to Wi-Fi | `AT+CWJAP` |
| Enable multiple connections | `AT+CIPMUX=1` |
| Start TCP server on port 80 | `AT+CIPSERVER=1,80` |
| Get IP address | `AT+CIFSR` |

## Algorithm
1. Initialise the HAL library.
2. Configure the system clock.
3. Initialise GPIO and USART6.
4. Wait for the Wemos module to start up.
5. Send `AT` to test communication.
6. Set Wi-Fi station mode.
7. Join the Wi-Fi access point.
8. Enable multiple connections.
9. Start the TCP server on port 80.
10. Request the Wemos IP address.

## HAL Functions Used
- `HAL_Init()`
- `HAL_Delay()`
- `HAL_UART_Init()`
- `HAL_UART_Transmit()`
- `HAL_UART_Receive()`
- `HAL_GetTick()`
- `HAL_RCC_OscConfig()`
- `HAL_RCC_ClockConfig()`

## Source Code
`Core/Src/main.c`

## Result
The STM32 issues AT commands that set the ESP8266 up for Wi-Fi connectivity and TCP server operation.

## Inference
This experiment demonstrates UART communication with the ESP8266 and configuring it as a TCP server on a Wi-Fi network.

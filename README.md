# Hall-Effect-mouse-V1
This is a mouse with hall effect switches that I made after 1 week of starting electrical engineering( since I'm in high school math and some things might be flawed but I will update the designs)

Wiring and components is as follow:
U1/stm32f042k6ux

PB0: SDA
PB1: SCL
VDD: VBUS and Ground through C1
VSS: Ground 
PA0: Vout U2
PA1: Vout U3
PA2: SW1 through R2 
PA3: SW2
PA4: SW3
PA5: SW4
PA6: SCLK
PA7: M0SI
PA8: TxD0
PA9: RxD0
PA11: D-
PA12: D+ through R1
PA13: MISO
PA14: CS
PA15: IRQ

U2/drv5053vaqdbzr

VCC: Vbus
GND: Ground
Vout: PA1

U3/drv5053vaqdbzr

VCC: Vbus
GND: Ground
Vout: PA0

U4/PMW3360dm-t2qu

VDD: Vbus
GND: Ground 
LED_P: Vbus
Reset: SW1 through R3
SCLK: PA6
MOSI: PA7
MISO: PA13
CS: PA14
P1/USB_C_Plug_USB2.0

Vbus: CC, Ground and other components power connections 
CC: Vbus
D-: PA11
D+: PA12 through R
GND: Vbus and Ground
Shield: Ground through C3

MOD1/ESP32-WROOM-32

3v3: Vbus
TxDO: PA8
RxDO: PA9
GND: ground 
GND: ground 
GND: ground 
GND: ground 

U5/MPR121QR2

VDD: Vbus
VSS: Ground parallel C2
SDA: PB0
SCL: PB1
IRQ: PA15

SW1

PIN1: PA2 through R2 and reset U4
PIN2: Ground

SW2

PIN1: PA3
PIN2: Ground

SW3

PIN1: PA4
PIN2: Ground

SW4

PIN1: PA5
PIN2: Ground


C1: VDD and VDD to ground 

C2: Parallel to VSS and ground 

C3: Shield and ground

C4: Vbus and GND

C5: Parallel to U4GND and ground 


R1: PA12 and D+

R2: PA2 and SW1

R3: Parallel to R2 connected to SW1 wiring 

R4: Connected in parallel Vbus and LED_P

R5: Connected in parallel to VDD and Vbus

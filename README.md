# Open-Frame1
![Open F1 logo stroke mode](https://user-images.githubusercontent.com/28491168/173758069-75f6b53f-6dd0-4fa1-a8ac-bf687989da07.png)
An open-source rectangle hardware project for smash, prioritizing ease of assembly and cost.

[Announcement/Overview video](frame1.gg)

[Example build guide](frame1.gg)

[Arte's code (pico-rectangle)](https://github.com/JulienBernard3383279/pico-rectangle)

### Overview
Currently, this project contains the files necessary to create your own Frame1 Light near-equivalent PCB. The files to get this PCB made with parts soldered on are already compiled for you (see: Fabrication Files), but the original schematics are also here if you want to make changes.

The boards are compatible with Rev 1 Heavy and Rev 1/2 Light cases (to be sold in waves on the Frame1.gg website). Switch plate files are included for those who want to design their own case, but full files/guides for creating your own case are planned.


# The Board
![whole board](https://user-images.githubusercontent.com/28491168/173757642-d8927d98-c139-43c3-8cbe-2c92696d7a9a.png)
### Overview
In desktop computer terms, the Rapberry Pico is your CPU, and the OF1 PCB is the motherboard. It just feeds power to the Raspberry Pico, routes the USB signal, and connects your switches to the correct pins. 

To accomplish all 3 of these tasks, you will have multiple options. The options you pick will largely depend on budget and level of soldering experience.

## Your Options
- To solder the pico to the board, you can use pin headers or solder the pico straight to the surface. If you use the pin headers, the USB connection will need to be routed via a cable. If you surface mount the pico, you will need to solder in the USB pads on the surface of the pico through the back of the OF1 board (see: Example Builds).
- A surface mount diode can be placed by JLC, but there's also a footprint for a through-hole diode. The through-hole one is easier to solder in if you're doing it yourself. Only use one. Do not populate both.
- You can use Kailh hotswap switches or solder the switches in directly.

Other than the pico, the OF1 board houses 4 main components, and only 2 are mandatory: 
- The main type-c port
- a diode
- a secondary internal type-c port (optional, used to more easily routing the usb signal from the pico to the main port)
- Hotswap sockets
![board overview](https://user-images.githubusercontent.com/28491168/173209396-a105109a-8bd6-4859-9a19-c7479b79a35b.png)

I would recommend having them assembled via a 3rd party assembly service such as JLC, as type-c ports can be difficult and time-consuming.

## Example Builds

These are examples of the main paths you can take when making a board. All of them assume a board assembled through a 3rd party with at least the main type-c port and diode soldered on already. 

The choice of connecting kailh hotswap sockets vs soldering switches in directly doesn't depend on any of the other assembly choices. The sockets are cheap, and take just as many solder joints to complete as soldering in switches directly. For this reason, I will also be assuming hotswap sockets are be used. It's the option that makes the most sense for the majority of people.

### The Easy Build
This build prioritizes ease of assembly above everything. I highly recommend this path for beginners to soldering. It has the second shortest build time, and the least potential for error. Requires the internal secondary type-c connector.
![easy mode](https://user-images.githubusercontent.com/28491168/173758831-21a278c2-3cd2-4326-9130-c9e73005c1ce.png)


The 3 main steps are:
- Solder in the pico via pin headers (link to that section of the crane vid here)
- Connect a USB micro-b to type-c cable from the pico to the port on the board. (These can be found in 6" lengths on sites like Amazon)
- Solder in hotswap sockets

### The Fast & Cheap build
This build is the cheapest, and assuming no errors, fastest build. Recommended for those with a lot of soldering experience
![expert mode](https://user-images.githubusercontent.com/28491168/173760333-405eabf4-2221-4371-b168-0d9663b95e7e.png)

The 3 main steps are:
- Solder the pico on the surface of the OF1 board using the pads and castellated edges on the pico. Alignment is extremely important. You can use the pico's corner holes as a visual guide. Or, you can use something like a matching set of M2 screws and nuts to physically align and hold the board in place (At the time of writing I have not personally tried screws but it should work).
- To connect the USB from the pico to the main board, you need to add solder to these holes on the back of the OF1 board. They make contact with the USB pads on the back of the pico. You may need to pre-tin the test pads before-hand, but your mileage may vary
- Solder in hotswap sockets


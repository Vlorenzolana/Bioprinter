# Bioprinter README

## What is the Bioprinter?

The Bioprinter is a modified MakerBot Thing-O-Matic (2010) designed for 3D printing biological materials instead of plastic. By replacing the standard extruder with a peristaltic pump and utilizing open-source software, this setup allows for precise deposition of biological substances onto petri dishes. The system is ideal for experimental biofabrication, microbial patterning, and DIY biohacking projects.

## How It Works

### 1. **Hardware Setup**

- **Base Printer:** MakerBot Thing-O-Matic (2010) with:
  - Arduino ATMega 1280
  - MightyBoard v2.4
  - ECB 3.6 electronics board
- **Extruder Replacement:**
  - Remove the standard stepper motor and plastic extruder.
  - Install a peristaltic pump with a stepper motor, such as this one: [12V-24V Peristaltic Pump](https://www.ebay.co.uk/itm/152485216708).

### 2. **Software Installation**

- **ReplicatorG 0040**: The control software for sending G-code to the printer.
  - Download: [http://replicat.org/](http://replicat.org/)
- **Processing**: A programming environment used to design and generate patterns for printing.
  - Download: [https://processing.org/](https://processing.org/)

### 3. **Preparing Petri Dishes with LB Medium**

- **Materials Needed:**
  - Square petri dishes (120mm x 120mm) or rounded glass petri dishes (200mm O.D., 20mm H)
  - LB agar medium (DIY recipe below)
- **DIY LB Medium Agar Recipe:**
  - 52.5g beef powder (e.g., Knorr meat soup cubes)
  - 1L water
  - 21g sugar
  - 37.5g agar
  - Mix and pour into yogurt crystal jars, filling 1/3 of each.
  - Cover loosely with aluminum foil or caps.
  - Place jars in a pressure cooker with water and a support grid to prevent spilling.
  - Autoclave for 15-20 minutes after reaching full pressure.
- **Successfully Grown Bacteria:**
  - *Micrococcus luteus* (yellow)
  - *Micrococcus aurantiacus* (orange)
  - *Micrococcus roseus* (pink)
  - *Jacinthobacterium violaceum* (purple)

### 4. **Designing Patterns in Processing**

- Create a custom Processing script to generate the desired pattern.
- Save background images in the "data" folder within the Processing script directory.

### 5. **Setting Up ReplicatorG**

- Open ReplicatorG 0040 and configure the machine:
  - Select Machine Type: *Thingomatic w/HBP and Stepstruder MK7*
  - Choose the correct USB port (e.g., `/dev/tty/usb.serial-A600euUF`)
  - Connect the printer
  - Load the G-code file generated from Processing
  - Start the print job

### 6. **Troubleshooting and Drivers**

If using a MacBook Pro (2017) with macOS Sierra 10.9 or older, additional drivers may be required:

- Arduino Drivers: [Download Arduino-1.8.5](https://downloads.arduino.cc/arduino-1.8.5-macosx.zip)
- FTDI USB Serial Driver: [Download v2.4.2](http://download.tinbert.com/ired2/FTDIUSBSerialDriver_v2_4_2.dmg)
- CH340G Driver (for non-original ATMega 1280): [Download from GitHub](https://github.com/adrianmihalko/ch340g-ch34g-ch34x-mac-os-x-driver/blob/master/CH34x_Install_V1.4.zip)
- Alternative Firmware: [Sailfish Installer](http://www.sailfishfirmware.com/doc/install.html)

### 7. **Running the Bioprinter**

1. Start ReplicatorG and calibrate: `File -> Scripts -> Calibration -> Thing-O-Matic_calibration.gcode`
2. Load and start your print job.
3. Observe the bioprinter deposit biological material onto the prepared petri dishes.

### 8. **Credits**

Special thanks to the contributors:

- **Vanessa Lorenzo** - Concept & Design Engineering
- **Javier Roel** - IT Assitance Media Lab Prado Madrid
- **Richard Timsi** - Troubleshooting Hackuarium Lausanne
- **Daniel Petrosemoli** - Makerspace Technician Media Lab Prado Madrid

For more information, visit: 
[Bioprinter - Hybridoa](https://hybridoa.org/bioprinter) 
[Pr(ink)t plastic its fantastic](https://hybridoa.org/prinkt-plastic-its-fantastic) 

---

Enjoy experimenting with bioprinting!


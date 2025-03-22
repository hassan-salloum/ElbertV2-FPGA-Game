# FPGA Spartan 3A Shooting Game  

This project walks you through building your first FPGA game step by step. You'll learn about VGA functionality, synchronization, and FPGA programming using the **Elbert V2 Spartan 3A** development board.  

---

## Requirements & Setup  
1️⃣We will use the **Elbert V2 Spartan 3A FPGA** board:[Numato Elbert V2 FPGA Board](https://numato.com/product/elbert-v2-spartan-3a-fpga-development-board)    
2️⃣To program the FPGA, install the required USB driver: [Download USB CDC Driver](https://productdata.numato.com/assets/downloads/common/numato_lab_usb_cdc_driver.zip)    
3️⃣We will use **Xilinx ISE 14.7** for FPGA development: [Download Xilinx ISE 14.7](https://www.xilinx.com/member/forms/download/xef.html?filename=Xilinx_ISE_S6_Win10_14.7_ISE_VMs_0206_1.zip)  
4️⃣To upload bitstreams to the FPGA, install **ElbertV2Config.exe**: [Download ElbertV2Config](https://productdata.numato.com/assets/downloads/fpga/elbertv2/ElbertV2Config.exe)  
5️⃣ **Additional Resources**: [Elbert V2 Documentation](https://docs.numato.com/doc/elbert-v2-spartan-3a-fpga-development-board/)  

---

## VGA Functionality  

To display graphics, we need to understand how the VGA controller works.  

### 📌VGA Controller Simplified view  
![image](https://github.com/user-attachments/assets/e7333760-7048-4121-a9a6-636c664ee5b6)
 
### 📌Horizontal & Vertical Synchronization  
This explains how VGA timing works and how we can use it to draw images in the **VGA_sync module**.  
![image](https://github.com/user-attachments/assets/6dad003c-cafb-440d-9191-594125f6ebbd)

---

## 💻 Main Code Structure  

The project consists of **four core modules**:  
- **🟢 TopModule** → Declares the VGA system inputs/outputs.  
- **🔵 U1 - IN_CLOCK_OUT** → Converts **12 MHz** input to **25 MHz** output.  
- **🟣 U2 - Counter** → Uses **25 MHz** input to synchronize **VGA_sync** and **TopModule**.  
- **🟠 U3 - VGA_sync** → Handles **vertical & horizontal synchronization** and **video output**.  

---

## Get Started  

1️⃣ **Set up your FPGA board** and install all required software.  
2️⃣ **Understand the VGA synchronization** and how it drives pixel rendering.  
3️⃣ **Compile & upload the code** to test the game on your FPGA board.  

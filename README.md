strings: 
10707C0.cab  - installer gak?
11623C0.cab

cypress brige firmware???
file:///home/xpi/dl/CY7C64013.PDF


65c816 cpu - 
 - some sram

pdip28 at27c512 otp rom -- dump it with minipro + T48  adapter?
https://github.com/queueRAM/ti_graph_link

74hc165 - shift in parallel in sr , Input front panel control mux? possible connected to 65c816
https://www.ti.com/lit/ds/symlink/sn74hc165.pdf?ts=1736697169924&ref_url=https%253A%252F%252Fwww.google.com%252F


some werid pal/gal 
https://www.microchip.com/en-us/product/atf16v8b#Documentation

22cv10 more weird gal
https://ww1.microchip.com/downloads/en/DeviceDoc/doc0735.pdf
https://github.com/simon-frankau/galette <- programs gals
weird config place: https://github.com/simon-frankau/galette/blob/master/src/chips.rs


S&S Research  Midi Processor II 

input optocoupler ilq615
https://www.vishay.com/docs/83652/ild615.pdf

input 74hc4046 pll
output stage?? appears to be 74hc595 shift registers.. interesting to drive those at the need 1mhz 

output leds get snother 595

74hc4052 4:1mux x2

others:
http://www.gweep.net/~prefect/eng/mtp2/
??? related product (same skin0 https://www.potm.org/resources/Unitor/emagic_unitor8_mkII_amt8_manual.pdf

tc dumps: 
https://service-tcgroup.tcelectronic.com/files/Tech_Service/C400XL/Schematics/p20203-AAB_Online.pdf

usb enumer dmesg from freebsd:
ugen0.6: <vendor 0x07fd MIDI Timepiece AV> at usbus0 
usbconfig:
ugen0.6: <MIDI Interface Mark of the Unicorn> at usbus0, cfg=0 md=HOST spd=FULL (12Mbps) pwr=ON (100mA)

{
    UE_CONTROL_OK       : 17
    UE_ISOCHRONOUS_OK   : 0
    UE_BULK_OK          : 0
    UE_INTERRUPT_OK     : 0
    UE_CONTROL_FAIL     : 0
    UE_ISOCHRONOUS_FAIL : 0
    UE_BULK_FAIL        : 0
    UE_INTERRUPT_FAIL   : 0
}

usbcofig dump_all_config_desc:
ugen0.6: <MIDI Interface Mark of the Unicorn> at usbus0, cfg=0 md=HOST spd=FULL (12Mbps) pwr=ON (100mA)


 Configuration index 0

    bLength = 0x0009 
    bDescriptorType = 0x0002 
    wTotalLength = 0x0089 
    bNumInterfaces = 0x0004 
    bConfigurationValue = 0x0001 
    iConfiguration = 0x0000  <no string>
    bmAttributes = 0x0080 
    bMaxPower = 0x0032 

    Interface 0
      bLength = 0x0009 
      bDescriptorType = 0x0004 
      bInterfaceNumber = 0x0000 
      bAlternateSetting = 0x0000 
      bNumEndpoints = 0x0002 
      bInterfaceClass = 0x00ff  <Vendor specific>
      bInterfaceSubClass = 0x0001 
      bInterfaceProtocol = 0x00ff 
      iInterface = 0x0000  <no string>

     Endpoint 0
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0081  <IN>
        bmAttributes = 0x0003  <INTERRUPT>
        wMaxPacketSize = 0x001e 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 

     Endpoint 1
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0002  <OUT>
        bmAttributes = 0x0002  <BULK>
        wMaxPacketSize = 0x0008 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 


    Interface 1
      bLength = 0x0009 
      bDescriptorType = 0x0004 
      bInterfaceNumber = 0x0001 
      bAlternateSetting = 0x0000 
      bNumEndpoints = 0x0002 
      bInterfaceClass = 0x00ff  <Vendor specific>
      bInterfaceSubClass = 0x0002 
      bInterfaceProtocol = 0x00ff 
      iInterface = 0x0000  <no string>

     Endpoint 0
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0081  <IN>
        bmAttributes = 0x0003  <INTERRUPT>
        wMaxPacketSize = 0x0010 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 

     Endpoint 1
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0002  <OUT>
        bmAttributes = 0x0001  <ISOCHRONOUS>
        wMaxPacketSize = 0x000e 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 


    Interface 2
      bLength = 0x0009 
      bDescriptorType = 0x0004 
      bInterfaceNumber = 0x0002 
      bAlternateSetting = 0x0000 
      bNumEndpoints = 0x0002 
      bInterfaceClass = 0x00ff  <Vendor specific>
      bInterfaceSubClass = 0x0003 
      bInterfaceProtocol = 0x00ff 
      iInterface = 0x0000  <no string>

     Endpoint 0
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0081  <IN>
        bmAttributes = 0x0001  <ISOCHRONOUS>
        wMaxPacketSize = 0x0010 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 

     Endpoint 1
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0002  <OUT>
        bmAttributes = 0x0001  <ISOCHRONOUS>
        wMaxPacketSize = 0x000d 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 


    Interface 3
      bLength = 0x0009 
      bDescriptorType = 0x0004 
      bInterfaceNumber = 0x0003 
      bAlternateSetting = 0x0000 
      bNumEndpoints = 0x0002 
      bInterfaceClass = 0x00ff  <Vendor specific>
      bInterfaceSubClass = 0x0004 
      bInterfaceProtocol = 0x00ff 
      iInterface = 0x0000  <no string>

     Endpoint 0
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0081  <IN>
        bmAttributes = 0x0003  <INTERRUPT>
        wMaxPacketSize = 0x0010 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 

     Endpoint 1
        bLength = 0x0007 
        bDescriptorType = 0x0005 
        bEndpointAddress = 0x0002  <OUT>
        bmAttributes = 0x0003  <INTERRUPT>
        wMaxPacketSize = 0x000c 
        bInterval = 0x0001 
        bRefresh = 0x0000 
        bSynchAddress = 0x0000 

      Additional Descriptor

      bLength = 0x24
      bDescriptorType = 0x03
      bDescriptorSubType = 0x4d
       RAW dump: 
       0x00 | 0x24, 0x03, 0x4d, 0x00, 0x49, 0x00, 0x44, 0x00, 
       0x08 | 0x49, 0x00, 0x20, 0x00, 0x54, 0x00, 0x69, 0x00, 
       0x10 | 0x6d, 0x00, 0x65, 0x00, 0x70, 0x00, 0x69, 0x00, 
       0x18 | 0x65, 0x00, 0x63, 0x00, 0x65, 0x00, 0x20, 0x00, 
       0x20 | 0x41, 0x00, 0x56, 0x00




windows USB Tree Viewer is cool:
  =========================== USB Port5 ===========================

  Connection Status        : 0x01 (Device is connected)
  Port Chain               : 2-5
  Properties               : 0x01
   IsUserConnectable       : yes
    PortIsDebugCapable      : no
     PortHasMultiCompanions  : no
      PortConnectorIsTypeC    : no
      ConnectionIndex          : 0x05 (Port 5)
      CompanionIndex           : 0
       CompanionHubSymLnk      : USB#ROOT_HUB30#4&1e3e598c&0&0#{f18a0e88-c30c-11d0-8815-00a0c906bed8}
        CompanionPortNumber     : 0x14 (Port 20)
         -> CompanionPortChain   : 2-20

               ========================== Summary =========================
               Vendor ID                : 0x07FD (Mark of the Unicorn, Inc.)
               Product ID               : 0x0001
               Manufacturer String      : ---
               Product String           : *ERROR* iProduct=119 but String Descriptor not found
               Serial                   : ---
               USB Version              : 1.0
               Port maximum Speed       : High-Speed (Companion Port 2-20 is doing the SuperSpeed)
               Device maximum Speed     : Full-Speed
               Device Connection Speed  : Full-Speed
               Self powered             : no
               Demanded Current         : 100 mA
               Used Endpoints           : 1

	  ======================== USB Device ========================

	          +++++++++++++++++ Device Information ++++++++++++++++++
	          Device Description       : MOTU USB MIDI (WDM) for 64 bit Windows
	          Device Path              : \\?\USB#VID_07FD&PID_0001#5&1378c611&0&5#{a5dcbf10-6530-11d2-901f-00c04fb951ed} (GUID_DEVINTERFACE_USB_DEVICE)
	          Kernel Name              : \Device\USBPDO-8
	          Device ID                : USB\VID_07FD&PID_0001\5&1378C611&0&5
	          Hardware IDs             : USB\VID_07FD&PID_0001&REV_0101 USB\VID_07FD&PID_0001
	          Driver KeyName           : {36fc9e60-c465-11cf-8056-444553540000}\0010 (GUID_DEVCLASS_USB)
	          Driver                   : \SystemRoot\System32\Drivers\MotuUsb64.sys (Version: 4.0.5.7483  Date: 2013-04-30  Company: MOTU)
	          Driver Inf               : C:\Windows\inf\oem64.inf
	          Legacy BusType           : PNPBus
	          Class                    : USB
	          Class GUID               : {36fc9e60-c465-11cf-8056-444553540000} (GUID_DEVCLASS_USB)
	          Service                  : MotuUsb64
	          Enumerator               : USB
	          Location Info            : Port_#0005.Hub_#0003
	          Address                  : 5
	          Location IDs             : PCIROOT(0)#PCI(1400)#USBROOT(0)#USB(5), ACPI(_SB_)#ACPI(PCI0)#ACPI(XHC_)#ACPI(RHUB)#ACPI(HS05)
	          Container ID             : {e697c5ef-f783-11ee-8423-e82aea69b5c6}
	          Manufacturer Info        : Mark of the Unicorn
	          Capabilities             : 0x14 (Removable, UniqueID)
	          Status                   : 0x0180600A (DN_DRIVER_LOADED, DN_STARTED, DN_DISABLEABLE, DN_REMOVABLE, DN_NT_ENUMERATOR, DN_NT_DRIVER)
	          Problem Code             : 0
	          Address                  : 5
	          EnhancedPowerMgmtEnabled : 0
	          Power State              : D0 (supported: D0, D3, wake from D0)

	                  ---------------- Connection Information ---------------
	                  Connection Index         : 0x05 (Port 5)
	                  Connection Status        : 0x01 (DeviceConnected)
	                  Current Config Value     : 0x00 (Configuration 0)   ERROR: must be non-zero
	                  Device Address           : 0x06 (6)
	                  Is Hub                   : 0x00 (no)
	                  Device Bus Speed         : 0x01 (Full-Speed)
	                  Number of open Pipes     : 0x00 (0 pipes to data endpoints)
	                  Data (HexDump)           : 05 00 00 00 12 01 00 01 FF 01 00 08 FD 07 01 00   ................
			       01 01 00 77 00 01 00 01 00 06 00 00 00 00 00 01   ...w............
				               00 00 00                                          ...

					    --------------- Connection Information V2 -------------
					    Connection Index         : 0x05 (5)
					    Length                   : 0x10 (16 bytes)
					    SupportedUsbProtocols    : 0x03
					     Usb110                  : 1 (yes, port supports USB 1.1)
					      Usb200                  : 1 (yes, port supports USB 2.0)
					       Usb300                  : 0 (no, port not supports USB 3.0) -> but Companion Port 2-20 does
					        ReservedMBZ             : 0x00
					        Flags                    : 0x00
					         DevIsOpAtSsOrHigher     : 0 (Device is not operating at SuperSpeed or higher)
					          DevIsSsCapOrHigher      : 0 (Device is not SuperSpeed capable or higher)
					           DevIsOpAtSsPlusOrHigher : 0 (Device is not operating at SuperSpeedPlus or higher)
					            DevIsSsPlusCapOrHigher  : 0 (Device is not SuperSpeedPlus capable or higher)
					             ReservedMBZ             : 0x00
					             Data (HexDump)           : 05 00 00 00 10 00 00 00 03 00 00 00 00 00 00 00   ................

					                 ---------------------- Device Descriptor ----------------------
					                 bLength                  : 0x12 (18 bytes)
					                 bDescriptorType          : 0x01 (Device Descriptor)
					                 bcdUSB                   : 0x100 (USB Version 1.0)
					                 bDeviceClass             : 0xFF (Vendor Specific)
					                 bDeviceSubClass          : 0x01
					                 bDeviceProtocol          : 0x00
					                 bMaxPacketSize0          : 0x08 (8 bytes)
					                 idVendor                 : 0x07FD (Mark of the Unicorn, Inc.)
					                 idProduct                : 0x0001
					                 bcdDevice                : 0x0101

looking for vendor/xref 0x07fd 0x0001
https://github.com/torvalds/linux/blob/9bffa1ad25b8b3b95d8f463e5c24dabe3c87d54d/sound/usb/midi.c#L1700
    /* MOTU Fastlane */
                 EXTERNAL_PORT(0x07fd, 0x0001, 0, "%s MIDI A"),
                 EXTERNAL_PORT(0x07fd, 0x0001, 1, "%s MIDI B"),

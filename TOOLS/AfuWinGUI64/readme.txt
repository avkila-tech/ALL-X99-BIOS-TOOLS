AFU (AMI Firmware Update) is a package of utilities used 
to update the system BIOS under various operating systems.  

Note: AFU only works for APTIO with SMI FLASH support.
      Compatible with Aptio 3, 4, and 4.5.

The package includes:

- AFUWINx64 3.09.03.1462
- AFUWINGUIx64 3.09.03.1462
- AFU User Guide

To run, extract all of the files from the folder with the name corresponding to the desired operating system.


Usage (applies to AFUWIN, AFUDOS, AFUEFI and AFUEFI64...
       for usage of AFUBSD and AFULNX see help files provided in their folders):
------------------------------------------------------------------
AFUEFI <BIOS ROM File Name> [Option 1] [Option 2]
Or
AFUEFI <Input or Output File Name> <Command>
Or
AFUEFI <Command>

BIOS ROM File Name
The mandatory field is used to specify path/filename of the BIOS ROM file with extension.

Commands
The mandatory field is used to select an operation mode.
- /O		Save current ROM image to file                            
- /U		Display ROM File's ROMID                                  
- /S		Refer to Options: /S                                      
- /D		Verification test of given ROM File without flashing BIOS.
- /OAD		Refer to Options: /OAD                                    
- /A		Refer to Options: /A                                      
- /CLNEVNLOG	Refer to Options: /CLNEVNLOG                              
Options
The optional field used to supply more information for flashing BIOS ROM. Following lists the supported optional parameters and format:
- /CLRCFG 	Program without preserving setup configuration
- /BCPALL 	Save all question values before flash
- /DPC  	Don't Check Aptio 4 and Aptio 5 platform.
- /MEUL:        Program ME Entire Firmware Block, which supports
                Production.BIN and PreProduction.BIN files.
- /Q  		Silent execution                                          
- /X  		Don't Check ROM ID                                        
- /CAF  	Compare ROM file's data with Systems is different or      
		not, if not then cancel related update.                   
- /S  		Display current system's ROMID                            
- /JBC          Don't Check AC adapter and battery                     
- /HOLEOUT:  	Save specific ROM Hole according to RomHole GUID.         
		NewRomHole1.BIN /HOLEOUT:GUID                             
- /SP  		Preserve Setup setting.                                   
- /Rn  		Preserve SMBIOS type N during programming(n=0-255)        
- /R  		Preserve ALL SMBIOS structure during programming          
- /B  		Program Boot Block                                        
- /P  		Program Main BIOS                                         
- /K  		Program all non-critical blocks.
- /N  		Program NVRAM                                             
- /Kn  		Program n'th non-critical block(n=0-15). 
- /HOLE:  	Update specific ROM Hole according to RomHole GUID.       
		NewRomHole1.BIN /HOLE:GUID                                
- /L  		Program all ROM Holes.                                    
- /Ln  		Program n'th ROM Hole only(n=0-15).                       
- /E  		Program Embedded Controller Block.
- /OAD  	Delete Oem Activation key                                 
- /A  		Oem Activation file                                       
- /E  		Program Embedded Controller Block
- /ECUF  	Update EC BIOS when newer version is detected.            
- /ME  		Program ME Entire Firmware Block.                         
- /MEUF  	Program ME Ignition Firmware Block.                       
- /CLNEVNLOG  	Clear Event Log.                                          
- /CAPSULE  	Override Secure Flash policy to Capsule                   
- /RECOVERY  	Override Secure Flash policy to Recovery                  
- /EC  		Program Embedded Controller Block. (Flash Type)           
- /CMD: 	Send special command to BIOS. /CMD:{xxx, xxx, xxx}
- /OEMCMD:	Send special value to BIOS. /OEMCMD:xxx
- /REBOOT  	Reboot after programming.                                 
- /SHUTDOWN  	Shutdown after programming.                               
- /FDR		Flash Flash-Descriptor Region.(*1)
- /GBER		Flash GBE Region.(*1)
- /MER		Flash Entire ME Region.(*1)
- /OPR		Flash Operation Region of SPS.(*1)
- /PDR          Flash PDR Region.(*1)                  

(*1)If BIOS ME Module have report, AFU will be show this command.

Rules
- Any parameter encolsed by < > is a mandatory field.
- Any parameter enclosed by [ ] is an optional field.
- <Commands> cannot co-exist with any [Options].
- Main BIOS image is default flashing area if no any option present.
- [/REBOOT], [/X], and [/S] will enable [/P] function automatically.
- If [/B] present alone, there is only the Boot Block area to be updated.
- If [/N] present alone, there is only the NVRAM area to be updated.
- If [/E] present alone, there is only the Embedded Controller block to be updated.

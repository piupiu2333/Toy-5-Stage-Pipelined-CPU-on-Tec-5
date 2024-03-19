###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = 80C51
COMPILER = "ASEM-51 (Proteus)"
TARGET = Debug
SHELL = E:\WINDOWS\system32\cmd.exe

## Tools general options

## Processing Tools
ASM=asem.exe
DDX=ASEMDDX.EXE
#  E:/Users/fmy/Documents/Tencent Files/768317729/FileRecv/pt5 (1)/pt5/PipelineTec5/PipelineTec5/80C51/Debug/Debug.HEX: TOOL=ASM
#  Post: $(DDX) $(DDXFLAGS) Debug.lst
#     E:/Users/fmy/Documents/Tencent Files/768317729/FileRecv/pt5 (1)/pt5/PipelineTec5/PipelineTec5/80C51/1.asm

# Build tree:
all:	Debug

Debug:	Debug.HEX

Debug.HEX:	../1.asm 
	$(ASM) "..\1.asm" "Debug.HEX" Debug.lst $(ASMFLAGS)  /INCLUDES:"F:\New Folder\Tools\ASEM51"
	$(DDX) $(DDXFLAGS) Debug.lst

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Debug.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Debug.HEX
	rm -rf Debug.SDI

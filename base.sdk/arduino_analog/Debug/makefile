################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
ELFSIZE += \
arduino_analog.elf.size \


# All Target
all: arduino_analog.elf secondary-outputs

# Tool invocations
arduino_analog.elf: $(OBJS) ../src/lscript.ld $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MicroBlaze gcc linker'
	mb-gcc -L"/home/junhonglin/Xilinx/PYNQ_Car/base.sdk/bsp_iop_arduino_mb/iop_arduino_mb/lib" -Wl,-T -Wl,../src/lscript.ld -mlittle-endian -mcpu=v9.6 -mxl-soft-mul -Wl,--no-relax -o "arduino_analog.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

arduino_analog.elf.size: arduino_analog.elf
	@echo 'Invoking: MicroBlaze Print Size'
	mb-size arduino_analog.elf  |tee "arduino_analog.elf.size"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(S_UPPER_DEPS)$(C_DEPS)$(ELFSIZE) arduino_analog.elf
	-@echo ' '

secondary-outputs: $(ELFSIZE)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

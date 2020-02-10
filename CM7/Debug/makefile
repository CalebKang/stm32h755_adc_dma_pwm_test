################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32H7xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include Common/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
stm32h755_adc_dma_test_CM7.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
stm32h755_adc_dma_test_CM7.list \

OBJCOPY_BIN += \
stm32h755_adc_dma_test_CM7.bin \


# All Target
all: stm32h755_adc_dma_test_CM7.elf secondary-outputs

# Tool invocations
stm32h755_adc_dma_test_CM7.elf: $(OBJS) $(USER_OBJS) C:\Workspace\_Demo\stm32h755_adc_dma_test\CM7\STM32H755ZITX_FLASH.ld
	arm-none-eabi-gcc -o "stm32h755_adc_dma_test_CM7.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"C:\Workspace\_Demo\stm32h755_adc_dma_test\CM7\STM32H755ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="stm32h755_adc_dma_test_CM7.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

stm32h755_adc_dma_test_CM7.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "stm32h755_adc_dma_test_CM7.list"
	@echo 'Finished building: $@'
	@echo ' '

stm32h755_adc_dma_test_CM7.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "stm32h755_adc_dma_test_CM7.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

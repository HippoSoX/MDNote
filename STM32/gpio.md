# GPIO控制

本文介绍在STM32CubeIDE开发环境下实现对GPIO口的配置和控制。

## 配置GPIO口

GPIO口的配置由IDE内置的MX来实现。打开ProjectName.ioc文件，在芯片引脚示意图Pinout view上点需要配置的IO口，选择相应的模式。然后在左侧目录Categories的System Core中打开GPIO，继续配置相关模式。其中，User Label将使用宏定义对该IO口进行命名。

GPIO相关的函数和定义分布在HAL库文件stm32f1xx_hal_gpio.c和头文件stm32f1xx_hal_gpio.h中，系统自动生成的配置代码则主要分布在gpio.h和gpio.c中，当IO口复用时也会分布在相应外设的配置文件中。

在 HAL 库开发中，初始化 GPIO 是通过 GPIO 初始化函数完成： 
`void HAL_GPIO_Init(GPIO_TypeDef  *GPIOx, GPIO_InitTypeDef *GPIO_Init)`

这个函数有两个参数。第一个参数是用来指定需要初始化的GPIO对应的GPIO组，取值范围为GPIOA~GPIOE。第二个参数为初始化参数结构体指针，对应类型GPIO_InitTypeDef。我们需要配置的参数可以通过这个结构体的定义来看一下：

```C
/**
  * @brief GPIO Init structure definition
  */
typedef struct
{
  uint32_t Pin;       /*!< Specifies the GPIO pins to be configured.
                           This parameter can be any value of @ref GPIO_pins_define */

  uint32_t Mode;      /*!< Specifies the operating mode for the selected pins.
                           This parameter can be a value of @ref GPIO_mode_define */

  uint32_t Pull;      /*!< Specifies the Pull-up or Pull-Down activation for the selected pins.
                           This parameter can be a value of @ref GPIO_pull_define */

  uint32_t Speed;     /*!< Specifies the speed for the selected pins.
                           This parameter can be a value of @ref GPIO_speed_define */
} GPIO_InitTypeDef;
```

举个例子

```c
GPIO_Initure.Pin=GPIO_PIN_9|GPIO_PIN_10;  //PF9,10 
GPIO_Initure.Mode=GPIO_MODE_OUTPUT_PP;  //推挽输出 
GPIO_Initure.Pull=GPIO_PULLUP;     //上拉 GPIO_Initure.Speed= 
GPIO_SPEED_FREQ_HIGH;  //高速 HAL_GPIO_Init(GPIOF,&GPIO_Initure); 
```

## stm32f1xx_hal_gpio.h


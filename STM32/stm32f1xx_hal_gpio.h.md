# stm32f1xx_hal_gpio.h

## GPIO 参数定义

### GPIO_InitTypeDef 初始化参数结构体

GPIO_InitTypeDef 此结构体定义了GPIO口初始化参数的结构体，包含了初始化所需要的参数。

Pin 指定了GPIO口的pin口号，参数范围为GPIO_PIN_0~GPIO_PIN_15，或GPIO_PIN_ALL。

Mode 指定了GPIO口的模式。

Pull 指定了IO口是上拉还是下拉。

Speed 指定了IO口的速率。

```c
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

### GPIO_PinState GPIO口的输出状态枚举

输出状态：输出0，为GPIO_PIN_RESET；输出1，为GPIO_PIN_SET。

```c
/**
  * @brief  GPIO Bit SET and Bit RESET enumeration
  */
typedef enum
{
  GPIO_PIN_RESET = 0u,
  GPIO_PIN_SET
} GPIO_PinState;
```

### GPIO_PIN_Define GPIO pin参数的宏定义

GPIO端口号的宏定义：GPIO_PIN_Num（0~15）。

```c
#define GPIO_PIN_0                 ((uint16_t)0x0001)  /* Pin 0 selected    */
#define GPIO_PIN_1                 ((uint16_t)0x0002)  /* Pin 1 selected    */
#define GPIO_PIN_2                 ((uint16_t)0x0004)  /* Pin 2 selected    */
#define GPIO_PIN_3                 ((uint16_t)0x0008)  /* Pin 3 selected    */
#define GPIO_PIN_4                 ((uint16_t)0x0010)  /* Pin 4 selected    */
#define GPIO_PIN_5                 ((uint16_t)0x0020)  /* Pin 5 selected    */
#define GPIO_PIN_6                 ((uint16_t)0x0040)  /* Pin 6 selected    */
#define GPIO_PIN_7                 ((uint16_t)0x0080)  /* Pin 7 selected    */
#define GPIO_PIN_8                 ((uint16_t)0x0100)  /* Pin 8 selected    */
#define GPIO_PIN_9                 ((uint16_t)0x0200)  /* Pin 9 selected    */
#define GPIO_PIN_10                ((uint16_t)0x0400)  /* Pin 10 selected   */
#define GPIO_PIN_11                ((uint16_t)0x0800)  /* Pin 11 selected   */
#define GPIO_PIN_12                ((uint16_t)0x1000)  /* Pin 12 selected   */
#define GPIO_PIN_13                ((uint16_t)0x2000)  /* Pin 13 selected   */
#define GPIO_PIN_14                ((uint16_t)0x4000)  /* Pin 14 selected   */
#define GPIO_PIN_15                ((uint16_t)0x8000)  /* Pin 15 selected   */
#define GPIO_PIN_All               ((uint16_t)0xFFFF)  /* All pins selected */

#define GPIO_PIN_MASK              0x0000FFFFu /* PIN mask for assert test */
```

### GPIO_MODE_Define GPIO mode参数宏定义

GPIO口模式配置的宏定义。

|宏名|模式|
|--|--|
|GPIO_MODE_INPUT|浮空输入|
|GPIO_MODE_OUTPUT_PP|推挽输出|
|GPIO_MODE_OUTPUT_OD|开漏输出|
|GPIO_MODE_AF_PP|复用推挽输出|
|GPIO_MODE_AF_OD|复用开漏输出|
|GPIO_MODE_AF_INPUT|复用输入|
|GPIO_MODE_ANALOG|模拟输入|
|GPIO_MODE_IT_RISING|上升沿触发的外部中断模式|
|GPIO_MODE_IT_FALLING|下降沿触发的外部中断模式|
|GPIO_MODE_IT_RISING_FALLING|上升和下降沿触发的外部中断模式|
|GPIO_MODE_EVT_RISING|上升沿触发的外部事件模式|
|GPIO_MODE_EVT_FALLING|下降沿触发的外部事件模式|
|GPIO_MODE_EVT_RISING_FALLING|上升和下降沿触发的外部事件模式|


```c
#define  GPIO_MODE_INPUT                        0x00000000u   /*!< Input Floating Mode                   */
#define  GPIO_MODE_OUTPUT_PP                    0x00000001u   /*!< Output Push Pull Mode                 */
#define  GPIO_MODE_OUTPUT_OD                    0x00000011u   /*!< Output Open Drain Mode                */
#define  GPIO_MODE_AF_PP                        0x00000002u   /*!< Alternate Function Push Pull Mode     */
#define  GPIO_MODE_AF_OD                        0x00000012u   /*!< Alternate Function Open Drain Mode    */
#define  GPIO_MODE_AF_INPUT                     GPIO_MODE_INPUT          /*!< Alternate Function Input Mode         */

#define  GPIO_MODE_ANALOG                       0x00000003u   /*!< Analog Mode  */

#define  GPIO_MODE_IT_RISING                    0x10110000u   /*!< External Interrupt Mode with Rising edge trigger detection          */
#define  GPIO_MODE_IT_FALLING                   0x10210000u   /*!< External Interrupt Mode with Falling edge trigger detection         */
#define  GPIO_MODE_IT_RISING_FALLING            0x10310000u   /*!< External Interrupt Mode with Rising/Falling edge trigger detection  */

#define  GPIO_MODE_EVT_RISING                   0x10120000u   /*!< External Event Mode with Rising edge trigger detection               */
#define  GPIO_MODE_EVT_FALLING                  0x10220000u   /*!< External Event Mode with Falling edge trigger detection              */
#define  GPIO_MODE_EVT_RISING_FALLING           0x10320000u   /*!< External Event Mode with Rising/Falling edge trigger detection       */
```

### GPIO_SPEED_Define GPIO speed参数宏定义

GPIO最大输出频率的定义：快HIGH、中MEDIUM、慢LOW。

```c
#define  GPIO_SPEED_FREQ_LOW              (GPIO_CRL_MODE0_1) /*!< Low speed */
#define  GPIO_SPEED_FREQ_MEDIUM           (GPIO_CRL_MODE0_0) /*!< Medium speed */
#define  GPIO_SPEED_FREQ_HIGH             (GPIO_CRL_MODE0)   /*!< High speed */
```

### GPIO_PULL_Define GPIO pull参数的宏定义

GPIO上拉与下拉的模式定义：上拉PULLUP、下拉PULLDOWN和没有NOPULL。

```c
#define  GPIO_NOPULL        0x00000000u   /*!< No Pull-up or Pull-down activation  */
#define  GPIO_PULLUP        0x00000001u   /*!< Pull-up activation                  */
#define  GPIO_PULLDOWN      0x00000002u   /*!< Pull-down activation                */
```

## 宏定义函数（中断标志相关）

### __HAL_GPIO_EXTI_GET_FLAG(__EXTI_LINE__) 获取GPIO口外部中断标志的函数

获取外部中断的标志，0还是1。
参数：GPIO_PIN_Num(0~15)
返回值：SET还是RESET。SET表示输出为1，RESET表示输出为0。

```c
/**
  * @brief  Checks whether the specified EXTI line flag is set or not.
  * @param  __EXTI_LINE__: specifies the EXTI line flag to check.
  *         This parameter can be GPIO_PIN_x where x can be(0..15)
  * @retval The new state of __EXTI_LINE__ (SET or RESET).
  */
#define __HAL_GPIO_EXTI_GET_FLAG(__EXTI_LINE__) (EXTI->PR & (__EXTI_LINE__))
```

### __HAL_GPIO_EXTI_CLEAR_FLAG(__EXTI_LINE__) 清除外部中断位标志的函数

```c
/**
  * @brief  Clears the EXTI's line pending flags.
  * @param  __EXTI_LINE__: specifies the EXTI lines flags to clear.
  *         This parameter can be any combination of GPIO_PIN_x where x can be (0..15)
  * @retval None
  */
#define __HAL_GPIO_EXTI_CLEAR_FLAG(__EXTI_LINE__) (EXTI->PR = (__EXTI_LINE__))
```

### __HAL_GPIO_EXTI_GET_IT(__EXTI_LINE__) 获取GPIO口外部中断标志的函数

```c
/**
  * @brief  Checks whether the specified EXTI line is asserted or not.
  * @param  __EXTI_LINE__: specifies the EXTI line to check.
  *          This parameter can be GPIO_PIN_x where x can be(0..15)
  * @retval The new state of __EXTI_LINE__ (SET or RESET).
  */
#define __HAL_GPIO_EXTI_GET_IT(__EXTI_LINE__) (EXTI->PR & (__EXTI_LINE__))
```

### __HAL_GPIO_EXTI_CLEAR_FLAG(__EXTI_LINE__) 清除外部中断位标志的函数

```c
/**
  * @brief  Clears the EXTI's line pending bits.
  * @param  __EXTI_LINE__: specifies the EXTI lines to clear.
  *          This parameter can be any combination of GPIO_PIN_x where x can be (0..15)
  * @retval None
  */
#define __HAL_GPIO_EXTI_CLEAR_IT(__EXTI_LINE__) (EXTI->PR = (__EXTI_LINE__))
```

### __HAL_GPIO_EXTI_GENERATE_SWIT(__EXTI_LINE__) 在GPIO口引起一个软件中断

```c
/**
  * @brief  Generates a Software interrupt on selected EXTI line.
  * @param  __EXTI_LINE__: specifies the EXTI line to check.
  *          This parameter can be GPIO_PIN_x where x can be(0..15)
  * @retval None
  */
#define __HAL_GPIO_EXTI_GENERATE_SWIT(__EXTI_LINE__) (EXTI->SWIER |= (__EXTI_LINE__))
```

## GPIO 控制函数原型

### HAL_GPIO_Init GPIO口初始化函数

GPIO口用这个函数进行初始化。
参数：
1. 第一个为GPIO口所在IO组：GPIO（A~D）
2. 第二个为GPIO口初始化参数句柄：GPIO_InitTypeDef

```c
/* Initialization and de-initialization functions *****************************/
void  HAL_GPIO_Init(GPIO_TypeDef  *GPIOx, GPIO_InitTypeDef *GPIO_Init);
void  HAL_GPIO_DeInit(GPIO_TypeDef  *GPIOx, uint32_t GPIO_Pin);
```

### HAL_GPIO_ReadPin 读取GPIO口的输出状态的函数

读取GPIO口的输出状态，输出是0还是1。
参数：
1. 第一个为GPIO口所在IO组：GPIO（A~D）
2. 第二个为GPIO口的端口号：GPIO_PIN_Num（0~15）
返回值： GPIO_PIN_RESET，代表输出0；GPIO_PIN_SET，代表输出1。

```c
/**
  * @brief  Reads the specified input port pin.
  * @param  GPIOx: where x can be (A..G depending on device used) to select the GPIO peripheral
  * @param  GPIO_Pin: specifies the port bit to read.
  *         This parameter can be GPIO_PIN_x where x can be (0..15).
  * @retval The input port pin value.
  */
GPIO_PinState HAL_GPIO_ReadPin(GPIO_TypeDef *GPIOx, uint16_t GPIO_Pin);
```

### HAL_GPIO_WritePin 设置GPIO口的输出状态的函数

设置GPIO口的输出状态，输出为是0还是1。
参数：
1. 第一个为GPIO口所在IO组：GPIO（A~D）
2. 第二个为GPIO口的端口号：GPIO_PIN_Num（0~15）
3. 第三个为GPIO口的输出状态：GPIO_PIN_RESET，代表输出0；GPIO_PIN_SET，代表输出1。

```c
/**
  * @brief  Sets or clears the selected data port bit.
  *
  * @note   This function uses GPIOx_BSRR register to allow atomic read/modify
  *         accesses. In this way, there is no risk of an IRQ occurring between
  *         the read and the modify access.
  *
  * @param  GPIOx: where x can be (A..G depending on device used) to select the GPIO peripheral
  * @param  GPIO_Pin: specifies the port bit to be written.
  *          This parameter can be one of GPIO_PIN_x where x can be (0..15).
  * @param  PinState: specifies the value to be written to the selected bit.
  *          This parameter can be one of the GPIO_PinState enum values:
  *            @arg GPIO_PIN_RESET: to clear the port pin
  *            @arg GPIO_PIN_SET: to set the port pin
  * @retval None
  */
void HAL_GPIO_WritePin(GPIO_TypeDef *GPIOx, uint16_t GPIO_Pin, GPIO_PinState PinState);
```

### HAL_GPIO_TogglePin 反转GPIO口的输出状态的函数

反转GPIO口的输出状态。
参数：
1. 第一个为GPIO口所在IO组：GPIO（A~D）
2. 第二个为GPIO口的端口号：GPIO_PIN_Num（0~15）

```c
/**
  * @brief  Toggles the specified GPIO pin
  * @param  GPIOx: where x can be (A..G depending on device used) to select the GPIO peripheral
  * @param  GPIO_Pin: Specifies the pins to be toggled.
  * @retval None
  */
void HAL_GPIO_TogglePin(GPIO_TypeDef *GPIOx, uint16_t GPIO_Pin);
```

### HAL_GPIO_LockPin 锁定GPIO口的函数

锁定GPIO口的输出状态，直到下一次reset前不能被修改/再次设置。
参数：

1. 第一个为GPIO口所在IO组：GPIO（A~D）
2. 第二个为GPIO口的端口号：GPIO_PIN_Num（0~15）

```c
/**
* @brief  Locks GPIO Pins configuration registers.
* @note   The locking mechanism allows the IO configuration to be frozen. When the LOCK sequence
*         has been applied on a port bit, it is no longer possible to modify the value of the port bit until
*         the next reset.
* @param  GPIOx: where x can be (A..G depending on device used) to select the GPIO peripheral
* @param  GPIO_Pin: specifies the port bit to be locked.
*         This parameter can be any combination of GPIO_Pin_x where x can be (0..15).
* @retval None
*/
HAL_StatusTypeDef HAL_GPIO_LockPin(GPIO_TypeDef *GPIOx, uint16_t GPIO_Pin);
```

### HAL_GPIO_EXTI_IRQHandler

发生外部中断时需要这个函数。
参数
1. 第一个为GPIO口的端口号：GPIO_PIN_Num（0~15）

```c
/**
  * @brief  This function handles EXTI interrupt request.
  * @param  GPIO_Pin: Specifies the pins connected EXTI line
  * @retval None
  */
void HAL_GPIO_EXTI_IRQHandler(uint16_t GPIO_Pin);
```

### __weak HAL_GPIO_EXTI_Callback

发生外部中断时调用。虚函数，需要自行重写。

```c
/**
  * @brief  EXTI line detection callbacks.
  * @param  GPIO_Pin: Specifies the pins connected EXTI line
  * @retval None
  */
__weak void HAL_GPIO_EXTI_Callback(uint16_t GPIO_Pin);
```


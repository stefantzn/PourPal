/* USER CODE BEGIN Includes */
#include "stm32f4xx_hal.h"
/* USER CODE END Includes */

/* Private variables ---------------------------------------------------------*/
/* USER CODE BEGIN PV */
GPIO_InitTypeDef GPIO_InitStruct = {0};
/* USER CODE END PV */

int main(void)
{
  /* ... (existing code) */

  /* USER CODE BEGIN 2 */
  /* Configure LED Pin */
  __HAL_RCC_GPIOA_CLK_ENABLE();    // Enable the GPIOA clock

  GPIO_InitStruct.Pin = GPIO_PIN_5; // Pin 5 is connected to the onboard LED on Nucleo boards
  GPIO_InitStruct.Mode = GPIO_MODE_OUTPUT_PP;
  GPIO_InitStruct.Speed = GPIO_SPEED_FREQ_LOW;
  HAL_GPIO_Init(GPIOA, &GPIO_InitStruct);
  /* USER CODE END 2 */

  /* Infinite loop */
  while (1)
  {
    /* USER CODE BEGIN 3 */
    HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5); // Toggle the state of the LED pin
    HAL_Delay(1000); // Delay for 1000 milliseconds (1 second)
    /* USER CODE END 3 */
  }
}

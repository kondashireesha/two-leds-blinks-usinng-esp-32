#include <stdio.h>
#include "freertos/FreeRTOS.h"
#include "freertos/task.h"
#include "driver/gpio.h"

#define LED1_GPIO GPIO_NUM_2
#define LED2_GPIO GPIO_NUM_4

void app_main(void) {
    // Configure GPIOs
    gpio_reset_pin(LED1_GPIO);
    gpio_set_direction(LED1_GPIO, GPIO_MODE_OUTPUT);

    gpio_reset_pin(LED2_GPIO);
    gpio_set_direction(LED2_GPIO, GPIO_MODE_OUTPUT);

    while (1) {
        // Turn on LED1, off LED2
        gpio_set_level(LED1_GPIO, 1);
        gpio_set_level(LED2_GPIO, 0);
        vTaskDelay(500 / portTICK_PERIOD_MS);

        // Turn off LED1, on LED2
        gpio_set_level(LED1_GPIO, 0);
        gpio_set_level(LED2_GPIO, 1);
        vTaskDelay(500 / portTICK_PERIOD_MS);
    }
}

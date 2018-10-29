1.修改 src/SdFat/SdFatConfig.h
//#define ENABLE_SOFTWARE_SPI_CLASS 0
#define ENABLE_SOFTWARE_SPI_CLASS 1

2.修改 Repetier.h

#include "src/SdFat/SdFat.h"

enum LsAction {LS_SerialPrint,LS_Count,LS_GetFilename};
class SDCard
{
public:

#if ENABLE_SOFTWARE_SPI_CLASS
    // SdFat software SPI template
    SdFatSoftSpi<SOFT_MISO_PIN, SOFT_MOSI_PIN, SOFT_SCK_PIN> fat;   	// 2.添加
#else
    SdFat fat;
#endif

3.修改 pins.h

在主板408,413定义添加：
#define SDSUPPORT 1 
#define SDCARDDETECTINVERTED 0
#define ENABLE_SOFTWARE_SPI_CLASS 1
const uint8_t SOFT_MISO_PIN = 50;
const uint8_t SOFT_MOSI_PIN = 51;
const uint8_t SOFT_SCK_PIN  = 52;

4.AZSMZ 12864 OLED

修改ui.cpp 
#ifdef U8GLIB_SH1106_SW_SPI
    u8g_InitSPI(&u8g, &u8g_dev_sh1106_128x64_sw_spi,  UI_DISPLAY_D4_PIN, UI_DISPLAY_ENABLE_PIN, UI_DISPLAY_RS_PIN, UI_DISPLAY_D5_PIN, U8G_PIN_NONE);
#endif

修改DisplayList.h

// For AZSMZ 12864 LCD
//#undef U8GLIB_ST7565_NHD_C2832_HW_SPI
//#define U8GLIB_ST7565_NHD_C2832_SW_SPI
//#define UI_ROTATE_180

#define U8GLIB_SH1106_SW_SPI    // For AZSMZ 12864 OLED

5.ESP8266 WIFI 端口
修改 Configuration.h

#define BLUETOOTH_SERIAL  2
#define BLUETOOTH_BAUD  115200

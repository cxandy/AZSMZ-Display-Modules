   #Panel
panel.enable                                 true             # set to true to enable the panel code
panel.lcd                                    viki2				# st7565_glcd
panel.contrast		                     15					  # 15 For azsmz lcd blue; 48 For azsmz lcd green; 
panel.rough_contrast		               36					# 36 For azsmz lcd
panel.is_sh1106				         1            # For AZSMZ OLED

panel.spi_channel                            0                 # spi channel to use  ; GLCD EXP1 Pins 3,5 (MOSI, SCLK)
panel.spi_cs_pin                             1.22              # spi chip select     ; GLCD EXP1 Pin 4
panel.a0_pin								 2.6			   
panel.encoder_a_pin                          4.28!^            # encoder pin         ; GLCD EXP2 Pin 3
panel.encoder_b_pin                          1.27!^            # encoder pin         ; GLCD EXP2 Pin 5
panel.click_button_pin                       3.26!^            
panel.buzz_pin                               1.30        
panel.reverse								 1

panel.external_sd                            true              # set to true if there is an extrernal sdcard on the panel
panel.external_sd.spi_channel                0                 # set spi channel the sdcard is on
panel.external_sd.spi_cs_pin                 0.16              # set spi chip select for the sdcard
panel.external_sd.sdcd_pin                   3.25!^            # sd detect signal (set to nc if no sdcard detect)
      
panel.menu_offset                            0                 # some panels will need 1 here
panel.encoder_resolution                     4   

panel.alpha_jog_feedrate                     6000              # x jogging feedrate in mm/min
panel.beta_jog_feedrate                      6000              # y jogging feedrate in mm/min
panel.gamma_jog_feedrate                     6000               # z jogging feedrate in mm/min

panel.hotend_temperature                     185               # temp to set hotend when preheat is selected
panel.bed_temperature                        60                # temp to set bed when preheat is selected

 # Example of a custom menu entry, which will show up in the Custom entry.
 # NOTE _ gets converted to space in the menu and commands, | is used to separate multiple commands
custom_menu.power_on.enable                  true              #
custom_menu.power_on.name                    Power_on          #
custom_menu.power_on.command                 M80               #

custom_menu.power_off.enable                 true              #
custom_menu.power_off.name                   Power_off         #
custom_menu.power_off.command                M81               #

custom_menu.fan_on.enable                    true              #
custom_menu.fan_on.name                      Fan_on          #
custom_menu.fan_on.command                   M106               #

custom_menu.fan_off.enable                   true              #
custom_menu.fan_off.name                     Fan_off         #
custom_menu.fan_off.command                  M107               #

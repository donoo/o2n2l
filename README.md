# o2n2l

Simple Node-red integration to connect to lovelace UI. 

<img width="1065" alt="image" src="https://user-images.githubusercontent.com/32016319/202849663-e4a097f6-7472-45f0-a354-e040196fc5d5.png">

Above nodes are to setup following things:
1. Path to LovelaceIcons.map
2. Path to OpenWeatherIcons.map
3. Page Setup up, It is a JSON with Ararry of Arrays.
```
var pages = {
    "LivingRoom" : [
        ["StudyRoom_StudyRoomFan", "lightbulb", "openhab", "switch"],
        ["LivingRoomLight_LivingRoomFan", "ceiling-fan", "openhab", "fan"],
        ["DinningRoomFan_DinningFan", "ceiling-fan", "openhab", "fan"],
        ["TV_Power", "remote-tv", "openhab", "light"],
        ["Master Bedroom.navigate", "bed-king", "subpage", "cardThermo_navigate"]
        ],
"ScreenSaver": 
                [
                ["WeatherandForecast_Current_Icon","lightbulb", "openhab", "icon"],
                ["WeatherandForecast_OutdoorTemperature", "lightbulb", "openhab", "text"],

                ["3Hr", "lightbulb", "subpage", "label"],
               
                ["WeatherandForecast_Icon", "lightbulb", "openhab", "icon"],
                ["WeatherandForecast_ForecastedTemperature", "lightbulb", "openhab", "text"],
               
                
                ["6Hr", "lightbulb", "subpage", "label"],
                ["WeatherandForecast6_Icon", "lightbulb", "openhab", "icon"],
                ["WeatherandForecast_ForecastedTemperature6", "lightbulb", "openhab", "text"],
               
                ["9Hr", "lightbulb", "subpage", "label"],
                ["WeatherandForecast9_Icon", "lightbulb", "openhab", "icon"],
                ["WeatherandForecast_ForecastedTemperature9", "lightbulb", "openhab", "text"],

                ["12Hr", "lightbulb", "subpage", "label"],
                ["WeatherandForecast12_Icon", "lightbulb", "openhab", "icon"],
                
                ["WeatherandForecast_ForecastedTemperature12", "lightbulb", "openhab", "text"],

                ["empty1", "lightbulb", "subpage", "empty"],
                ["empty2", "lightbulb", "subpage", "empty"],

                ["NSPanel_NSPanelSwitch1", "lightbulb", "openhab", "switch"],
                ["NSPanel_NSPanelSwitch2", "lightbulb", "openhab", "switch"],
                
                ["empty3", "lightbulb", "subpage", "empty"],
                ["empty4", "lightbulb", "subpage", "empty"],
                ]

}

```

Example of config 

```
 ["WeatherandForecast_Current_Icon","lightbulb", "openhab", "icon"],
 ```
 
1.  `WeatherandForecast_Current_Icon` = Openhab item name
2.  `lightbulb` = icon name in lovelaceIcon.map
3.  `openhab` = type of config i.e is config for openhab item or normal label.
4.  `switch` = type of the control in lovelace UI. 
 
 
 Note: This is WIP and code fails in many cases. Not all error handling is present. 
 

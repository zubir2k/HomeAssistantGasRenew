<img alt="Home Assistant Gas Renew" src="https://user-images.githubusercontent.com/1905339/198865307-5006de3f-cf6d-4562-850b-fda09e3c8f28.png" width="75%">

![visitors](https://visitor-badge.glitch.me/badge?page_id=zubir2k.homeassistantgasrenew.visitor-badge)
[![Donate](https://img.shields.io/badge/donate-Coffee-yellow.svg)](https://zbrj.ml/buymecoffee)

LPG Gas Monitoring Automation purely based on date comparison. It may not give accurate measures but at least it will provide some estimation when is the gas tank going to be empty and then make neccessary preparations to avoid disruption (thus make wifey happy).

### Features:
1. Dynamic selection of duration (days).
2. Sensor gauge from Full -> Medium -> Low -> Critical
3. Renew button to reset status (upon changing the gas tank of course)

![image](https://user-images.githubusercontent.com/1905339/198865938-03c48285-2ba7-43b7-9aee-f81dceda9e23.png)

![image](https://user-images.githubusercontent.com/1905339/198867810-904da397-5fed-42c1-85cf-b83296648bb6.png)

## Video Tutorial

[![Youtube](https://user-images.githubusercontent.com/1905339/206341098-a6a216bc-e869-44d7-8e07-802e52159215.png)](https://youtu.be/nE4BGvmo7f4)

- Tong Gas Automation menggunakan Home Assistant: https://youtu.be/nE4BGvmo7f4
- Beginners Guide to Home Assistant: https://youtu.be/-jyegp-mL20 

## Installation
1. Simply copy the downloaded source into your Home Assistant `\config`

2. Add the following line into your [configuration.yaml](configuration.yaml) \
(***IMPORTANT***: If you have this line added from another template of mine, you may ignore this step)

```yaml
homeassistant:
  packages: !include_dir_named HAMY/
```

3. Create a dashboard [lovelace-ui.yaml](lovelace-ui.yaml)
- Add new card, scroll at the bottom and choose Manual. 
- Copy & paste the YAML respectively.

![image](https://user-images.githubusercontent.com/1905339/196153827-56e67de2-1591-46aa-9b10-090d5dfb9633.png)

4. Restart Home Assistant to take effect.

### First Time Setup
1. Enter your estimated duration; maximum is 365 days @ 1 year (default is 70 days)
2. Enter your last change date.
3. Enter your previous change date.

### Automation Ideas
1. Integrate with [Google Calendar](https://www.home-assistant.io/integrations/google/) and add reminder to your Google account.
2. Make an order via telegram to your nearest convenience store (if the store supports it).

### Future Development
- Integration with [weight sensors](https://github.com/ishakmuhamad/home-assistant-tong-petronas-weight-scale) to provide more accurate readings by [@ishakmuhamad](https://github.com/ishakmuhamad)\
Reference: [ESPHome-Smart-Scale](https://github.com/markusressel/ESPHome-Smart-Scale)

## Join Us
- [HomeAssistantMalaysia](https://www.facebook.com/groups/homeassistantmalaysia)

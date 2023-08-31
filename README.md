# Irrigation

## Home assistant: Irrigation unlimited and Smart irrigation integration

I'd to share the code I came to in order to automate irrigation of a 13 zones sytem that is made of:
- One lawn watered by a sprinkler
- 12 separate zones watered by drip lines

<p>[Irrigation Unlimited](https://github.com/rgc99/irrigation_unlimited) is managing the control of all valves and the related timings, whilst [HA smart irrigation](https://github.com/jeroenterheerdt/HAsmartirrigation) is used to compute once a day the lawn watering time. As for HA Smart Irrigation, I currently run the production version. I have an in house Davis Vantage VP2 station featuring a solar sensor. Hence, the station delivers directly the evapotraspiration figure, no need to go to internet to get it.</p>



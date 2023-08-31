# Irrigation

## Home assistant: Irrigation unlimited and Smart irrigation integration

I'd to share the code I came to in order to automate irrigation of a 13 zones sytem that is made of:
- One lawn watered by a sprinkler
- 12 separate zones watered by drip lines

<p><a href="https://github.com/rgc99/irrigation_unlimited">Irrigation unlimited</a> is managing the control of all valves and the related timings, whilst <a href="https://github.com/jeroenterheerdt/HAsmartirrigation">HA smart irrigation</a> is used to compute once a day the lawn watering time. As for HA Smart Irrigation, the current production version is used. I have an in house Davis Vantage VP2 station featuring a solar sensor. Hence, the station delivers directly the evapotraspiration value, no need to go to internet to get it.</p>

All zones are adjustments are based on lawn adjustment. A standard watering time is defined for each of them and a percentage is computed from this standard time. Bucket is reset one sequence 1 is finished (huit or night if your prefer).

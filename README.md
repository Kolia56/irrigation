# Irrigation

## Home Assistant - Irrigation unlimited and Smart irrigation integration

I share the code for automating irrigation of a 13 zones sytem that is made of:
- One lawn watered by a sprinkler
- 12 separate zones watered by drip lines

<p><a href="https://github.com/rgc99/irrigation_unlimited">Irrigation unlimited</a> is managing of all valves and the related timings, whilst <a href="https://github.com/jeroenterheerdt/HAsmartirrigation">HA smart irrigation</a> is used to compute once a day the lawn watering time. As for HA Smart Irrigation, the current production version is used. I have an in house Davis Vantage VP2 station featuring a solar sensor. Hence, the station delivers directly the evapotraspiration value, no need to go to internet to get it.</p>

All zones adjustments are based on lawn adjustment (id7 in the code). A standard watering time has been defined by experience for each of them and a percentage is computed from this standard time. Bucket is reset once sequence 1 is finished (nuit or night if your prefer).

input_datetime.watering_s1_start sets sequence 1 start time and can be changed if need arises. Watering time computation is done 2' before and watering time sequence set is done 1 minute before. Please refer to the code to see how it is done.

In Home assistant configuration file this shall be added:
```
homeassistant:
  packages: !include_dir_named packages
```

Interface elements are pretty straightforward and are not included in the repositery. On top of it, <a href="https://github.com/rgc99/irrigation-unlimited-card">Irrigation unlimited companion card</a> is used and turns out to be very compact and effecient.

My deep acknowledgements goes to both <a href="https://github.com/rgc99">rgc99</a> and <a href="[https://github.com/rgc99](https://github.com/jeroenterheerdt)https://github.com/jeroenterheerdt">jeroenterheerdt</a> with a special thanks to rgc99 who help me to sorted out some issues and become more Home Assistant proficient.



| Command | Description | Usage |
| --- | --- | --- |
| screen | Screen width and height of the device | "screen":"1920x1080" |
| stops | Complexity of your curve, suggested 1-2-3 | "stops":"2" |
| duration | Duration of the trajectory | "duration":"2" |
| starting_pos | Starting position | "starting_pos":"20,20" |
| ending_pos | Ending Positions of each stop | "ending_pos":[{"index":"0", "x":"100","y":"100"}, {"index":"1", "x":"200","y":"200"}] |
| snr | SNR | "snr":"100"|
| frequency | Sampling Frequency | "frequency":"100"|


Send request in a json format, example:
> time curl http://server:8000/api -H "Content-Type: application/json" -d '{"stops":"2", "frequency":"60"}'

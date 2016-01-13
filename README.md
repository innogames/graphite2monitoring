# Description

This service is taking metric **m** with timerange from **range1From** untill **range1Until** and compare it with timerange between **range2From** and **range2Until**
If there is increasing more, than **-wi** it will exit with code 1 and if more, than **-ci** - with exit code 2.
Same for decreasing with arguments **-wd** and **-cd**
Also exit message will be percentage of the difference between timeranges.
# Usage
Usage:
- -a string  
        AuthToken to access the graphite-API. For example 'qqq'  
- -ci int  
        Metrics above this threshold will be marked as critical (default 40)
- -wi int
        Metrics above this threshold will be marked as warning (default 20)
- -cd int
        Metrics below this threshold will be marked as critical (default 40)
- -wd int
        Metrics below this threshold will be marked as warning (default 20)
- -m string  
        Name of metric or metric filter e.g. qqqq.test.leoleovich.currentProblems
- -range1From int
    	Amount of seconds ago for the 1st range (from) (default 90000)
- -range1Until int
    	Amount of seconds ago for the 1st range (until) (default 86400)
- -range2From int
    	Amount of seconds ago for the 2st range (from) (default 3600)
- -range2Until int
    	Amount of seconds ago for the 2st range (until)
- -u string
    	User, which has rights to access Graphite (default "graphite")
- -d	Debug mode will print a lot of additinal info

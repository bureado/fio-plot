### fio-plot
Create charts from FIO storage benchmark tool JSON output.
Just take a look at the images below to understand what can be expected.
There are more examples in the 'images' folder.

### 2d chart 
![2d][2d]

### 3d chart
![3d][3d]

### Usage
Requires: numpy, matplotlib

    usage: fio-plot.py [-h] [-i INPUT_DIRECTORY] [-t TITLE] [-s SOURCE] [-L] [-l]
                       [-H] [-D [MAXDEPTH]] [-J [MAXJOBS]] [-n [NUMJOBS]] [-m MAX]
    
    Convert FIO JSON output to charts
    
    optional arguments:
      -h, --help            show this help message and exit
    
    Generic Settings:
      -i INPUT_DIRECTORY, --input-directory INPUT_DIRECTORY
                            input directory where JSON files can be found
      -t TITLE, --title TITLE
                            specifies title to use in charts
      -s SOURCE, --source SOURCE
                            Author
      -L, --latency_iops_3d
                            generate latency + iops 3d
      -l, --latency_iops_2d
                            generate latency + iops 2d graph
      -H, --histogram       generate latency histogram per queue depth
      -D [MAXDEPTH], --maxdepth [MAXDEPTH]
                            maximum queue depth to graph
      -J [MAXJOBS], --maxjobs [MAXJOBS]
                            maximum numjobs to graph in 3d graph
      -n [NUMJOBS], --numjobs [NUMJOBS]
                            specifies for which numjob parameter you want the 2d
                            graphs to be generated
      -m MAX, --max MAX     optional max value for z-axis

### Caveat

I've made this tool on Mac OS, using brew. I have yet to test this on (a headless) Linux.
Also, the code may leave a lot to be desired, I'm aware of that.


[2d]: https://raw.githubusercontent.com/louwrentius/fio-plot/master/images/HPMICROSERVERG8/SATA300/SAMSUNG680PRO/randread_iodepth_2019-08-25-21%3A58%3A58_1_iops_latency.png
[3d]: https://raw.githubusercontent.com/louwrentius/fio-plot/master/images/HPMICROSERVERG8/SATA300/SAMSUNG680PRO/3d-iops-jobsRandom%20Read-2019-08-25-21%3A58%3A56.png

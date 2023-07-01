In this script:

Main disk drive and RAM memory information.

Active Services.

Internet speed test [Speedtest CLI].

Congestion information.
 

The measure_latency function uses the subprocess module to run the ping command and extract latency from the output. The solve_network_congestion function continuously measures latency by calling measure_latency at regular intervals defined by check_interval.

If the measured latency exceeds the target latency, you can add your workaround code to take appropriate actions to resolve the congestion. You may need to use additional tools or libraries depending on your specific requirements.

You can customize the target_latency and check_interval parameters according to your needs. Remember to run the script with root privileges (sudo python script.py) as the ping command requires administrative access to create ICMP packets.


How to use:

1 step:

Install the curl package if it is not already installed on your system. curl is required to download the Speedtest CLI. Run the command below to install curl:

sudo apt install curl

2- Step:

curl -s https://install.speedtest.net/app/cli/install.deb.sh | sudo bash

3- To run the Speedtest, use the following command:

speed test

4- Make a git clone of the softping repo and give the following permission to the softping python script.

chmod a+x softping.py

5- Run softping.py and let it work on your network.

python3 softping.py

6- The script will ask for your name and then it will inform you via the terminal the most important information about your main disk drive, active services on your machine, test your internet speed and finally it will seek to identify congestion on your network in order to reduce latencies optimizing performance.






Thank you for your choice, I hope I have collaborated.
By Morgan Bin Bash / 2023

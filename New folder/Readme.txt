chao cac ban, day la project cua toi!

3.1 Kill the SpringBoot App
If your springboot jar file name is myapp-exec.jar, kill it as this:

kill $(ps aux | grep 'myapp-exec.jar' | grep -v grep | awk '{print $2}')
Save the above script as stop.sh

3.2 Start the SpringBoot App in background
To start the app in background, you can use the nohup commmand:

nohup java -jar myapp-exec.jar > nohup.out &
Save the above script as start.sh

3.2 Restart the SpringBoot App
Now you can open an editor to create a file named restart.sh to do the restart job:

echo 'stop the app...'
./stop.sh
echo 'stopped'
sleep 2
echo 'start the app...'
./run.sh
echo 'started'
Save the above script as restart.sh

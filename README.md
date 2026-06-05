# Create a new file called disk_monitor.sh and paste the following code into it:

# How to Set It Up

# 1. Make the script executable
# You need to grant the script permission to run. Run this command in your terminal:
chmod +x disk_monitor.sh

# 2. Test it manually
# Run the script to ensure it executes without errors. If your disks are below the threshold, it won't output anything. To force a test, temporarily change the THRESHOLD variable in the script to something very low (like 10).
./disk_monitor.sh

# 3. Automate it with Cron
# You don't want to run this manually every day. You can use a cron job to have the server run it automatically at a set interval.
# Open your crontab editor:
crontab -e
# Add this line at the bottom to run the check every hour:
0 * * * * /path/to/your/disk_monitor.sh

---
Created: 2024-07-27T14:00:15+05:30
Updated: 2024-07-27T14:00:38+05:30
Maintainer: Ibrar Ansari
---
# Monitor all processes
```
pm2 monit
```
# Fork mode
```
pm2 start app.js --name my-api	# Start and name a process
```
# Cluster mode
```
pm2 start app.js -i 0	# Will start maximum processes with LB depending on available CPUs
```
# Listing
```
pm2 list	#Display all processes status
pm2 jlist	#Print process list in raw JSON
pm2 prettylist	#Print process list in beautified JSON
pm2 describe 0	#Display all information about a specific process
```
# Logs
```
pm2 logs [--raw]	#Display all processes logs in streaming
pm2 flush	#Empty all log files
pm2 reloadLogs	#Reload all logs
```
# Actions
```
pm2 stop all	Stop all processes
pm2 restart all	Restart all processes
pm2 reload all	Will 0s downtime reload (for NETWORKED apps)
pm2 stop 0	Stop specific process id
pm2 restart 0	Restart specific process id
pm2 delete 0	Will remove process from pm2 list
pm2 delete all	Will remove all processes from pm2 list
pm2 save	Save processes list to respawn at reboot
pm2 reset	reset the restart counter
pm2 reset all	reset all restart counters
```
# Misc
```
pm2 reset <process>	Reset meta data (restarted time…)
pm2 updatePM2	Update in memory pm2
pm2 ping	Ensure pm2 daemon has been launched
pm2 sendSignal SIGUSR2 my-app	Send system signal to script
pm2 start app.js --no-daemon	Run pm2 daemon in the foreground if it doesn’t exist already
pm2 start app.js --no-vizion	Skip vizion features (versioning control)
pm2 start app.js --no-autorestart	Do not automatically restart app
```
Different ways to launch a process
```
pm2 start app.js           # Start app.js
pm2 start app.js -- -a 23  # Pass arguments '-a 23' argument to app.js script
pm2 start app.js --name serverone # Start a process an name it as server one you can now stop the process by doing pm2 stop serverone
pm2 start app.js --node-args="--debug=7001" # --node-args to pass options to node V8
pm2 start app.js -i max    # Start maximum processes depending on available CPUs (cluster mode)
pm2 start app.js --log-date-format "YYYY-MM-DD HH:mm Z"    # Log will be prefixed with custom time format
pm2 start app.json                # Start processes with options declared in app.json
                                    # Go to chapter Multi process JSON declaration for more
pm2 start app.js -e err.log -o out.log  # Start and specify error and out log
pm2 --run-as-user foo start app.js  # Start app.js as user foo instead of the user that started pm2
pm2 --run-as-user foo --run-as-group bar start app.js  # Start app.js as foo:bar instead of the user:group that started pm2
```

### 💼 Connect with me 👇👇 😊

- 🔥 [**Youtube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
- ✍ [**Blog**](https://ibraransari.blogspot.com/)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
- 👨‍💻 [**Github**](https://github.com/meibraransari?tab=repositories)
- 💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
- 🐳 [**Docker**](https://hub.docker.com/u/ibraransaridocker)

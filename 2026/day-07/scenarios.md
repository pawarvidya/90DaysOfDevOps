# Scenario Questions 
# Scenario 1 : Service Not Starting
  A web application service called 'myapp' failed to start after a server reboot.
What commands would you run to diagnose the issue?
Write at least 4 commands in order.
- Step 1 : Check service status
   Command : systemctl status myapp
   Why : See  if the service is active, failed, or stopped.
- Step 2 : Check service logs
  Command: journalctl -u myapp -n 50
  Why : View the last 50 log entries to find error messages.
- Step 3: Check if service starts automatically on boot
  Command: sysyemctl is -enabled myapp
  Why: Verify whether the service is configured to start after reboot.
- Step 4: Check recent boot logs for the service
  Command: journalctl -u myapp -b
  Why: See what happened during the current boot.
- Step 5: Try starting the service manually
  Command: sudo systemctl start myapp
  Why : heck whether it starts successfully or throws an error.
  

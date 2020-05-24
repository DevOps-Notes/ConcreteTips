# ConcreteTips

* Some tips for daily work, eg, Find and close the port occupancy program:

  ```po
  # Get PID
  PS C:\Users\luo.wei> netstat -ano | findstr 8080
  TCP    0.0.0.0:8080           0.0.0.0:0              LISTENING       7880
  
  # Get Program
  PS C:\Users\luo.wei> tasklist|findstr "7880"
  javaw.exe                     7880 Console                    1    232,068 K
  
  # Kill Program
  PS C:\Users\luo.wei> taskkill /T /F /PID 7880
  SUCCESS: The process with PID 7880 (child process of PID 10524) has been terminated.
  ```

  
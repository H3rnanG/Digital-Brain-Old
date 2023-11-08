#Personal 

# Cerrar un puerto:
```cmd
netstat -ano | findstr :(puerto)
```
y luego:
```cmd
taskkill -PID <PID> -F
```

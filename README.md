## Boss Ping Remover
Hace que los ataques de los jefes coincidan con los servidores.

### Comando(s): 
* `BPR` -- Habilitar / Deshabilitar el módulo

* `BPR debug` -- Habilitar / Deshabilitar la salida de depuración

### Config:

Realice los siguientes cambios en `config/config.json` si se cumple **_alguna_** de las siguientes condiciones:

* Si tiene un ping alto (más de 200 ms) 

* Si está utilizando skill prediction (o ping compensation, ping remover, class script, etc)

```diff
{
    "version": "6.0",
    "enabled": true,
    "debug": false,
    "pingHistoryMax": 30,
-   "pingSpikesLimit": false,
+   "pingSpikesLimit": true,
-   "pingSpikesMin": 100,
+   "pingSpikesMin": X, (X = (su ping mínimo) - 10 o 20)
-   "pingSpikesMax": 1000,
+   "pingSpikesMax": Y, (Y = (su ping normal x 2) + 20 o 40)
    "minCombatFPS": 30
}
```
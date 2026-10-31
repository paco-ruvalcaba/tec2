| Tiempo | Evento | Estado de Máquina A | Estado de Máquina B | Cola 1 | Cola 2 |
| --- | --- | --- | --- | --- | --- |
| **00:00** | Llega **Silla 1** | Entra a **Máquina A** | Desocupada | 0 | 0 |
| **00:08** | **Silla 1** sale de A y pasa a B | Desocupada | Entra a **Máquina B** | 0 | 0 |
| **00:10** | Llega **Silla 2** | Entra a **Máquina A** | Procesando **Silla 1** | 0 | 0 |
| **00:18** | **Silla 2** sale de A | Desocupada | Procesando **Silla 1** (termina al min 23) | 0 | **1 (Silla 2)** |
| **00:20** | Llega **Silla 3** | Entra a **Máquina A** | Procesando **Silla 1** | 0 | **1 (Silla 2)** |
| **00:23** | **Silla 1** sale terminada | Procesando **Silla 3** | Entra **Silla 2** a **Máquina B** | 0 | 0 |
| **00:28** | **Silla 3** sale de A | Desocupada | Procesando **Silla 2** (termina al min 38) | 0 | **1 (Silla 3)** |
| **00:30** | Llega **Silla 4** | Entra a **Máquina A** | Procesando **Silla 2** | 0 | **1 (Silla 3)** |

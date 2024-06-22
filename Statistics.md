## Damage Formula
```
(
  (
    (
	   + (Base Damage + "Buff" Weapon Damage) * Combo Bonus * Impact Zone Bonus
        + Gear "+N Weapon Damage"|"N Magical Damage"
        + Divine Strike Damage
    )
    * (1 + Power Bonus)
    + "Additional" Damage
  )
  * (Hit Location Multiplier)
  * (1 - Damage Reduction * (1 - Penetration))
  * (1 - Projectile Reduction)
)
* Projectile Falloff
+ True Damage
```
#### Esemplificazione
- Base damage: danno base del arma o magia
- "Buff" Weapon Damage: buff da skill e solo skill
- [[Fighter | Combo Bonus]]
- [[Fighter | Impact Zone]]
- Gear Damage: danno bonus
	- dato da + weapon bonus per le armi melee
	- per le armi magiche si aggiunge il magical damage
- Power Bonus
	- Definito dal [[physical]]/[[magical]] power bonus

Queste statistiche guadagnano dal power bonus e possono essere soggette a riduzioni

- additional damage: meglio true damage
- true damage: danno flat senza nessun debuff o buff
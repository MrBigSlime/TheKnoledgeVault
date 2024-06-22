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
>[!column | list no-i no-t]
> - __Base damage__: __danno base__ del arma o magia
> - "Buff" __Weapon Damage__: __buff da skill__ e solo skill
> - __[[Fighter | Combo Bonus]]__
> - __[[Fighter | Impact Zone]]__
> - __Gear Damage__: danno bonus
>	- dato da + weapon bonus per le armi melee
>	- per le armi magiche si aggiunge il magical damage
> - Divine Strike: roba da chierici
> - __Power Bonus__
>	- Definito dal __[[Statistics#^fdd568|physical]]/[[Statistics#^9452d6|magical]] power bonus__

Queste statistiche guadagnano dal power bonus e possono essere soggette a riduzioni
>[!column | list no-i no-t]
> - __Additional damage__: meglio true damage, danno in più non scala con power damage e viene diminuito con la riduzione del danno
> - __True damage__: danno flat senza nessun debuff o buff
> - __Hit Location Multiplier__: in base alla parte della colpita il danno verrà modificato di una percentuale
> 	- Head: 150%
> 	- Body: 100%
> 	- Arms: 80%
> 	- Legs: 60%
> 	- Feet/Hand: 50%
> - __Penetration__: fa quello che ti aspetti


## Statistics
Lo scaling delle statistiche varia in base al intervallo, quindi si hanno diminishing returns
>[!danger|no-i]- esempio 
> ![[Pasted image 20240622153844.png|wm-sm]]

>[!column|no-i no-t]
>>[!note|no-i] Strength
>>Governa il physical power bonus, [[Statistics#^a90e40|max health]]
>> - 30 str -> 18% phys. power
>> - 40 str -> 25% phys. power ^fdd568
>
>>[!tip|no-i] Vigor
>> Governa il recupero vita e [[Statistics#^a90e40|max health]]
>> - 30 vig -> 100% (doppio della rigenerazione normale)
>
>>[!example|no-i] Agility
>>Governa la velocità di movimento, [[Statistics#^b0e358|Action speed]], [[Statistics#^0ef567|Regular Interaction speed]], 
>> - 15 agi -> 0 bonus
>> - 30 agi -> 10 bonus (rallentamento di uno spellbook)
>
>>[!abstact|no-i] Dexterity
>>Governa [[Statistics#^b0e358|Action speed]], manual dexterity, item equip speed
>> - 15 dex -> 0 bonus item equip e manual dexterity
>> - 30 dex -> 80% bonus item equip e 40% bonus manual dex
>> - 40 dex -> 110% bonus item equip e 48% bonus manual dex


> __Manual dexterity__
> velocità di un bardo di suonare gli strumenti

>[!column|no-i no-t]
>>[!warning|no-i] Will
>> Governa il magical power bonus anche le cure magiche, resistenza magica, buff duration
>> - 15 will 0 power bonus e buff duration, 3% magical damage reduction
>> - 40 will 53% power bonus, 35% buff duration, 30% magical damage reduction
>
>>[!check|no-i] Knowledge
>>Governa la velocità di casting, la memory capacity memory recovery
>> - 15 knw -> 0 bonus casting speed, 60% recovery
>> - 35 knw -> 50% bonus casting speed, 120% recovery
>> - 45 knw -> 75% bouns casting speed, 135% recovery
>> Memory capacity = Knowledge 
>> - 10 knw -> 10 mem capacity
>
>>[!note|no-i] Resourcefulness
>>Governa il Cooldown reduction delle abilità,la durata dei buff del bardo(persuasiveness) e [[Statistics#^0ef567|Regular Interaction speed]]
>> - 15 res -> 0 bonus cooldown reduction, 15 persuasiveness
>> - 40 res ->30% bonus cooldown reduction, 37,5 persuasiveness

^9452d6

> Memory recovery
> velocità di recupero spell mentre si riposta/medita

> Nota: buff duration è stimata per gli effetti positivi
> lo scaling per i negativi ve lo andate a guardare vuoi

> Nota: durata dei buff del bardo dipende da persuasiveness e dalla buff duration

## Hybrid Statistics
>[!danger|no-i] Max health
> Forza 25% e Vigore 75%
> __Strength \* 0.25 + Vigor \* 0.75__

^a90e40

>[!success|no-i] Action Speed
> Agility 25% e Dexterity 75%
> __Agility \* 0.25 + Dexterity \* 0.75__
> interact with your weapons, meaning stowing, swapping, reloading or attacking with weapons, as well as the speed of usage of consumables.
> Velocizza le animazioni

^b0e358

>[!note|no-i] Regular Interaction Speed
> Agility 40% e Resourcefulness 60%
>__Agility \* 0.4 + Resourcefulness \* 0.6__
> Velocizza l'interazione con gli oggetti del dungeon (porte, leve, etc...)

^0ef567

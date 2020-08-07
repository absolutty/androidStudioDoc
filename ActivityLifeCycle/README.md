# Activity LifeCycle
https://developer.android.com/guide/components/activities/activity-lifecycle <br>
![alt desc](https://developer.android.com/guide/components/images/activity_lifecycle.png) <br>
- **onCreate()**: tento callback **musí** byť implementovaný, pretože je spustený pri tom ako systém vytvára aktivitu.
Počas tohto vytvárania, aktivita zostane vo *created state*. Táto metóda počas ktorej sa robia
základné úkony na spustenie aplikácie by mala byť zavolaná iba **raz** počas celého života aktivity. <br>
Počas tohto cyklu sa môže diať:
  - bind dát do listu
  - oboznámenie aktivity s ViewModel-om
  - inicializovanie class-scope premenných
- **onStart()**:  keď je tento callback zavolaný, aktivita vstupuje do *started state*. Táto metóda
spraví aktivitu viditeľnu pre užívateľa počas toho ako sa aktivita pripravuje vstúpiť do popredia 
a začať byť interaktívna. 
- **onResume()**: keď je tento callback zavolaný, aktivita vstupuje do *resumed state*. 
Aktivita vstupuje do popredia a je schopná interagovať s užívateľom. V tomto stave aktivita zostáva pokým 
sa nestane niečo, čo preruší aplikáciu. 
Napríklad:
  - prichádzajúci telefonát
  - užívateľ prechádza do inej aktivity
  - obrazovka zariadenia sa vypne

- **onPause()**: tento callback je zavolaný počas prvého náznaku že užívateľ opúšťa aktivitu
(aj keď to neznamená vždy že aktivita musí byť zničená). Znamená to že aktivita nie je naďalej v popredí
(môže byť viditeľná v multi-window režime). Aktivita vstupuje do *paused state*.
- **onStop()**: tento callback je zavolaný keď aktivita nie je naďalej viditeľná používateľovi, aktivita
vstupuje do *stopped state*. Nastane to vtedy ak nová aktivita prekryje celú obrazovku. alebo aplikácia sa 
začína vypínať. Vstupuje do *stopped state*. 
- **onDestroy()**: tento callback je zavolaný počas toho ako je aplikácia zničená. <br>
Systém ho môže invokovať počas:
  -aktivita sa vypína(užívateľ vypína opúšťa aktivitu) alebo je *finish()* je zavolaný v aktivity
  - systém dočasne ničí aktivitu kvôli zmene konfigurácie (otočenie zariadenia, multi-window režim)

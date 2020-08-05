# Activity
https://developer.android.com/reference/android/app/Activity <br>
Takmer všetky aktivity komunikujú s užívateľom, Activity trieda sa zaoberá vytváraním a zobrazovaním
UI pomocou *setContentView(View)*. Aktivity sú väčšinou prezentované ako full-screen okná, nemusí
to byť vždy tak. Môžu byť zobrazené aj ako **floating window**, **multi-window mode** alebo zapustené
do ostatných okien. Tieto dve metódy bývajú vždy implementované: 
- **onCreate(Bundle)**: väčšinou obsahuje *setContentView(int)* s layoutom ktorý definuje UI a metódy
*findViewById(id)* ktoré nájdu widgety v tom danom UI a umožňujú programovú interakciu s nimi. 
- **onPause()**: tu sú definované úkony počas pozastavanie aktivity. Hocijaké zmeny spravené používateľom
by maôo byť zachované (väčšinou pomocou ContentProvider-a)

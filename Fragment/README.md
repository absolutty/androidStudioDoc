# Fragment
https://developer.android.com/guide/components/fragments <br>
Reprezentuje správanie časti UI v *FragmentActivity*. Je možné skombinovať viacero fragmentov 
v jednej aktivite na vytvorenie multi-pane UI. Fragment by mal byť dizajnovaný univerzálne --> je ho 
možné použiť na niekoľkých aktivitách. <br>
Fragment je *modulárna* sekcia aktivity, má svoj vlastný lifecycle, dostáva vlastné input eventy, ktoré 
môžu byť pridané a odstránené. Vždy musí byť súčasťou aktivitay, pretože jeho lifecycle je priamo
ovplyvnený jeho host-activity lifecycle-om. Napr. keď je aktivita *paused* tak sú aj všetky fragmenty 
v nej a keď je aktivita *destroyed* tak sú aj všetky fragmenty v nej. Ale keď je aktivita *resumed*
(spustená) je možné manipolovať každý fragment nezávisle od jeho host-activity a od ostatných fragmentov. <br>
Počas toho ako je uskutočňovaná activity *transaction* je možné pridať fragment do *back stack*, ktorá je 
spravovaná aktivitov. Umožňuje užívateľovi zvrátiť fragment transaction ktorá bola vykonaná, napr. pomocou
*back button*

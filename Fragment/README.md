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
Počas toho ako je uskutočňovaná activity *transaction* je možné pridať fragment do *back stack*, ktorá je spravovaná aktivitov. Umožňuje užívateľovi zvrátiť fragment transaction ktorá bola vykonaná, napr. pomocou *back button*. <br>
**Zobrazovanie fragmentu**: <br>
Pre vytvorenie fragmentu je potrebné aby trieda obsahujúca fragment bola sub-classov k triede *Fragment*. Pre pridanie layoutu je potrebné implementovať metódu *onCreateView()*, ktorá je zavolaná
počas toho ako fragment vykresluje svoj layout. Táto metóda vracia *view*, ktorý je základom fragmentu.
Na vrátenie layoutu je možné ho *inflatnuť* z layout zdroju definovaného v XML. Metóda onCreateView() pre tento účel poskytuje objekt *LayoutInflater*. <br> 
Metóda *inflate* má tri argumenty:
- ID layoutu ktorý chceme inflatnuť
- ViewGroup do ktorého bude layout inflatnutý.
- boolean indikujúci že či inflated layout má byť pripnutý k ViewGroup počas inflation. 
```java
public static class ExampleFragment extends Fragment {
    @Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container,
                             Bundle savedInstanceState) {
        // Inflate the layout for this fragment
        return inflater.inflate(R.layout.example_fragment, container, false);
    }
}
```
*container* paremeter v metóde je parent v ktorom je fragment layout vložený. <br>
*savedInstanceState* parameter je Bundle ktorý poskytuje dáta o predchádzajúcom state-u fragmentu. <br>

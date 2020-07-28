# Dimension
https://developer.android.com/guide/topics/resources/more-resources#Dimension <br>
Veľkosť view-ov je špecifikovaná *číslom* a *jednotkou*. <br>
**Jednotky podporované v AndroidStudiu:**
- **dp** (Density-independent Pixels): abstraktná jednotka ktorá je založená na fyzickej veľkosti obrazovky.
Ak je view zobrazený na väčšej obrazovke, počet pixelov použitých na vykreslenie 1dp sa zväčší. 
Takisto aj v opačnom prípade, ak je obrazovka menšia. Pomer dp-a-pixel sa zmení z veľkosťou obrazovky ale
nemusí sa v priamom pomere. Použitie dp jednotiek je jednoduché riešenie tvorby responzívneho layoutu.
- **sp** (Scale-independent Pixels): odporúčané pre veľkosť fontov. Podobné ako dp, prispôsobená veľkosť 
aj podľa používateľových preferencií.
- **pt** (Points): 1/72 z veľkosti palca (inch) založené na fyzickej veľkosti zariadenia. Počíta s tým
že veľkosť obrazovky je 72dpi. 
- **px** (Pixels): aktuálne pixely obrazovky. Použitie tejto jednotky sa neodporúča, lebo počet pixelov
obrazovky sa na jednotlivých zariadeniach líši. 
- **mm** (Millimeters): založené na fyzickej veľkosti obrazovky v milimetroch. 
- **in** (Inches): založené na fyzickej veľkosti obrazovky v palcoch.

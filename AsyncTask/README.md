# ASyncTask
https://www.tutorialspoint.com/android-asynctask-example-and-explanation <br>
Vykonáva operácie na *background thread*  a updatuje *main thread*. Umožňuje komunikáciu medzi tymito dvomi Threadmi. <br>
**Metódy**:
- **onPreExecute()**: pred vykonaním *background operácie* je vhodné používateľovi zobraziť na obrazovke niečo ako progressbar alebo
nejakú animáciu.
- **doInBackground(Params)**: v tejto metóde sa vykonávajú operácie pre background thread. Operácie v tejto metóde by nemali nič spoločné s tým čo robí main thread. 
- **onProgressUpdate(Progress…)**: pokiaľ chceme počas vykonávania operácie updatnuť nejakú informíciu v UI. 
- **onPostExecute(Result)**: v tejto metóde je možné updatnuť UI na základe výsledku operácie. 

**Async Task obsahuje tieto Generic Types**:
- **TypeOfVarArgParams**: obsahuje informácie o druhu parametra ktorý sa používa.
- **ProgressValue**: obsahuje informácie o progresových jednotkách. Pokiaľ vykonáva background operáciu
je možné updatnuť UI použitím onProgressUpdate().
- **ResultValue**: obsahuje informácie o typu výsledku. 

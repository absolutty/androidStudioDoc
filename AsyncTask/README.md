# ASyncTask
Vykonáva operácie na *background thread*  a updatuje *main thread*. Umožňuje komunikáciu medzi tymito dvomi
Threadmi. <br>
**Metódy:**
- **onPreExecute()**: pred vykonaním *background operácie* je vhodné používateľovi zobraziť na obrazovke niečo ako progressbar alebo
nejakú animáciu.
- **doInBackground(Params)**: v tejto metóde sa vykonávajú operácie pre background thread. Operácie v tejto metóde
by sa nemali dotýkať ničoho čo robí main thread. 
- **onProgressUpdate(Progress…)**: pokiaľ chceme počas vykonávania operácie updatnuť nejakú informíciu v UI. 
- **onPostExecute(Result)**: v tejto metóde je možné updatnuť UI na základe výsledku operácie. 

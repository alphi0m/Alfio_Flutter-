# EMAD - Task 1: Primo Progetto Flutter & Deploy iOS

**Studente:** Alfio Marra  
**Corso:** Enterprise Mobile Application Development (EMAD)  
**Progetto:** Flutter Counter App & Physical Device Deployment  

---

## 📱 Panoramica del Progetto

Questo repository contiene il primo elaborato pratico per il corso di **Enterprise Mobile Application Development (EMAD)**.
L'obiettivo del task consiste nella configurazione dell'ambiente di sviluppo Flutter/Dart, nella personalizzazione della prima applicazione e nel completamento dell'intero flusso di compilazione ed esecuzione su dispositivo fisico **Apple iPhone**.

---

## ✨ Funzionalità e Personalizzazioni

L'applicazione si basa sul template interattivo *Stateful* di Flutter con le seguenti modifiche e configurazioni dedicate:

- **Identificativo Utente & Titolo:** L'app bar e il titolo dell'applicazione (`MyHomePage`) sono personalizzati a nome dello studente (**Alfio Marra**).
- **Theme & ColorScheme:** Personalizzazione del tema visivo Material 3 mediante un seed color verde bosco scuro (`Color.fromARGB(255, 13, 77, 55)`), che rigenera dinamicamente la palette cromatica dell'interfaccia (AppBar, accenti e FloatingActionButton).
- **Gestione dello Stato:** Gestione del contatore reattivo tramite `StatefulWidget` e invocazione di `setState()` per l'aggiornamento dinamico della UI al tocco del pulsante floating.

---

## ⚙️ Configurazione & Deploy su Dispositivo Fisico (iPhone)

Il progetto è stato configurato per la compilazione e l'installazione nativa su dispositivo **iOS fisico**:

1. **Configurazione Xcode & Bundle Identifier:**
   - Aggiornato il Bundle ID univoco in `com.alfio.flutter01`.
   - Assegnato il Development Team per il signing (`BC9GE2XGD4`).
   - Generato e associato il provisioning profile di sviluppo personale.

2. **Autorizzazione Profilo iOS:**
   - Sul dispositivo, abilitata la modalità sviluppatore (*Impostazioni > Privacy e sicurezza > Modalità sviluppatore*).
   - Autorizzato il certificato dello sviluppatore (*Impostazioni > Generali > Gestione VPN e dispositivi*).

3. **Compilazione Release:**
   - L'applicazione è stata eseguita in modalità standalone **Release**, garantendo l'esecuzione fluida e indipendente senza vincoli di debug attach (LLDB):
     ```bash
     flutter run -d <DEVICE_ID> --release
     ```

---
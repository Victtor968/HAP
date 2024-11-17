<!DOCTYPE html>
<html lang="it">
<body>
    <h1>Descrizione Generica della Pagina Web</h1>
    <p>
        Questa pagina web, intitolata <strong>“HAP”</strong>, è progettata per calcolare e visualizzare:
    </p>
    <h2>1. Giorni rimanenti alla pensione:</h2>
    <ul>
        <li>Determinati dalla data di pensionamento inserita dall'utente.</li>
        <li>Mostrati dinamicamente nella sezione <em>"Giorni alla pensione"</em>.</li>
    </ul>
    <h2>2. Giorni lavorativi rimanenti:</h2>
    <ul>
        <li>
            Calcolati escludendo sabati, domeniche e festività italiane, in base alla data di pensionamento 
            e a eventuali ferie e permessi specificati dall'utente.
        </li>
        <li>Visualizzati nella sezione <em>"Giorni lavorativi rimanenti"</em>.</li>
    </ul>
    <h2>3. Interazione dinamica:</h2>
    <ul>
        <li>Permette all'utente di salvare la data di pensionamento, i giorni di ferie e le ore di permesso utilizzando i cookie.</li>
        <li>I calcoli vengono aggiornati automaticamente in base ai dati immessi dall'utente.</li>
    </ul>
    <h2>4. Integrazione con Home Assistant:</h2>
    <ul>
        <li>
            I valori di <em>"Giorni alla pensione"</em> e <em>"Giorni lavorativi rimanenti"</em> vengono inviati automaticamente a Home Assistant tramite WebSocket, 
            aggiornando le entità <code>input_number.days</code> e <code>input_number.workday_count</code>.
        </li>
    </ul>
    <h1>Istruzioni per Farla Interagire con Home Assistant</h1>
    <h2>1. Requisiti Prerequisiti:</h2>
    <ul>
        <li>Una configurazione attiva di Home Assistant.</li>
        <li>La chiave di autorizzazione (access token) valida per l'accesso ai WebSocket API di Home Assistant.</li>
        <li>Due entità di tipo <code>input_number</code> configurate in Home Assistant:</li>
    </ul>
    <pre>
input_number:
  days:
    name: Giorni alla pensione
    min: 0
    max: 10000
    step: 1
  workday_count:
    name: Giorni lavorativi rimanenti
    min: 0
    max: 10000
    step: 1
    </pre>
    <p>Riavvia Home Assistant dopo aver aggiunto queste entità.</p>
</body>
</html>

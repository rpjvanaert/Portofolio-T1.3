# Portofolio Ralf van Aert
**TI1.3 FP Individueel Resultaat**
> TI1.3 IPR Ralf van Aert\
Studentennummer: 2163995\
E-mail: <rpj.vanaert@student.avans.nl>


#### Delete this, to-do list:
- Wekelijkse reflectie van eigen bijdrage
    - Les week 2 t/m 9
- Wekelijkse vakinhoudelijke reflectie
    - Minstens 4 waarvan 1 voor ontwerpfase
- Reflectie op stellingen
    - Minstens 1 reflectie op onderzoeksmethodiek
        - Hoe je te werk bent gegaan. Inclusief conclusie en bronvermeldingen
- Lijst met applicatie die gebruik maken van JSON
#### Delete this, to do list: ^


## Inhoudsopgave
<div id="TOC">
<ul>
    <li>
    <h3>
        <a href="#intro"> Inleiding </a>
    </h3>
    </li>
    <li>
    <h3>
        <a href="#weekly"> Weekelijkse Reflectie</a>
    </h3>
    </li>
        <ul>
            <li>
                <a href="#week2">Week 2</a>  
            </li>
            <li>
                <a href="#week3">Week 3</a>  
            </li>
            <li>
                <a href="#week4">Week 4</a>  
            </li>
            <li>
                <a href="#week5">Week 5</a>  
            </li>
            <li>
                <a href="#week6">Week 6</a>  
            </li>
            <li>
                <a href="#week7">Week 7</a>  
            </li>
            <li>
                <a href="#week8">Week 8</a>  
            </li>
            <li>
                <a href="#week9">Week 9</a>  
            </li>
        </ul>
    <li>
    <h3>
        <a href="#onderzoeksMethodiek"> Reflectie Onderzoeksmethodiek </a>
    </h3>
    </li>
</ul>
</div>

---

<div id="intro">
    <h2>
        <a href="TOC"> Inleiding</a>
    </h2>
<div>

<div id="weekly">
    <h2>
        <a href="TOC">Wekelijkse Reflectie</a>
    </h2>
</div>
Inleiding weekelijkse reflectie

<div id="week2">
    <h2>
        <a href="TOC">Week 2</a>
    </h2>
</div>

#### **Reflectie eigen bijdrage**
Bij het verdelen van de rollen is codebeheerder aan mij gegeven, dit is vooral omdat ik nog niet goed met GIT/GIT-Kraken om kan gaan. Op deze manier en met de hulp van mijn groepsleden, hoop ik GIT te leren begrijpen.

Ook hebben we een Plan van Aanpak gemaakt, daarbij heb ik het achtergrond gemaakt en gegevens/opmaak mede-geregeld. Naast dat heb ik ook de Java-Style-Guide opgezet en samen met de rest overlegd over het samenwerkings contract.

Tot slot heb ik de repository opgezet bij GIT-hub, met wat hulp van andere. Ik heb veel problemen gehad met GIT op het begin, maar alles is uiteindelijk verholpen. Ik heb aan de Visual-tab als paar, waarbij ik meedacht. Visual-tab is niet volledig modulair, maar simpel en elegant genoeg om de benodigde variabele snel aan te passen. De visual-tab modulairder te maken is dus ook een toekomstige verbetering die eventueel zou kunnen gebeuren.

<img src="visualTabExample1.png" alt="Visual Tab Progress" width="400"/>

#### **Reflectie technische & vakinhoudelijke bijdrage**
Er zijn in de tweede week veel kleine, maar grondige besluiten genomen. Hiervan ga ik er een paar beschrijven waaraan ik heb mee gedacht met beredenering.

We waren al van plan elke artiest en show een genre te geven, maar we hadden niks gedetaileerd afgesproken. We hadden al besloten om redelijk veel genres te nemen als enumerator. Nu moesten alleen nog bepalen of we hiervan een apart java bestand van maken. Daar hebben we voor gekozen, omdat deze enumerator door verschillende klasses gebruikt gaat worden. Ook zorgt dit voor meer duidelijkheid in de code.

---

<div id="week3">
    <h2>
        <a href="TOC">Week 3</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**
<img src="schedule-Week3-1.png" alt="Schedule Tab Progress" width="400"/>
<img src="schedule-Week3-2.png" alt="Schedule Tab Progress" width="400"/>
<img src="schedule-Week3-3.png" alt="Schedule Tab Progress" width="400"/>

Deze week heb ik aan het begin veel meegedacht aan de problemen van schedule tab,
maar naast dat veel testen en kleine features verfijnen en maken. Ik heb ook gewerkt aan de artiesten afbeelding keuze optie, maar dit is niet door gegaan.
Dit kwam doordat, beide javax.json en google.gson de afbeeldingen niet wilde opslaan.

<img src="schedule-Week3-4.png" alt="Schedule Tab Progress" width="400"/>

Naast dat heb ik de (mijn mening vreselijke) paarse kleurpallet aangepast naar lichtblauw en grijs, dit ziet er veel rustiger uit. Ook heb ik de window groter gemaakt met de daar nodige aanpassingen aan schedule tab en visual tab. De show en artiesten beschrijving weergave (die weergeeft de geselecteerde show met bijhorende artiest(en)) was het mogelijk om horizontaal te scrollen, dit is eruit gehaald inclusief andere verhoudingen tussen de TextArea's.

Ik heb de show beschrijving van een TextArea omgezet naar een TextFlow. De bijhorende code;

 ```java     
    VBox descriptionBase = new VBox();
    descriptionBase.getChildren().add(new Label("Show:"));
    TextFlow showDescriptionTextFlow = new TextFlow();

    Text textTitle = new Text(this.selectedItem.getName());
    textTitle.setStyle("-fx-font-weight: bold; -fx-font-size: 40");

    Text textDescrTitle = new Text("\n\n Show Description:");
    textDescrTitle.setStyle("-fx-font-weight: bold;");

    Text textDescription = new Text("\n" + this.selectedItem.getDescription());
    showDescriptionTextFlow.getChildren().addAll(textTitle, textDescrTitle, textDescription);
    showDescriptionTextFlow.setMaxWidth(450);
```


Zoals je in de code kan zien, stop ik Text een TextFlow object. De Text klasse geeft de mogelijkheid om de text **dik-gedrukt** te krijgen. Ook is de TextFlow de maximale breedte meegegeven, hier zonder variabele nog, als magicnumber.

<img src="schedule-Week3-5.png" alt="Schedule Tab Progress" width="400"/>

In de afbeelding hierboven is weer te zien hoe de kleuren zijn geworden. Voor de rest zijn er kleine aanpassingen gedaan, zoals de window bij het toevoegen en aanpassen van shows was nog resizable, wat dus niet meer is.

<img src="schedule-Week3-6.png" alt="Schedule Tab Progress" width="400"/>
<img src="schedule-Week3-7.png" alt="Schedule Tab Progress" width="400"/>

De laatste afbeelding van de schedule tab is de uiteindelijke geworden voor de demo bij de senior. ten slot de weergave van visual-tab hieronder, een canvas in een scrollpane, hier heb ik zelf niet aan gewerkt, maar wel aangepast bij het groter maken van de applicatie window.

<img src="visual-Week3-1.png" alt="Visual Tab Progress" width="400"/>

### **Reflectie technische & vakinhoudelijke bijdrage**


Bij een artiest wilde we een afbeelding gebonden, dit werkte niet. We kwamen er niet uit waarom gson/json het niet wilde. Dus hadden we een andere optie; filePath opslaan als string, ik heb dit ontwikkeld, werkend. Alleen deed ook nu helaas de gson/json niet (ook hier stack overflow error). Deze error verwees alleen naar de gson library en niet naar een lijn in de code. Johan Talboom heeft hier ook naar gekeken en kwam er ook niet uit.

Hierbij lees je de directory van de map in Resources folder uit, een aparte folder genaamd 'Artist_Images'. De files die eindigen op '.jpg', '.jpeg' of '.png' worden weergegeven als optie in een ComboBox en de geselecteerde optie wordt weergegeven. Ook is er de optie 'None' die de default artiesten afbeelding weergeeft als standaard optie in de ComboBox.

Omdat dit uiteindelijk niet werkte hebben we uiteindelijk besloten om dit als aparte branch te behouden en te werken aan de bugs en ontbrekende features van de agenda module in andere feature branches.

---

<div id="week4">
    <h2>
        <a href="TOC">Week 4</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**

- TestCaseDiagram en testen Schedule tab

### **Reflectie technische & vakinhoudelijke bijdrage**

- Constraints over Stages, de hoeveelheid op de map en capacity


---

<div id="week5">
    <h2>
        <a href="TOC">Week 5</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**


### **Reflectie technische & vakinhoudelijke bijdrage**

---

<div id="week6">
    <h2>
        <a href="TOC">Week 6</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**


### **Reflectie technische & vakinhoudelijke bijdrage**

---

<div id="week7">
    <h2>
        <a href="TOC">Week 7</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**


### **Reflectie technische & vakinhoudelijke bijdrage**

---

<div id="week8">
    <h2>
        <a href="TOC">Week 8</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**


### **Reflectie technische & vakinhoudelijke bijdrage**

---

<div id="week9">
    <h2>
        <a href="TOC">Week 9</a>
    </h2>
</div>

### **Reflectie eigen bijdrage**


### **Reflectie technische & vakinhoudelijke bijdrage**


---

<div id="onderzoeksMethodiek">
    <h2>
        <a href="TOC">Reflectie Onderzoeksmethodiek</a>
    </h2>
</div>
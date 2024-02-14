# HHS SE S4 - GitHub Lab

Als onderdeel van dit college gaan jullie een Lab uitvoeren, waarbij jullie GitHub gebruiken voor het werken met Version Control. Het is een lab dat je **met je groepje** uitvoert. We gaan geen code bewerken, maar alleen tekst. Hierdoor hoef je je alleen te focussen op de concepten en niet ook nog op (onbekende) code.

> [!CAUTION]
> Loop het stap voor stap door. Als je een stap mist, kan het zijn dat vervolgopdrachten niet lukken.
> Tot paragraaf 4 werk je alleen maar in je browser, vanaf paragraaf 4 ga je een IDE gebruiken voor wijzigingen.

# 1. Initialiseren repo

1. Initialiseer je repo door een README.md en een .gitignore toe te voegen
2. Voeg de groepsnaam aan de README.md toe en commit deze wijziging via de webinterface

> [!NOTE]
> Je merkt dat er geen branch nodig is en dat je direct op de main branch kunt wijzigen. Als je ervan uit wil gaan dat je main branch alleen maar code bevat die door minstens vier ogen bekeken is en wellicht gecontroleerd is door een CI pipeline, dan is dit niet wenselijk. We komen er later op terug.

# 2. Werken met branches en pull requests

1. Maak een feature branch aan
2. Maak een wijziging in de feature branch in de README.md en commit deze wijziging
3. Maak een pull request aan en laat een medegroepslid deze reviewen en mergen
4. Zorg er ook voor dat de branch weer verwijderd wordt

> [!NOTE]
> Pull Requests zijn de manier om wijzigingen van 1 branch in de andere te mergen in GitHub.

5. Maak nog een feature branch aan
6. Maak daar een wijziging in de README.md en commit deze
7. Laat iemand anders een wijziging maken in de .gitignore in de **main** branch en deze committen
8. Voer een **forward integration** uit; merge de wijziging van de .gitignore van de main naar de feature branch via een pull request
9. Maak nu een pull request in de feature branch en merge deze weer naar main
10. Laat iemand anders de pull request reviewen en mergen
11. Verwijder de feature branch

> [!NOTE]
> Het is goed gebruik om voordat je een pull request op je feature branch maakt, eerst een **forward integration** te doen. Je haalt daarbij de laatste wijzigingen uit de main branch op. Hiermee voorkom je dat je op het moment dat je de pull request aanmaakt, je merge conflicts krijgt.

# 3. Branch policies 

Je gaat nu Branch policies instellen, waardoor het verplicht wordt om via een pull request op de main branch wijzigingen te maken. Dit zorgt ervoor dat de main branch code van een vantevoren afgesproken kwaliteit bevat.

1. Stel de branch policies zo in dat:
   * Pushes direct naar de main branch niet meer toegestaan zijn
   * Pull requests verplicht zijn voor het mergen (1 approver)
   * De laatste push van een pull request moet door iemand anders goedgekeurd worden dan de pusher
   * Ook alle opmerkingen in de conversatie moeten opgelost zijn
2. Test de branch policy door een commit te maken, rechtstreeks op de main branch. Als je dit doet, zou je een foutmelding moeten krijgen.
3. Maak een feature branch aan
4. Maak een wijziging in de feature branch in de README.md en commit deze wijziging
5. Maak een pull request aan en laat een medegroepslid deze reviewen en mergen
6. Zorg er ook voor dat de branch weer verwijderd wordt

> [!NOTE]
> Je ziet dat je nu niet meer rechtstreeks op de main branch kunt wijzigen. Dit is een belangrijk onderdeel van het werken met GitHub. Het zorgt ervoor dat de main branch alleen maar code bevat die door minstens vier ogen bekeken is en wellicht gecontroleerd is door een CI pipeline. De CI pipeline wordt in het volgende gastcollege behandeld.

# 4. Een IDE gebruiken zoals Visual Studio Code

1. Open Visual Studio Code (of je eigen IDE)

# 5. Tegelijkertijd wijzigingen maken in aparte branches en deze samenvoegen

1. Maak ieder een eigen feature branch aan

# 6. Werken met historie


# HHS SE S4 - GitHub Lab

Als onderdeel van dit college gaan jullie een Lab uitvoeren, waarbij jullie GitHub gebruiken voor het werken met Version Control. Het is een lab dat je **met je groepje** uitvoert. We gaan geen code bewerken, maar alleen tekst. Hierdoor hoef je je alleen te focussen op de concepten en niet ook nog op (onbekende) code.

> [!CAUTION]
> Loop het stap voor stap door. Als je een stap mist, kan het zijn dat vervolgopdrachten niet lukken.
> Tot paragraaf 4 werk je alleen maar in je browser, vanaf paragraaf 4 ga je een IDE gebruiken voor wijzigingen.

> [!TIP]
> Naast Visual Studio Code, kan ik adviseren om de volgende tools te installeren:
> 
> * [Git Fork](https://git-fork.com/) - Erg handig, omdat er een hoop gevisualiseerd wordt en het is mogelijk om de uitgevoerde git commando's te zien
> * [GitHub Desktop](https://desktop.github.com/) - Hiermee is het mogelijk om signed commits te maken (zonder dat je met GPG keys hoeft te werken) wat in sommige organisaties verplicht is

# 1. Initialiseren repo

1. Initialiseer je repo door een README.md en een .gitignore toe te voegen
2. Voeg de groepsnaam aan de README.md toe en commit deze wijziging via de webinterface

> [!NOTE]
> Je merkt dat er geen branch nodig is en dat je direct op de main branch kunt wijzigen. Als je ervan uit wilt gaan dat je main branch alleen maar code bevat die door minstens vier ogen bekeken is en wellicht gecontroleerd is door een CI pipeline, dan is dit niet wenselijk. We komen er later op terug.

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

Een lab over het werken met pull requests vind je hier: https://github.com/skills/review-pull-requests

# 3. Branch policies 

Je gaat nu Branch policies instellen, waardoor het verplicht wordt om via een pull request op de main branch wijzigingen te maken. Dit zorgt ervoor dat de main branch code van een vantevoren afgesproken kwaliteit bevat.

> [!NOTE]
> Omdat jullie een Pro licentie hebben, kunnen jullie branch policies instellen. Deze policies kunnen echter niet "enforced" worden, dit is geen onderdeel van de "Pro" licentie. Dit betekent dat je de policies wel kunt instellen, maar dat je er niet op kunt vertrouwen dat ze ook daadwerkelijk nageleefd worden. Dit is een belangrijk verschil met de "Enterprise" licentie. Ga er voor nu vanuit dat de policies wel nageleefd moeten worden.

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

In een IDE heb je veel meer mogelijkheden dan in de webinterface van GitHub. Je kunt bijvoorbeeld makkelijker wijzigingen maken, je kunt makkelijker zien wat er gewijzigd is en je kunt makkelijker wijzigingen mergen. In deze paragraaf ga je met je groepje samenwerken in een IDE.

1. Alle groepsleden openen Visual Studio Code (of een andere eigen IDE)
2. Iedereen doet een clone de repository naar de lokale machine (via de IDE of via het commando: `git clone <url>`, waarbij je `<url>` vervangt door de URL van je repository)
3. Werk samen, er moeten twee verschillende feature branches aangemaakt worden (als je bijvoorbeeld met z'n vieren bent dan werk je in tweetallen, ieder tweetal maakt een eigen feature branch aan)
4. Publiceer de feature branches naar de repository (ZONDER wijzigingen)
5. Start nu met het maken van wijzigingen in de feature branches. Probeer alles door elkaar te doen, zodat je merge conflicten krijgt
6. Zorg ervoor dat alles gemerged wordt naar de feature branches
7. Maak voor elke feature branch een pull request aan
8. Merge de eerste pull request
9. Voer een **forward integration** uit; merge de wijziging van de main naar de tweede feature branch. Dit dien je via je lokale repo te doen. Grofweg zijn de stappen als volgt:
   1. checkout main
   1. pull (bij voorkeur met een rebase, zodat je geen merge commit krijgt)
   1. checkout <feature branch>
   1. merge main
   1. Los eventuele merge conflicten op
   1. force push
10. Maak de tweede pull request aan
11. Laat iemand anders de pull request reviewen en mergen

> [!NOTE]
> Je merkt dat het, ondanks de feature branches en pull requests, nog best lastig kan zijn om wijzigingen te mergen. Dit komt omdat je met meerdere mensen aan dezelfde code werkt. Dit is een belangrijk onderdeel van het werken met GitHub. Het zorgt ervoor dat je goed moet communiceren en dat je goed moet nadenken over de wijzigingen die je maakt. Zorg er ook voor dat je regelmatig een forward integration uitvoert, zodat je de laatste wijzigingen uit de main branch opneemt.

Wil je meer leren over het aanpakken van merge conflicten? Volg dan deze GitHub skills lab: https://github.com/skills/resolve-merge-conflicts.

# 5. Overige Repo instellingen

In GitHub kun je nog veel meer instellingen maken in je repo. Denk hierbij aan instellingen met betrekking tot rechten, maar ook instellingen met betrekking tot de history die je in Git wilt opbouwen; linear of non-linear.

1. Ga naar de instellingen van de repository (tab: general)
2. Stel de repository dusdanig in dat alleen squash merges toegestaan zijn
3. Probeer nu een pull request te mergen, waarbij je meerdere commits hebt. 

> [!NOTE]
> Je zult zien dat de commits samengevoegd worden tot 1 commit. Dit zorgt ervoor dat het eenvoudiger wordt om een wijziging terug te draaien. Je hoeft immers maar 1 commit terug te draaien in plaats van alle commits die nodig waren voor de wijziging.

4. Ga opnieuw naar de instellingen van de repository (tab: Collaborators and teams)
5. Voeg een van de andere groepen toe en zorg dat zij alleen kunnen lezen
6. Vraag die groep om te controleren of zij inderdaad alleen kunnen lezen


---
title: Fejlfinding af Microsoft Teams-integration
description: 'Få mere at vide om, hvad du kan gøre for en administrator at styre Microsoft Teams-integrationen.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 10/01/2021
ms.author: jswymer
---

# <a name="troubleshooting-microsoft-teams-integration-with-include-prodshortincludesprodshortmd" />Fejlfinding af Microsoft Teams-integration med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikel indeholder oplysninger om, hvordan du identificerer og løser problemer, der kan opstå, når du bruger Microsoft Teams med [!INCLUDE [prod_short](includes/prod_short.md)], som typisk bruger eller administrator.

## <a name="the-sign-in-link-doesnt-work" />Dette link til logon fungerer ikke

Hvis du forsøger at logge på appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams, umiddelbart efter at du har installeret appen, og linket til logon ikke reagerer, kan det skyldes, at installationen af appen ikke er fuldført. Hvis du vil forsøge at løse problemet, skal du logge af Teams-klienten og derefter logge på igen.

## <a name="the-settings-page-is-empty" />Siden Indstillinger er tom

Du skal logge på først for at få adgang til dine indstillinger. Hvis du vil logge på appen, skal du enten indsætte et link til en [!INCLUDE [prod_short.md](includes/prod_short.md)]-post eller søge efter kontakter. Begge disse handlinger vil føre dig gennem en registreringsprocedure, hvorefter du kan bruge siden **Indstillinger**.

## <a name="i-changed-company-but-it-didnt-seem-to-work" />Jeg har skiftet regnskab, men det fungerer ikke

Når du skifter regnskab på siden **Indstillinger**, vil du muligvis bemærke, at rullelisten i kommandoboksen angiver, at du stadig søger i det forrige regnskab. Dette problem opstår, når du åbner siden **Indstillinger** direkte fra kommandoboksen. I dette tilfælde skiftes regnskabet korrekt, og du vil faktisk søge i det regnskab, du har skiftet til. Problemet er, at rullelisten i kommandoboksen ikke er blevet opdateret endnu. For at rullelisten skal afspejle det regnskab, du vil søge i, skal du lukke eller frigøre [!INCLUDE [prod_short.md](includes/prod_short.md)] fra kommandoboksen og derefter åbne appen igen.


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts" />Fejlen "Noget gik galt" vises ved søgning efter kontakter

Du kan opleve denne fejl, når du søger i et regnskab, der ikke er initialiseret eller ikke er i stand til at svare. Du kan f.eks. ikke søge i et nyt prøveregnskab, hvor vilkårene for anvendelse endnu ikke er blevet accepteret. Du kan løse dette problem ved at logge på [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklienten og reagere på eller lukke de indledende dialogbokse, der vises.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts" />Fejlmeddelelsen "Kontaktoversigt over kontakt/Kontaktoversigt blev ikke fundet" under søgning efter kontakter

Dette problem kan skyldes tilpasninger eller brancheløsninger, der påvirker eller ændrer [!INCLUDE [prod_short.md](includes/prod_short.md)], eller de angiver ikke en oversigt over-API til kontakt eller kontakt. Hvis problemet fortsætter, skal du kontakte din administrator eller supportudbyder.

## <a name="none-of-my-links-expand-into-a-card" />Ingen af mine links udvides til et kort

Hvis du oplever dette problem, kan du prøve at:

1. Kontroller først, at [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams er installeret.

    Kontroller ved åbne Teams stationære pc-app eller Teams i browseren. Vælg derefter på venstre side **Apps**, og søg efter **[!INCLUDE [prod_short](includes/prod_short.md)]**. Når du finder **[!INCLUDE [prod_short](includes/prod_short.md)]**-appen, skal du vælge den for at åbne siden App-oplysninger. Hvis knappen **Tilføj til mig** vises, er appen [!INCLUDE [prod_short](includes/prod_short.md)] ikke installeret. Du kan finde flere oplysninger om, hvordan du installerer appen, i [Installation af [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gæstebrugere kan ikke straks installere apps. Du kan finde flere oplysninger om gæstebrugere på vores ofte stillede spørgsmål om samarbejde med gæster. 

2. Kontroller derefter, at du har logget ind med den korrekte identitet.

    I Teams skal du gå til en vilkårlig chat, højreklikke under meddelelsesboksen på ikonet [!INCLUDE [prod_short](includes/prod_short.md)] og derefter vælge **Indstillinger**. Når vinduet vises, skal du kontrollere, om brugeren har forbindelse, så det passer til det, du bruger til at oprette forbindelse til [!INCLUDE [prod_short](includes/prod_short.md)].

3. Kontroller at kodeenhed 2718 **Page Summary Provider** udgives som en webtjeneste.

    Teams opretter forbindelse til [!INCLUDE [prod_short](includes/prod_short.md)] ved hjælp af et slutpunkt til denne kodeenhed på [!INCLUDE [prod_short](includes/prod_short.md)]-tjenesten. Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

4. Din organisation kan også begrænse, at du indsætter hyperlinks i kort. Kontakt administratoren for at få kendskab til de team politikker, der gælder for dig.

## <a name="my-link-sometimes-doesnt-expand-into-a-card" />Mine hyperlinks udvides nogle gange ikke til et kort

Et link kan ikke udvides til et kort i følgende situationer:

- Hyperlinket er rettet mod en side, som (på et teknisk niveau) ikke er knyttet til en kildetabel i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollere om en side har en kildetabel ved hjælp af sideinspektionsruden i webklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om sideinspektion i [Inspicere sider](across-inspect-page.md).
- Teams understøtter ikke linkeksempler i alle sine funktioner. Det kan f.eks. ske, når du åbner en chat, eller du er gæst hos en anden organisation.
- Teams afbryder uovervåget forsøg på at vise kortet efter 15 sekunder, f.eks. pga. netværksproblemer.
- Teams kan ikke udvide hyperlinket, hvis du allerede har indsat et hyperlink i den samme meddelelsesboks og har slettet kortet.

Linket skal også indeholde alle de oplysninger, der er nødvendige for at finde posten og få vist det tilsvarende kort. Disse oplysninger omfatter:

- Miljønavnet, ved at medtage det i URL-stien. Hvis du ikke angiver et miljønavn, antager Teams, at du forsøger at få adgang til miljøet med navnet "Produktion".
- Firmanavn ved hjælp af parameteren *Virksomhed=*
- Side-id ved hjælp af parameteren *side=*
- Bogmærket til posten ved hjælp af parameteren *Bookmark=*

Eksempler:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Du kan finde tekniske oplysninger om URL-adresser for [!INCLUDE [prod_short](includes/prod_short.md)] under [Webklientens URL-adresse](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) i [!INCLUDE [prod_short](includes/prod_short.md)]-hjælp til udviklere og it-fagfolk.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown" />Vinduet detaljer åbnes, men der vises en fejlmeddelelse, inden detaljer vises

Dette problem kan skyldes et par ting: manglende tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)] eller webbrowserindstillinger (når der bruges Teams i browseren).

1. Kontroller tilladelserne i [!INCLUDE [prod_short](includes/prod_short.md)].

    Hvis du vil have vist detaljer om et kort [!INCLUDE [prod_short](includes/prod_short.md)], skal du kontrollere licensen og tilladelserne for at få vist den pågældende post og side i det specifikke regnskab og miljø. Hvis du ikke har tilladelse til noget af disse ting, vises standardfejlmeddelelsen [!INCLUDE [prod_short](includes/prod_short.md)] om tilladelserne i vinduet detaljer. 

    Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)

2. Kontroller browserindstillingerne, hvis du bruger teams i browseren.

    - Blokeringen af pop op-vinduer i browseren skal enten være deaktiveret eller indstillet til at tillade pop op-vinduer fra domænerne *businesscentral.dynamics.com* eller *bc.dynamics.com*. Du kan finde flere oplysninger om, hvordan du tillader pop op-vinduer i [!INCLUDE [prod_short](includes/prod_short.md)], skal du se [Opsætning af browseren](across-browser-settings.md#popup).
    - Browseren skal have adgang til lokal browser storage for cookies og præferencer, mens du arbejder.
    - Undgå at bruge gæst eller privat browsing, medmindre det er nødvendigt, fordi de sletter eller blokerer noget indhold i nogle browsere.

    Du kan finde flere oplysninger om minimumskrav til browseren i [Minimumskrav til brug af [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams" />Jeg har problemer med kameraet eller stedet i grupper

Når du bruger [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner i vinduet detaljer, som kræver adgang til din placering eller dit enheds kamera, skal du først give dit samtykke til, at teams kan få adgang til disse enhedsfunktioner.  

- For Teams i browseren skal du kontrollere, at browserindstillingerne giver adgang til kamera og placering for https://teams.microsoft.com. 

- For Teams i iOS eller Android skal du kontrollere, at enhedsindstillingerne giver adgang til kamera og placering for Teams-mobilapp. 

Hvis du vil have hjælp til at ændre disse indstillinger, skal du se [Mit kamera virker ikke i Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) i Microsoft Support.

[!INCLUDE [prod_short](includes/prod_short.md)]-appen understøtter ikke placering i Teams-desktopappen. Du kan finde flere oplysninger om placering i [Ofte stillede spørgsmål om Teams](teams-faq.md#location).

Nogle browsere, f.eks. den nye Microsoft Edge, giver dig mulighed for at vælge, hvilket enheds kamera der skal bruges, når enheden understøtter flere kameraer. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details" />Teams viser blandede sprog for mine kort og kort detaljer

Hvis kort og kort skal vises ensartet på samme sprog i grupper, skal sproget for team klienten og det sprog, du bruger i [!INCLUDE [prod_short](includes/prod_short.md)]-webklienten, være ens.

- Hvis du vil vide mere om ændring af sproget i grupper, skal du se [Ændre indstillinger i Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) i Microsoft Support. 

- Hvis du vil vide mere om ændring af sproget i [!INCLUDE [prod_short](includes/prod_short.md)], se [Ændre grundlæggende indstillinger – sprog](ui-change-basic-settings.md#language).

Du kan finde flere oplysninger om, hvordan sprog fungerer mellem grupper og [!INCLUDE [prod_short](includes/prod_short.md)], i [Ofte stillede spørgsmål om Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved" />Jeg har redigeret et felt i detalje vinduet, men ændringen blev ikke gemt

De ændringer, du foretager i et felt i detalje vinduerne, gemmes automatisk, når du forlader feltet. Før du lukker vinduet, efter at du har ændret et felt, skal du trykke på <kbd>Tab</kbd> eller klikke uden for feltet.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it" />Der vises et nyt felt i Appstarteren. Hvordan fjerner jeg det?

Når du får vist dine apps på Office 365-startsiden (https://home.office.com) eller i appstarteren, vises der et nyt felt med navnet "Business Central Teams Integration Service Connector" efter installation af [!INCLUDE [prod_short](includes/prod_short.md)]-app'en til Teams. Dette felt indeholder ingen værdi i sig selv og kan være sikkert skjult.

Som administrator, der har Azure Active Directory-administratorrettigheder, kan du skjule flisen ved at benytte følgende fremgangsmåde:

1. Log på [Azure Active Directory-administrationscenter](https://aad.portal.azure.com/).
2. Vælg **virksomhedsapps**, og vælg derefter **Business Central Teams Integration Service Connector**.
3. Vælg **Egenskaber**, og angiv derefter indstillingen **Synlig for brugere** til **Nej**.
4. Vælg **Gem**.

> [!NOTE]
> Det vil vare et stykke tid, før ændringen træder i kraft.

## <a name="duplicate-text-in-the-share-to-teams-window" />Dublettekst i vinduet Del til Teams

Når du indsætter tekst i meddelelsesboksen i vinduet **Del til Teams**, duplikeres teksten. Dette problem er kendt af Microsoft og vil blive behandlet i en senere opdatering. 

## <a name="unable-to-sign-into-the-share-to-teams-window" />Vinduet Del til Teams kan ikke logges ind

Dette problem kan skyldes en række årsager. Den identitet, du bruger til at logge på skal have adgang til Microsoft Teams, f.eks. via et Microsoft 365-abonnement.

## <a name="my-cards-no-longer-have-a-popout-button" />Mine kort har ikke længere en pop-op-knap

Fra og med den 2022 vil hyperlinks, der vises som Compact kort i grupper, ikke længere indeholde knappen **Pop-op**. Hvis du vil åbne det pågældende kort i et separat vindue, skal du klikke på knappen **Detaljer** og derefter vælge **Åbn i webbrowser** i menuen ellipser (**...**) i øverste højre hjørne af vinduet.

## <a name="cant-pin-a-card-to-tab" />Kan ikke fastgøre et kort til fanen

Der er et par grunde til dette problem.

- Hvis kortet er delt mod Søg ME, kan det ikke fastgøres til en fane. 

- Kan ikke fastgøres, før du tilføjer din første Business Central-fane. Dette problem er kendt i Teams. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me" />Nogen har tilføjet en fane, men fanen vises ikke for mig

Dette problem skyldes, at du ikke har installeret BC app til Teams. Det er kun dem, der har installeret appen, som kan se Business Central-fanerne.

## <a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees" />Andre ser forskellige sorterings- eller kolonneformater, end hvad faneudvikleren ser

Dette problem skyldes sandsynligvis, at du har delt en listevisning, som er en personlig visning. I dette tilfælde skal du samarbejde med administratoren om at oprette rollespecifikke listevisninger, der dækker de forskellige roller i kanalen/chatten, eller oprette visningen for hele organisationen, så alle kan få en ensartet visning.


## <a name="see-also" />Se også

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installere appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Dele poster i Microsoft Teams](across-working-with-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Ændring af virksomhed og andre indstillinger i Teams](across-teams-settings.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## <a name="included365finincludesfreetrialmdmd" />[!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Registrere forbrug eller forbrug af sagsopgaver og varer
description: 'Denne artikel beskriver, hvordan du registrerer forbrug af varer eller ressourcer på sager for at gøre projektstyringen nemmere.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-jobs" />Registrere forbrug eller forbrug til sager

Fra siden **jobkort** kan du åbne siden **Sagsplanlægningslinjer** for at gennemgå og registrere brugen af forskellige dele af sagen. Disse oplysninger opdateres automatisk, når du ændrer og overfører oplysninger mellem sager og sagskladder eller sagskladder. Dette kræver, at du aktiverer **Anvend anvendelseslink som standard** til/fra på siden **Konfigurer sager**. Flere oplysninger i [Konfigurere sager](projects-how-setup-jobs.md).  

F.eks. kan du angive antallet af en ressource, og hvilken mængde, der skal overføres til sagskladden, for planlægningslinjer af typen **Budget**. Hvis planlægningslinjens type er **Fakturerbar**, kan du angive antallet af ressourcen, og angive hvilket antal, der skal overføres til en faktura. Yderligere oplysninger om fakturering af debitor finder du i [Fakturasager](projects-how-invoice-jobs.md). Ved at sammenligne den oprindelige mængde, restantal eller bogført antal kan du hurtigt gennemgå oplysninger om forbrug. Du kan finde oplysninger om vurdering af budgetterede værdier under planlægning under [Administrere sagsbudgetter](projects-how-manage-budgets.md).  

Følgende procedurer beskrives, hvordan du kan registrere faktiske (fakturerbare) mængder eller udgifter ved sagskladde. Du kan også bruge købsdokumenter til at registrere indkøb for en sag. Få mere at vide i [Administrere sagsforsyninger](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget" />Sådan registreres forbrug for en sagsplanlægningslinje af typen Budget

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Sagsplanlægningslinjer**. 
3. Vælg en sagsplanlægningslinje af typen **Budget** eller **Både budget og fakturerbar**, som du vil registrere forbruget for.   

    > [!NOTE]
    > Du kan også registrere forbrug for en sagsplanlægningslinje af typen **Fakturerbar**. I dette tilfælde skal du typisk bruge disse linjer til at oprette fakturaer, men du kan også overføre det til en kladde. Flere oplysninger [Fakturere sager](projects-how-invoice-jobs.md) 

4. I feltet **Antal, der skal overføres til kladde** skal du angive det nummer, du vil overføre. Standardantallet er den værdi, du angiver i feltet **Antal**.

    Feltet **Restantal** viser det antal, der mangler for at afslutte sagen og blive overført til kladden.
5. Vælg handlingen **Opret sagskladdelinjer**.

    > [!TIP]
    > Hvis du vil tilføje flere sagsplanlægningslinjer for denne sag, skal du vente med dette trin, indtil du har tilføjet alle sagsplanlægningslinjer.
6. På siden **Kopier sag til sagsplanlægningslinje** skal du udfylde felterne efter behov og derefter vælge knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Vælg handlingen **Åbn sagskladde**.  
8. På siden **Sagskladde** skal du markere den relevante linje, og derefter vælge handlingen **Bogfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. På siden **Sagsplanlægningslinjer** skal du gennemgå det registrerede forbrug ved at holde øje felterne **Antal**, **Restantal** og **Antal, der skal overføres til kladde**.  
10. Gentag trin 3 til 8 for at registrere ekstra forbrug.  

## <a name="to-create-job-journal-lines-manually" />Sådan oprettes sagskladdelinjer manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2. I feltet **Kladdenavn** skal du vælge et relevant sagskladdenavn.  
3. På en ny linje skal du angive bilagsnummer, sagsnummer, sagsopgavenummer, type og mængde af den type, der forbruges.  
4. Når sagskladdelinjerne er fuldført, skal du vælge handlingen **Bogfør**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-job-usage-estimates-and-post-updates" />Sådan vises sagsforbrugsestimater og bogføringsopdateringer

Du kan få vist sagsforbruget op til færdiggørelsen af et projekt i ét trin. Hvis du vil gøre det, skal du bruge kørslen **Beregn resterende forbrug for sag** for alle sagerne op til og inklusive afslutningen af en sag.  

På denne måde kan du holde styr på og sammenligne dine oprindelige estimater med de faktiske resultater og foretage ændringer eller oprette nye poster efter behov. Du kan f.eks. have anslået, at en sag krævede 10 timer, og at den frem til nu har taget 15 timer. Du kan føje de ekstra fem timer til den eksisterende kladdelinje eller oprette en ny kladdelinje for at rapportere disse fem timer som overtid, hvilket er en anden arbejdstype. Den korrekte omkostning og pris beregnes, og du kan derefter bogføre den til kladden.  

> [!NOTE]  
> Vareposter opretter vareposter til finans og reducerer antallet af varer på lager. Kørslen **Bogfør lagerregulering** overfører omkostningen fra lager til finans. Ressourceposter opretter ressourceposter til finans.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2. Vælg en relevant sagskladde, og vælg derefter handlingen **Beregn resterede forbrug**.  
3. På siden **Beregn resterende forbrug for sag** skal du angive dokumentnummeret og bogføringsdatoen, der skal indsættes i kladden, og derefter vælge knappen **OK**.  
4. Opdater kladden med eventuelle nødvendige ændringer.  
5. Vælg **Bogfør**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job" />Opret lagerbeholdnings- lagersteds-plukdokumenter for et job

Hvis du vil oprette lagerplukdokumenter for sager, skal din administrator aktivere **Funktionsopdatering: Aktivér lagerbeholdning og lagerpluk fra job** på siden **Funktionsstyring**.

Funktionen tilføjer handlingerne **Opret pluk (lager)** og **Opret lager (logistik)** på **Jobkort**. Hvis du vil oprette eller registrere et plukdokument, skal du bruge **Læg-på-lager/pluk-linjer/bevægelseslinjer** eller **registrerede pluklinjer**. Flere oplysninger i [Flows for produktion, montage og sager](design-details-internal-warehouse-flows.md).

Du kan bruge handlingerne under følgende betingelser:

* Sagens **status** er **åben**.
* **Linjetypen** for sagsplanlægningslinjen er **budget** eller **Både budget og fakturerbart**.
* **Typen** på sagsplanlægningslinje er **vare**.
* **Kræv pluk** er aktiveret for den relaterede lokation.
* **Styret læg-på-lager og pluk** er deaktiveret.

> [!NOTE] 
> Selvom indstillingen kaldes **kræver pluk**, kan du stadig bogføre forbrug direkte fra sagskladdelinjen for lokationen. Hvis lokationen er sat op til at kræve pluk, men ikke leverance, skal du bruge dokumentet **Pluk (lager)** til at organisere og udskrive plukaktiviteten. Du kan også bruge siden til at angive og bogføre resultatet af plukket, som igen bogfører forbruget af varer. 
> 
> Hvis lokationen er indstillet til at kræve både pluk og leverance, dvs. at du har markeret både feltet **Kræv pluk** og feltet **Kræv leverance** på **lokationskortet**, kan du bruge siden **Pluk (logistik)** til at håndtere plukningen. Lagerpluk svarer til pluk (lager). Forskellen er, at i stedet for at bogføre plukoplysninger, registrerer du plukket. Denne registrering bogfører ikke forbrug, den gør blot varerne disponible til bogføring. Som lagerchef kan du bruge en plukkladde til at organisere plukoplysningerne, før du opretter de enkelte plukinstruktioner (logistik)

## <a name="to-review-planning-lines-for-a-job-ledger-entry" />Sådan gennemgås planlægningslinjerne for en sagspost

Når du har bogført sagskladdelinjer, kan du se de planlægningslinjer, der er knyttet til posterne i sagskladden, der er blevet bogfør.

> [!NOTE]  
> Dette kræver, at afkrydsningsfeltet **Anvend anvendelseslink** er markeret for opgaven. Der er flere oplysninger i [Konfigurere sager](projects-how-setup-jobs.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2. Vælg en relevant sagskladde, og vælg derefter handlingen **Poster**.  
3. På siden **Sagsposter** skal du vælge handlingen **Vis tilknyttede sagsplanlægningslinjer**.

## <a name="see-related-microsoft-trainingtrainingpathspost-job-usage-sales" />Se relateret [Microsoft-træning](/training/paths/post-job-usage-sales/)

## <a name="see-also" />Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

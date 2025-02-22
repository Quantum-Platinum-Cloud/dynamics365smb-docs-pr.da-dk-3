---
title: Allokeringsstatus og reparationsstatus | Microsoft Docs
description: Få mere at vide om relationerne mellem serviceartiklernes reparationsstatus og allokeringsposternes allokeringsstatus for dem.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resources, allocation, status, repairs'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocation-status-and-repair-status-of-service-items" />Allokeringsstatus og reparationsstatus for serviceartikler
Der er en særlig relation mellem serviceartiklernes reparationsstatus og allokeringsposternes allokeringsstatus for serviceartiklerne i Service. Allokeringsstatus ændres, når du ændrer reparationsstatus for serviceartiklen til **Udført** eller **Delvist repareret**, og når du konverterer et servicetilbud til en serviceordre. Reparationsstatus for serviceartiklen ændres, når du annullerer serviceartikelallokeringen eller genallokerer serviceartiklen til en anden ressource. Du kan få vist reparationsstatus for serviceartiklerne på siden **Serviceopgaver**, og du kan opdatere reparationsstatussen i feltet **Reparationsstatuskode** på siden **Serviceartikelkladde**. Du kan få vist allokeringsstatus i feltet **Status** på siden **Ressourceallokeringer**.  
  
## <a name="changing-repair-status" />Ændre reparationsstatus
Når du ændrer reparationsstatus for en serviceartikel på en serviceartikellinje, søges der automatisk efter en tilsvarende allokeringspost for serviceartiklen, som har status **Aktiv**. Hvis der bliver fundet en sådan allokeringspost, opdateres dens status på en af følgende måder:  
  
* Hvis du ændrer reparationsstatus til **Udført**, ændres allokeringsstatus automatisk fra **Aktiv** til **Udført**.  
* Hvis du ændrer reparationsstatus til **Delvist repareret**, dvs. at en del af reparationen er udført, eller **Henvist**, dvs. at der er ikke lavet nogen reparation, ændres allokeringsstatus fra **Aktiv** til **Genallokering nødvendig**.  
* Når der er oprettet en serviceordreallokeringspost, der angiver, at der ikke er allokeret ressourcer, angives feltet **Status** på siden **Ressourceallokering** til **Inaktiv**.  
* Allokeringsstatus indstilles til **Annulleret**, når du igen allokerer den henviste serviceartikel i serviceordreallokeringsposten, hvilket angiver, at den allokerede ressource eller ressourcegruppe ikke har forsøgt at udføre serviceopgaven.  
  
Allokeringsstatus viser, hvornår reparationsprocessen er afsluttet, eller hvornår det er nødvendigt, at en anden ressource gør reparationen af serviceartiklen færdig.  
  
## <a name="converting-service-quotes-to-service-orders" />Konvertere servicetilbud til serviceordrer
Når du konverterer et servicetilbud til en serviceordre, opdateres serviceordren og serviceartiklerne i ordren samt de tilhørende allokeringsposter på følgende måde:  
  
* Serviceartiklernes reparationsstatus ændres til **Oprettet**  
* Serviceordrens status ændres til **Igangsat**.  
* Der søges automatisk efter allokeringsposter for alle de serviceartikler i serviceordren, der har status **Aktiv**. Hvis der bliver fundet sådanne allokeringsposter, ændres deres allokeringsstatus fra **Aktiv** til **Genallokering nødvendig**.  
  
## <a name="canceling-allocations" />Annullere allokeringer
Når du annullerer en allokering for en serviceartikel, opdaterer [!INCLUDE[prod_short](includes/prod_short.md)] allokeringsstatus for den tilsvarende allokeringspost fra **Aktiv** til **Genallokering nødvendig**.

Serviceartiklens reparationsstatus i allokeringsposten opdateres på følgende måde:  
  
* Hvis reparationsstatus er **Oprettet**, ændres reparationsstatus automatisk til **Henvist** (der er ikke påbegyndt nogen reparation).  
* Hvis reparationsstatus er **I arbejde**, ændres reparationsstatus til **Delvist repareret** (en del af reparationen er udført).  
  
## <a name="reallocating-an-active-allocation-entry" />Genallokere en aktiv allokeringspost
Når du genallokerer en serviceartikel i en allokeringspost, som er **Aktiv**, opdateres allokeringsposten automatisk på følgende måder:  
  
* Hvis reparationen blev startet, da allokeringen var **Aktiv** (dvs. hvis reparationsstatus for serviceartiklen i posten blev ændret til **I arbejde**), ændres allokeringsstatus automatisk fra **Aktiv** til **Udført**.  
* Hvis reparationen ikke blev påbegyndt, da allokeringen var **Aktiv**, ændres allokeringsstatus automatisk fra **Aktiv** til **Annulleret**.  
  
Reparationsstatus for serviceartiklen i allokeringsposten bliver automatisk opdateret på samme måde, som hvis du havde annulleret allokeringen:  
  
* Hvis reparationsstatus er **Oprettet**, ændres reparationsstatus automatisk til **Henvist** (der er ikke påbegyndt nogen reparation).  
* Hvis reparationsstatus er **I arbejde**, ændres reparationsstatus til **Delvist repareret** (en del af reparationen er udført).  
  
Der oprettes en ny allokeringspost, som indeholder den nye ressource og har statussen **Aktiv**.  
  
## <a name="reallocating-a-service-item" />Genallokere en serviceartikel
Når du genallokerer en serviceartikel i en allokeringspost, der har statussen **Genallokering nødvendig**, opdateres allokeringsposten automatisk på følgende måder:  
  
* Hvis reparationen blev startet, da allokeringen var **Aktiv** (dvs. hvis reparationsstatus for serviceartiklen i posten blev ændret til **I arbejde**), ændres allokeringsstatus automatisk fra **Genallokering nødvendig** til **Udført**.  
* Hvis reparationen ikke blev påbegyndt, mens allokeringen var **Aktiv**, ændrer programmet allokeringsstatus fra **Genallokering nødvendig** til **Annulleret**.  
  
Der oprettes en ny allokeringspost, som indeholder den nye ressource og har statussen **Aktiv**.  
  
## <a name="see-also" />Se også
[Opsætte ressourceallokeringer](service-how-setup-resource-allocation.md)  
[Allokere ressourcer](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]

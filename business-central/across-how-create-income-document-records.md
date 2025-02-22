---
title: Oprette indgående bilagsposter
description: 'Brug forskellige funktioner på siden indgående dokumenter til at gennemgå udgifts kvitteringer, administrere OCR-opgaver, konvertere indkommende dokumentfiler og vedhæfte eksterne filer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records" />Oprette indgående bilagsposter

På siden **Indgående bilag** kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.

Når du vil registrere et eksternt dokument i [!INCLUDE[prod_short](includes/prod_short.md)], skal du først oprette eller fuldføre en indgående bilagspost. Du kan gøre dette manuelt, eller du kan tage et billede af det eksterne dokument og derefter oprette den indgående bilagspost med billedfilen vedhæftet.

Før du kan bruge funktionen **Indgående bilag**, skal du foretage den nødvendige opsætning. Du kan finde flere oplysninger i [Konfigurere indgående bilag](across-how-setup-income-documents.md).

## <a name="approve-or-reject-an-incoming-document" />Sådan godkendes eller afvises et indgående bilag

Hvis du har angivet , at funktionen til **indgående bilag** skal godkendes, før der kan oprettes dokumenter, skal brugere med de nødvendige rettigheder godkende posterne, før de behandles. Du kan finde flere oplysninger i [konfigurere godkendere af indgående dokument poster](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
2. Marker linjen i det dokument, du vil godkende eller afvise, og vælg derefter handlingen **Godkend** eller **Afvis**.

Hvis du godkender den indgående bilagspost, markeres afkrydsningsfeltet **Frigivet** på den indgående bilagslinje. Brugeren, der har ansvaret for at godkende, f.eks, købsfakturaer, kan fortsætte med at behandle posten.

## <a name="create-an-incoming-document-record-by-taking-a-photo" />Sådan opretter du en indgående bilagspost ved at tage et billede

> [!NOTE]  
> Følgende procedure gælder kun for [!INCLUDE[prod_short](includes/prod_short.md)] tablet- og telefonklienter.

1. I rollecentret skal du vælge feltet **Opret indgående bilag fra kamera** og derefter gå til trin 4.
2. Du kan også vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
3. På siden **Indgående bilag** skal du vælge **Ny** og derefter vælge **Opret fra kamera**. Kameraet på tabletten eller telefonen aktiveres.
4. Tag et billede af et dokument, f.eks en købsleverance, som du vil behandle som et indgående bilag, og vælg derefter knappen **Brug**.

    Der oprettes en ny indgående bilagspost med billedet vedhæftet.

## <a name="attach-an-image-to-an-incoming-document-record-by-taking-a-photo" />Sådan vedhæfter du et billede til en indgående bilagspost ved at tage et billede

> [!NOTE]  
> Følgende procedure gælder kun for [!INCLUDE[prod_short](includes/prod_short.md)] tablet- og telefonklienter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
2. Åbn kortet for en eksisterende indgående bilagspost.
3. På siden bilagspostsiden skal du vælge **Behandle** og derefter vælge **Vedhæft billede fra kamera**. Kameraet på tabletten eller telefonen aktiveres.
4. Tag et billede af et dokument, f.eks en købsleverance, som du vil behandle som et indgående bilag, og vælg derefter knappen **Brug**.

    Billedet vedhæftes til den indgående bilagspost.

## <a name="create-an-incoming-document-record-manually" />Sådan oprettes en indgående bilagspost manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**, og vælg derefter **Opret ny fil**.  
3. På siden **Indsæt fil** skal du vælge en fil og derefter klikke på **Åbn**. Filen vedhæftes automatisk.
4. Du kan også vælge handlingen **Ny**.
5. Du kan vedhæfte en fil ved at vælge **Behandle** og derefter handlingen **Vedhæft fil** .
6. På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående bilag og derefter vælge knappen **Åbn**.
7. På siden **Indgående bilag** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Se relateret [Microsoft-træning](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Brug OCR til at omdanne PDF-og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)
[Oprette indkommende bilagsposter](across-how-connect-disconnect-income-document-records.md)
[Finde bogførte dokumenter uden indkommende bilagsposter](across-how-find-posted-documents-without-income-document-records.md)
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

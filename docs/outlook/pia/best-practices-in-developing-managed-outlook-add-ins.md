---
title: Méthodes conseillées pour le développement de compléments Outlook managés
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5961c66ccdd2b7d243ecfe32a9efb3ceaf9f12b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623837"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a>Méthodes conseillées pour le développement de compléments Outlook managés

Même si les assemblys d'interopérabilité Outlook vous permettent d'écrire des solutions managées qui fonctionnent avec Outlook, Outlook est antérieur au .NET Framework et est conçu pour prendre en charge la programmabilité via des langages non managés comme Visual Basic pour Applications (VBA) et Visual Basic. Cette rubrique répertorie les principaux points à prendre en considération lors du développement d'un complément managé pour Outlook.

- [Libération systématique des objets](systematically-releasing-objects.md)
- [Utilisation d’un domaine d’application distinct pour éviter les blocages](using-a-separate-application-domain-to-avoid-crashing.md)
- [Utilisation d’un objet d’application approuvée fourni par les outils de développement Office pour Visual Studio](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [Définir convenablement la portée des variables dans les gestionnaires d’événements](scoping-variables-appropriately-in-event-handlers.md)
- [Éviter les technologies non prises en charge dans les compléments Outlook managés](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [Utilisation de la liaison tardive en cas de dépendance envers plusieurs versions d’Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)


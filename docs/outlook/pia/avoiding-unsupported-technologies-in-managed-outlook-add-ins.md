---
title: Éviter les technologies non prises en charge dans les compléments Outlook managés
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e4572a7ed6ba2262874d03252f1bfb4adfefc82f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549748"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a>Éviter les technologies non prises en charge dans les compléments Outlook managés

Certaines technologies qui sont antérieures à .NET Framework ne sont pas prises en charge dans la programmation du code managé. Il s'agit notamment des technologies CDO (Collaboration Data Objects), MAPI (Messaging Application Programming Interface, souvent appelé Extended MAPI), et Simple MAPI. Ces technologies ont été conçues et développées avec du code non managé et Microsoft ne fournit aucun wrapper managé officiel pour prendre en charge leur utilisation dans des applications managées. 

Pour plus d’informations, reportez-vous à la section relative aux API prises en charge dans le code managé de l’article de la [base de connaissances 266353 : Instructions de prise en charge pour le développement de messagerie côté client](https://go.microsoft.com/fwlink/?linkid=89209).

Néanmoins, Microsoft Outlook propose de nombreuses fonctionnalités de modèle objet qui effectuent ce que seuls CDO et les extensions client Exchange (ECE) permettaient précédemment d’effectuer pour les développeurs. Si vous utilisez CDO dans une application Outlook non managée existante et que l'absence de prise en charge de CDO dans les solutions managées vous a empêché d'effectuer une migration de l'application vers le code managé, vous pouvez désormais mettre à jour votre solution vers le code managé, uniquement en faisant appel au modèle objet Outlook et à l'assembly PIA (Primary Interop Assembly), sans avoir à recourir à CDO. 

Pour plus d'informations sur une plateforme Outlook plus complète introduite dans Outlook 2007 afin de réduire la dépendance envers CDO et les Extensions de client Exchange, voir [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).


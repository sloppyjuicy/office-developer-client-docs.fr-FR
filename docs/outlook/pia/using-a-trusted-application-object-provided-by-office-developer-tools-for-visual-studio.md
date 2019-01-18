---
title: Utilisation de l’objet d’une application approuvée fourni par les Outils de développement Office pour Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f86ad294e894b4faea10d033a069638221f1bd78
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703012"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a>Utilisation de l’objet d’une application approuvée fourni par les Outils de développement Office pour Visual Studio

Si vous développez un complément managé à l’aide des Outils de développement Office pour Visual Studio, utilisez toujours l’objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) fourni par Visual Studio. 

À moins que vous n'envisagiez d'automatiser une nouvelle instance d'Outlook, n'utilisez pas le mot clé New ou new pour créer une instance d'Outlook, car cette instance de l'objet **Application** n'est pas approuvée du point de vue du module de protection du modèle objet Outlook. 

Si votre complément utilise une instance non approuvée de l'objet **Application**, selon la version d'Outlook exécutée par le client, le complément, par défaut, appellera le module de protection du modèle objet Outlook sur plusieurs membres du modèle objet. 

Pour en savoir plus sur le comportement de la protection du modèle objet, consultez l’article relatif aux [modifications de sécurité du code dans Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)). Même si cet article fait référence aux compléments COM approuvés par défaut, cette application s’applique aux versions d’Outlook depuis Outlook 2007, et l’approbation s’applique de la même manière aux compléments managés. Que le complément soit managé ou non, l'approbation est basée sur la supposition que le complément utilise un objet **Application** approuvé.


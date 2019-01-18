---
title: Installation et référencement de l’assembly PIA Outlook
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718202"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Installation et référencement de l’assembly PIA Outlook

Nous vous recommandons d’installer l’assembly PIA (Primary Interop Assembly) Outlook dans le cache GAC (Global Assembly Cache) avant d’incorporer les informations de l’assembly PIA dans un complément managé Outlook. Par défaut, l’assembly PIA est installé automatiquement quand vous installez Office sur l’ordinateur de développement. Toutefois, pour installer l’assembly PIA séparément, consultez l’article [Configurer un ordinateur pour développer des solutions Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).


> [!NOTE] 
> Seule une personne ayant un rôle d’administrateur sur l’ordinateur de développement peut installer les assemblies PIA Office.

Après l’installation, si vous utilisez Visual Studio pour créer le projet managé, vous pouvez ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0. Par la suite, dans le navigateur d'objets, sous l'espace de noms **Microsoft.Office.Interop.Outlook**, vous pouvez voir les interfaces managées de l'assembly PIA dont les noms correspondent aux objets du modèle objet Outlook.

## <a name="see-also"></a>Voir aussi

- [Installation des assemblies PIA Office](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Architecture de l’assembly PIA Outlook](architecture-of-the-outlook-pia.md)


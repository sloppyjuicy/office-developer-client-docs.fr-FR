---
title: Architecture de l’assembly PIA Outlook
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713302"
---
# <a name="architecture-of-the-outlook-pia"></a>Architecture de l’assembly PIA Outlook

L’assembly PIA (Primary Interop Assembly) Outlook prend entièrement en charge le développement avec le modèle objet Outlook dans le code managé. Toutefois, la première fois que vous observez l'assembly PIA dans un navigateur d'objets, vous risquez d'être surpris par les nombreuses interfaces supplémentaires que contient l'assembly PIA et par le fait que tous les membres (méthodes, propriétés et événements) d'un objet ne soient pas exposés par la même interface d'objet. Les rubriques de cette section indiquent comment accéder aux membres d'un objet dans le code et où rechercher de l'aide sur les objets, les méthodes, les propriétés et les événements.

## <a name="in-this-section"></a>Dans cette section

|Rubrique|Description|
|:----|:----------|
|[Mise en rapport de l’assembly PIA Outlook avec le modèle objet](relating-the-outlook-pia-with-the-object-model.md) |Décrit comment les objets et les membres du modèle objet Outlook basé sur COM sont mappés aux interfaces et classes managées correspondant dans l’assembly PIA.|
|[Objets dans l'assembly PIA Outlook](objects-in-the-outlook-pia.md) |Décrit les interfaces, classes et délégués .NET typiques qui sont mappés à un objet COM et décrit comment accéder à un objet dans l'assembly PIA.|
|[Méthodes et propriétés dans l’assembly PIA Outlook](methods-and-properties-in-the-outlook-pia.md) |Décrit comment accéder aux méthodes et propriétés d’un objet dans le code managé à l’aide de l’assembly PIA.|
|[Événements dans l'assembly PIA Outlook](events-in-the-outlook-pia.md) |Décrit les interfaces, les délégués et les classes d’assistance de récepteur liés à un événement dans l’assembly PIA.|

## <a name="see-also"></a>Voir aussi

- [Configuration pour utiliser l’assembly PIA Outlook](setting-up-to-use-the-outlook-pia.md)
- [Développement de compléments managés Outlook à l’aide de l’assembly PIA Outlook](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [Procédure (Référence PIA Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)


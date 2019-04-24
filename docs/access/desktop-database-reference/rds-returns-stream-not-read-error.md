---
title: RDS renvoie l’erreur « Flux non lu »
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300853"
---
# <a name="rds-returns-stream-not-read-error"></a>L'objet \"RDS renvoie un\" flux non lu.


**S’applique à** : Access 2013, Office 2013

« L'objet flux ne peut pas être lu car il est vide, ou la position actuelle se situe à la fin du flux. Pour les flux non vides, définissez la position actuelle à l'aide de la propriété Position. Pour savoir si un flux est vide, utilisez la propriété Size ».

L'obtention de l'erreur précédente peut être le résultat d'une tentative d'utilisation d'une requête hiérarchique paramétrée sur http. Or, RDS ne permet pas d'utiliser à distance les hiérarchies paramétrées.


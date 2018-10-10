---
title: Retour d'une erreur de type « Flux non lu » par RDS
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b3372db2ff86ea2af401720ba091100d4cfce1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472379"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS renvoie \"flux non lu\" erreur


**S’applique à**: Access 2013 | Office 2013

« L'objet flux ne peut pas être lu car il est vide, ou la position actuelle se situe à la fin du flux. Pour les flux non vides, définissez la position actuelle à l'aide de la propriété Position. Pour savoir si un flux est vide, utilisez la propriété Size ».

L'obtention de l'erreur précédente peut être le résultat d'une tentative d'utilisation d'une requête hiérarchique paramétrée sur http. Or, RDS ne permet pas d'utiliser à distance les hiérarchies paramétrées.


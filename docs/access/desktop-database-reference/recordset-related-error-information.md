---
title: Informations sur les erreurs en lien avec le recordset
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708899"
---
# <a name="recordset-related-error-information"></a>Informations sur les erreurs en lien avec le recordset

**S’applique à**: Access 2013, Office 2013

Au cours du traitement par lots, la propriété **Status** de l'objet **Recordset** fournit des informations sur chaque élément de l'objet **Recordset**. Avant la mise à jour d'un lot, la propriété **Status** de l'objet **Recordset** donne des indications concernant les enregistrements à ajouter, à modifier et à supprimer. 

Après l'appel de **UpdateBatch**, la propriété **Status** indique la réussite ou l'échec de l'opération. Lorsque vous passez d'un enregistrement à l'autre dans l'objet **Recordset**, la valeur de la propriété **Status** est modifiée afin de décrire le statut de l'enregistrement actif.


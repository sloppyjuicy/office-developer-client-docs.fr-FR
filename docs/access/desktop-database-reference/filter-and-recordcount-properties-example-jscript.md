---
title: Filter et RecordCount, propriétés – Exemple (JScript)
TOCTitle: Filter and RecordCount properties example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 993209478d18d013771de8239d8e8cd10efc5da2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718886"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a>Filter et RecordCount, propriétés – Exemple (JScript)


**S’applique à**: Access 2013, Office 2013

Cet exemple ouvre un objet **Recordset** sur la table Companies (base de données Northwind) et utilise ensuite la propriété [Filter](filter-property-ado.md) pour limiter le nombre d'enregistrements visibles à ceux dont la valeur du champ CompanyName commence par la lettre D. Coupez et collez le code suivant dans le Bloc-notes ou dans un autre éditeur de texte et enregistrez-le sous **FilterJS.asp**.


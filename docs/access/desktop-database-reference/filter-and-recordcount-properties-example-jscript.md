---
title: Filter et RecordCount, propriétés - Exemple (JScript)
TOCTitle: Filter and RecordCount Properties Example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f6b33ce6824144626a9219fa2d218d90b38ed89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471164"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a>Filter et RecordCount, propriétés - Exemple (JScript)


**S’applique à**: Access 2013 | Office 2013

Cet exemple ouvre un objet **Recordset** sur la table Companies (base de données Northwind) et utilise ensuite la propriété [Filter](filter-property-ado.md) pour limiter le nombre d'enregistrements visibles à ceux dont la valeur du champ CompanyName commence par la lettre D. Coupez et collez le code suivant dans le Bloc-notes ou dans un autre éditeur de texte et enregistrez-le sous **FilterJS.asp**.


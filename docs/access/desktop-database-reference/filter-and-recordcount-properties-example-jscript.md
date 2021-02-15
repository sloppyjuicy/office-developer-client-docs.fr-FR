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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292488"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a><span data-ttu-id="a4052-102">Filter et RecordCount, propriétés – Exemple (JScript)</span><span class="sxs-lookup"><span data-stu-id="a4052-102">Filter and RecordCount properties example (JScript)</span></span>


<span data-ttu-id="a4052-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4052-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4052-104">Cet exemple ouvre un objet **Recordset** sur la table Companies (base de données Northwind) et utilise ensuite la propriété [Filter](filter-property-ado.md) pour limiter le nombre d'enregistrements visibles à ceux dont la valeur du champ CompanyName commence par la lettre D. Coupez et collez le code suivant dans le Bloc-notes ou dans un autre éditeur de texte et enregistrez-le sous **FilterJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="a4052-104">This example opens a **Recordset** on the Companies table of the Northwind database and then uses the [Filter](filter-property-ado.md) property to limit the records visible to those where the CompanyName field starts with the letter D. Cut and paste the following code to Notepad or another text editor, and save it as **FilterJS.asp**.</span></span>


---
title: Agrégats petit-enfant
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292145"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="64d77-102">Agrégats petit-enfant</span><span class="sxs-lookup"><span data-stu-id="64d77-102">Grandchild aggregates</span></span>


<span data-ttu-id="64d77-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64d77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64d77-p101">Un *nom d'alias-chapitre* peut être donné à la colonne de chapitre créée dans une clause d'une commande de mise en forme (généralement avec le mot clé AS). Vous pouvez identifier toute colonne de n'importe quel chapitre de l'objet **Recordset** mis en forme à l'aide d'un nom complet identifiant l'enfant contenant la colonne. Par exemple, si le chapitre parent appelé chap1 contient un chapitre enfant intitulé chap2 qui comporte une colonne de montants appelé « amt », le nom complet correspond à chap1.chap2.amt. Ce nom peut alors être utilisé comme argument dans une des fonctions d'agrégation, à savoir SUM (SOMME), AVG (MOYENNE), MAX, MIN, COUNT (COMPTE), STDEV (ECARTTYPE) ou ANY).</span><span class="sxs-lookup"><span data-stu-id="64d77-p101">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword). You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>


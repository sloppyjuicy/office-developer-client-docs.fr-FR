---
title: Agrégats de petits-enfants
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947937"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="a42ad-102">Agrégats de petits-enfants</span><span class="sxs-lookup"><span data-stu-id="a42ad-102">Grandchild aggregates</span></span>


<span data-ttu-id="a42ad-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a42ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a42ad-104">Un *nom d’alias-chapitre* (généralement avec le mot clé AS) peut être donnée à la colonne de chapitre créée dans une clause d’une commande shape.</span><span class="sxs-lookup"><span data-stu-id="a42ad-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="a42ad-105">Vous pouvez identifier une colonne quelconque dans n’importe quel chapitre de l' **objet Recordset** mis en forme avec un nom complet identifiant l’enfant contenant la colonne.</span><span class="sxs-lookup"><span data-stu-id="a42ad-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="a42ad-106">Par exemple, si le chapitre parent, chap1, contient un chapitre enfant, chap2, qui a une colonne quantité, montant, puis le nom complet est Chap1.Chap2.mnt. Le nom qualifié peut ensuite être utilisé en tant qu’argument à une des fonctions d’agrégation (somme, moyenne, MAX, MIN, COUNT, STDEV ou toute).</span><span class="sxs-lookup"><span data-stu-id="a42ad-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>


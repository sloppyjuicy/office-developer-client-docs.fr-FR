---
title: Agrégats de petits-enfants
TOCTitle: Grandchild Aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e79cfe863e80e70e75d7f8e65c10764df67a39df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471637"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="bd0a0-102">Agrégats de petits-enfants</span><span class="sxs-lookup"><span data-stu-id="bd0a0-102">Grandchild Aggregates</span></span>


<span data-ttu-id="bd0a0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd0a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd0a0-104">Un *nom d’alias-chapitre* (généralement avec le mot clé AS) peut être donnée à la colonne de chapitre créée dans une clause d’une commande shape.</span><span class="sxs-lookup"><span data-stu-id="bd0a0-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="bd0a0-105">Vous pouvez identifier une colonne quelconque dans n’importe quel chapitre de l' **objet Recordset** mis en forme avec un nom complet identifiant l’enfant contenant la colonne.</span><span class="sxs-lookup"><span data-stu-id="bd0a0-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="bd0a0-106">Par exemple, si le chapitre parent, chap1, contient un chapitre enfant, chap2, qui a une colonne quantité, montant, puis le nom complet est Chap1.Chap2.mnt. Le nom qualifié peut ensuite être utilisé en tant qu’argument à une des fonctions d’agrégation (somme, moyenne, MAX, MIN, COUNT, STDEV ou toute).</span><span class="sxs-lookup"><span data-stu-id="bd0a0-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>


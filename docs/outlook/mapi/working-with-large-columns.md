---
title: Utilisation de colonnes de grande taille
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325780"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="5ea1f-103">Utilisation de colonnes de grande taille</span><span class="sxs-lookup"><span data-stu-id="5ea1f-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="5ea1f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ea1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ea1f-105">Les colonnes avec des données de propriété binaire ou de chaîne peuvent être volumineuses, voire plusieurs milliers d'octets.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="5ea1f-106">Étant donné que l'inclusion d'une ou plusieurs colonnes avec des centaines d'octets dans une vue est souvent peu pratique, MAPI permet aux implémenteurs de tableau de tronquer la valeur, le plus souvent à 255 octets et moins souvent à 510 octets.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="5ea1f-107">Dans la mesure du possible, les implémenteurs de tableaux doivent inclure la valeur complète d'une propriété dans une colonne de tableau.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="5ea1f-108">L'alternative recommandée consiste à inclure uniquement les premiers 255 octets.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="5ea1f-109">Les clients ne peuvent pas savoir à l'avance si une table qu'ils utilisent tronque des colonnes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="5ea1f-110">Elles doivent supposer qu'une colonne représente une propriété tronquée si la longueur de la colonne est de 255 ou 510 octets.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="5ea1f-111">Si nécessaire, les clients peuvent récupérer directement la valeur complète d'une colonne tronquée à partir de l'objet en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'objet.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="5ea1f-112">Les clients qui créent des restrictions avec des propriétés importantes doivent être conscients du fait que la mise en œuvre de la table est la manière dont ces restrictions fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="5ea1f-113">Certains implémenteurs de tableau permettent à des restrictions créées à l'aide d'une colonne tronquée de se fonder sur la taille tronquée, tandis que d'autres le basent sur la valeur entière.</span><span class="sxs-lookup"><span data-stu-id="5ea1f-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ea1f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ea1f-114">See also</span></span>



[<span data-ttu-id="5ea1f-115">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="5ea1f-115">MAPI Tables</span></span>](mapi-tables.md)


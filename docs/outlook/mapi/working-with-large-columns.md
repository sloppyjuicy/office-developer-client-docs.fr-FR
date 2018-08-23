---
title: Utilisation de colonnes volumineuses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 11007fa18a57e296472c28f86480cb71b780e568
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593031"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="add11-103">Utilisation de colonnes volumineuses</span><span class="sxs-lookup"><span data-stu-id="add11-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="add11-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="add11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="add11-105">Colonnes avec des données de propriété binaire ou chaîne pouvant être volumineux, voire des milliers d’octets.</span><span class="sxs-lookup"><span data-stu-id="add11-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="add11-106">Y compris une ou plusieurs colonnes avec des centaines d’octets dans un affichage est souvent difficile, MAPI permet l’implémentation de la table à tronquer la valeur, la plupart du temps à 255 octets et moins souvent 510 octets.</span><span class="sxs-lookup"><span data-stu-id="add11-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="add11-107">La mesure du possible, l’implémentation de la table doit inclure la valeur complète d’une propriété dans une colonne de table.</span><span class="sxs-lookup"><span data-stu-id="add11-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="add11-108">L’alternative recommandée consiste à inclure uniquement les 255 premiers octets.</span><span class="sxs-lookup"><span data-stu-id="add11-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="add11-109">Les clients ne peut pas savoir à l’avance si une table qu’ils utilisent tronque colonnes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="add11-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="add11-110">Ils doivent supposer qu’une colonne représente une propriété tronquée si la longueur de la colonne est 255 ou 510 octets.</span><span class="sxs-lookup"><span data-stu-id="add11-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="add11-111">Si nécessaire, les clients peuvent directement récupérer la valeur d’une colonne tronquée complète de l’objet en appelant la méthode l’objet [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="add11-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="add11-112">Création des restrictions de grandes propriétés des clients doivent être conscients qu’il est à l’implémentation de la table quant à ces restrictions de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="add11-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="add11-113">Certains programmeurs table autoriser les restrictions qui sont créées avec une colonne tronquée selon la taille tronquée tandis que d’autres personnes selon la valeur entière.</span><span class="sxs-lookup"><span data-stu-id="add11-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="add11-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="add11-114">See also</span></span>



[<span data-ttu-id="add11-115">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="add11-115">MAPI Tables</span></span>](mapi-tables.md)


---
title: À propos des Restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782853"
---
# <a name="about-restrictions"></a><span data-ttu-id="d170a-103">À propos des Restrictions</span><span class="sxs-lookup"><span data-stu-id="d170a-103">About Restrictions</span></span>

  
  
<span data-ttu-id="d170a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d170a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d170a-105">Une restriction est un moyen de limiter le nombre de lignes dans un affichage uniquement aux lignes avec des valeurs pour les colonnes qui correspondent à des critères spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d170a-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="d170a-106">Il existe plusieurs opportunités différentes pour des tableaux à l’aide de restrictions.</span><span class="sxs-lookup"><span data-stu-id="d170a-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="d170a-107">Les applications clientes peuvent utiliser restrictions, par exemple, pour filtrer un tableau de contenu pour les messages envoyés par une personne particulière, pour rechercher des lignes qui ne prennent pas en charge une propriété ou ont défini une propriété à une valeur spécifique, ou pour rechercher des destinataires en double dans un Message.</span><span class="sxs-lookup"><span data-stu-id="d170a-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="d170a-108">Les méthodes [IMAPITable](imapitable-restrict.md) et [IMAPITable::FindRow](imapitable-findrow.md) sont utilisés pour définir des restrictions sur une table.</span><span class="sxs-lookup"><span data-stu-id="d170a-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="d170a-109">**Restrict** applique la restriction à la table sans récupérer toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="d170a-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="d170a-110">Pour récupérer uniquement les lignes qui répondent à la restriction, un appel ultérieur à [IMAPITable::QueryRows](imapitable-queryrows.md) ou une méthode similaire est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d170a-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="d170a-111">**FindRow** applique la restriction et récupère la première ligne dans le tableau qui correspond aux critères.</span><span class="sxs-lookup"><span data-stu-id="d170a-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="d170a-112">**FindRow** applique une restriction temporaire, qui est uniquement à la durée de l’appel, alors que **Restrict** applique une restriction permanente.</span><span class="sxs-lookup"><span data-stu-id="d170a-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="d170a-113">Certains clients peuvent générer une restriction à l’aide de colonnes qui sont définies pas dans la colonne en cours.</span><span class="sxs-lookup"><span data-stu-id="d170a-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="d170a-114">Prise en charge une telle restriction est facultative et l’implémentation de tableau qui prennent en charge ajouter la valeur, en particulier pour les tables des matières.</span><span class="sxs-lookup"><span data-stu-id="d170a-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="d170a-115">L’implémentation de tableau qui ne prennent pas en charge qu’il peut renvoyer la valeur MAPI_E_TOO_COMPLEX à partir d’un appel de **restreindre** ou la valeur MAPI_E_NOT_FOUND à partir d’un appel **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="d170a-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="d170a-116">Les clients doivent être conscient que, même si le fournisseur ne prend pas en charge les restrictions sur les colonnes pas dans le jeu actuel de la colonne, ils obtenir globale de meilleures performances en spécifiant les colonnes qu'ils souhaitent dans leurs restrictions avec [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="d170a-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d170a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d170a-117">See also</span></span>



[<span data-ttu-id="d170a-118">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="d170a-118">MAPI Tables</span></span>](mapi-tables.md)


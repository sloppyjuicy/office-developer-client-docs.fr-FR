---
title: À propos des restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433107"
---
# <a name="about-restrictions"></a><span data-ttu-id="6ca42-103">À propos des restrictions</span><span class="sxs-lookup"><span data-stu-id="6ca42-103">About Restrictions</span></span>

  
  
<span data-ttu-id="6ca42-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ca42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ca42-105">Une restriction permet de limiter le nombre de lignes d'un affichage aux seules lignes dont les valeurs correspondent à des critères spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6ca42-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="6ca42-106">Il existe de nombreuses opportunités différentes pour l'utilisation de restrictions avec des tables.</span><span class="sxs-lookup"><span data-stu-id="6ca42-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="6ca42-107">Les applications clientes peuvent utiliser des restrictions, par exemple, pour filtrer une table de contenu pour les messages envoyés par une personne particulière, pour rechercher des lignes qui ne prennent pas en charge une propriété ou ont défini une propriété sur une valeur spécifique, ou pour rechercher des destinataires en double dans un Message.</span><span class="sxs-lookup"><span data-stu-id="6ca42-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="6ca42-108">Les méthodes [IMAPITable](imapitable-restrict.md) :: Restrict et [IMAPITable:: FindRow](imapitable-findrow.md) permettent de définir des restrictions sur une table.</span><span class="sxs-lookup"><span data-stu-id="6ca42-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="6ca42-109">\*\*\*\* La méthode Restrict applique la restriction à la table sans récupérer de ligne.</span><span class="sxs-lookup"><span data-stu-id="6ca42-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="6ca42-110">Pour récupérer uniquement les lignes qui satisfont à la restriction, un appel suivant à [IMAPITable:: QueryRows](imapitable-queryrows.md) ou une méthode similaire est requise.</span><span class="sxs-lookup"><span data-stu-id="6ca42-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="6ca42-111">**FindRow** applique la restriction et récupère la première ligne du tableau qui correspond aux critères.</span><span class="sxs-lookup"><span data-stu-id="6ca42-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="6ca42-112">**FindRow** applique une restriction temporaire, qui existe uniquement pendant la durée de l'appel, tandis que **restrict** applique une restriction permanente plus permanente.</span><span class="sxs-lookup"><span data-stu-id="6ca42-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="6ca42-113">Certains clients peuvent créer une restriction à l'aide de colonnes qui ne figurent pas dans le jeu de colonnes actuel.</span><span class="sxs-lookup"><span data-stu-id="6ca42-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="6ca42-114">La prise en charge d'une restriction de ce type est facultative et les implémenteurs de tableau qui le prennent en charge ajoutent une valeur ajoutée, en particulier pour les tables des matières.</span><span class="sxs-lookup"><span data-stu-id="6ca42-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="6ca42-115">Les implémenteurs de tableau qui ne le prennent pas en charge peuvent renvoyer la \*\*\*\* valeur MAPI_E_TOO_COMPLEX à partir d'un appel de la propriété restrict ou de la valeur MAPI_E_NOT_FOUND à partir d'un appel **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="6ca42-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="6ca42-116">Les clients doivent savoir que, même si le fournisseur prend en charge les restrictions sur les colonnes qui ne figurent pas dans le jeu de colonnes actuel, il obtiendra de meilleures performances globales en spécifiant les colonnes qu'ils entendent utiliser dans leurs restrictions avec la fonction [IMAPITable:: SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca42-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ca42-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ca42-117">See also</span></span>



[<span data-ttu-id="6ca42-118">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="6ca42-118">MAPI Tables</span></span>](mapi-tables.md)


---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581957"
---
# <a name="ssubrestriction"></a><span data-ttu-id="bea63-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="bea63-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="bea63-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bea63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bea63-105">Décrit une restriction objet secondaire qui permet de filtrer les lignes de pièce jointe ou un tableau de destinataire d’un message.</span><span class="sxs-lookup"><span data-stu-id="bea63-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bea63-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bea63-106">Header file:</span></span>  <br/> |<span data-ttu-id="bea63-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bea63-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="bea63-108">Members</span><span class="sxs-lookup"><span data-stu-id="bea63-108">Members</span></span>

 <span data-ttu-id="bea63-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="bea63-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="bea63-110">Type d’objet secondaire en guise de la cible de la restriction.</span><span class="sxs-lookup"><span data-stu-id="bea63-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="bea63-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bea63-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="bea63-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="bea63-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="bea63-113">Appliquer la restriction à la table des destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="bea63-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="bea63-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="bea63-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="bea63-115">Appliquer la restriction à la table des pièces jointes d’un message.</span><span class="sxs-lookup"><span data-stu-id="bea63-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="bea63-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="bea63-116">**lpRes**</span></span>
  
> <span data-ttu-id="bea63-117">Pointeur vers une structure [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="bea63-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bea63-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="bea63-118">Remarks</span></span>

<span data-ttu-id="bea63-119">Restrictions de l’objet sous-fonctionnalités ne sont pas pris en charge par toutes les tables.</span><span class="sxs-lookup"><span data-stu-id="bea63-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="bea63-120">En règle générale, uniquement le dossier contenu tables et dossiers de résultats de recherche les prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="bea63-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="bea63-121">Par exemple, restrictions de l’objet sous-sites sont utilisées pour rechercher un message qui a un type particulier de pièce jointe ou un destinataire.</span><span class="sxs-lookup"><span data-stu-id="bea63-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="bea63-122">Si une implémentation ne gère pas les restrictions de l’objet secondaire, elle renvoie MAPI_E_TOO_COMPLEX à partir de ses méthodes [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="bea63-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="bea63-123">Pour une présentation générale du fonctionnement des restrictions, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bea63-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bea63-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bea63-124">See also</span></span>



[<span data-ttu-id="bea63-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bea63-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="bea63-126">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="bea63-126">MAPI Structures</span></span>](mapi-structures.md)


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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406324"
---
# <a name="ssubrestriction"></a><span data-ttu-id="79284-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="79284-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="79284-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79284-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79284-105">Décrit une restriction de sous-objet qui est utilisée pour filtrer les lignes de la table de destinataires ou de la table de destinataires d'un message.</span><span class="sxs-lookup"><span data-stu-id="79284-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79284-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="79284-106">Header file:</span></span>  <br/> |<span data-ttu-id="79284-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="79284-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="79284-108">Members</span><span class="sxs-lookup"><span data-stu-id="79284-108">Members</span></span>

 <span data-ttu-id="79284-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="79284-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="79284-110">Type de sous-objet servant de cible pour la restriction.</span><span class="sxs-lookup"><span data-stu-id="79284-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="79284-111">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="79284-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="79284-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="79284-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="79284-113">Appliquer la restriction à la table de destinataires d'un message.</span><span class="sxs-lookup"><span data-stu-id="79284-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="79284-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="79284-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="79284-115">Appliquer la restriction à la table des pièces jointes d'un message.</span><span class="sxs-lookup"><span data-stu-id="79284-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="79284-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="79284-116">**lpRes**</span></span>
  
> <span data-ttu-id="79284-117">Pointeur vers une structure [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="79284-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="79284-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="79284-118">Remarks</span></span>

<span data-ttu-id="79284-119">Les restrictions de sous-objet ne sont pas prises en charge par toutes les tables.</span><span class="sxs-lookup"><span data-stu-id="79284-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="79284-120">En règle générale, seules les tables de contenu de dossier et les dossiers de résultats de recherche les prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="79284-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="79284-121">Par exemple, des restrictions de sous-objet sont utilisées pour rechercher un message comportant un type particulier de pièce jointe ou de destinataire.</span><span class="sxs-lookup"><span data-stu-id="79284-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="79284-122">Si une implémentation ne prend pas en charge les restrictions de sous-objet, elle renvoie MAPI_E_TOO_COMPLEX à partir de ses méthodes [IMAPITable](imapitable-restrict.md) :: restrict ou [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="79284-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="79284-123">Pour plus d'informations sur le fonctionnement des restrictions, consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="79284-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79284-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79284-124">See also</span></span>



[<span data-ttu-id="79284-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="79284-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="79284-126">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="79284-126">MAPI Structures</span></span>](mapi-structures.md)


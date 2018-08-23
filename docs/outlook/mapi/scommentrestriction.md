---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589181"
---
# <a name="scommentrestriction"></a><span data-ttu-id="9e295-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="9e295-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="9e295-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e295-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e295-105">Décrit une restriction de commentaire, qui sert à annoter une restriction.</span><span class="sxs-lookup"><span data-stu-id="9e295-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e295-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9e295-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e295-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e295-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="9e295-108">Members</span><span class="sxs-lookup"><span data-stu-id="9e295-108">Members</span></span>

 <span data-ttu-id="9e295-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9e295-109">**cValues**</span></span>
  
> <span data-ttu-id="9e295-110">Nombre de valeurs de propriété dans le tableau indiqué par le membre **lpProp** .</span><span class="sxs-lookup"><span data-stu-id="9e295-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="9e295-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="9e295-111">**lpRes**</span></span>
  
> <span data-ttu-id="9e295-112">Pointeur vers une structure [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="9e295-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="9e295-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="9e295-113">**lpProp**</span></span>
  
> <span data-ttu-id="9e295-114">Pointeur vers un tableau de structures [SPropValue](spropvalue.md) , chacun contenant la balise de propriété et la valeur d’une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="9e295-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e295-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e295-115">Remarks</span></span>

<span data-ttu-id="9e295-116">La structure **SCommentRestriction** associe un objet avec un ensemble de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="9e295-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="9e295-117">Restrictions de commentaire sont Contrairement à d’autres restrictions, car ils ne sont pas évaluées.</span><span class="sxs-lookup"><span data-stu-id="9e295-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="9e295-118">Autrement dit, ils sont ignorés par la méthode [IMAPITable](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="9e295-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="9e295-119">Il n’existe aucun effet sur les lignes renvoyées par la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un appel **IMAPITable** a été effectué.</span><span class="sxs-lookup"><span data-stu-id="9e295-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="9e295-120">La structure **SCommentRestriction** peut être utilisée pour conserver les informations spécifiques à l’application avec une restriction lorsqu’il est enregistré sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9e295-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="9e295-121">Par exemple, un client de l’enregistrement du nom d’une propriété nommée utilisé dans une restriction de propriété permettre le faire dans une structure **SCommentRestriction** .</span><span class="sxs-lookup"><span data-stu-id="9e295-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="9e295-122">L’enregistrement d’un nom de propriété n’est pas possible dans une restriction de propriété car la structure [SPropertyRestriction](spropertyrestriction.md) associée conserve uniquement la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="9e295-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="9e295-123">Pour plus d’informations sur les restrictions de structure **SCommentRestriction** en général, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="9e295-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e295-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e295-124">See also</span></span>



[<span data-ttu-id="9e295-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9e295-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9e295-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9e295-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="9e295-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="9e295-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="9e295-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9e295-128">MAPI Structures</span></span>](mapi-structures.md)


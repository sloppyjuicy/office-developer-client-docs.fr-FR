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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430608"
---
# <a name="scommentrestriction"></a><span data-ttu-id="237b8-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="237b8-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="237b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="237b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="237b8-105">Décrit une restriction de commentaire, qui est utilisée pour annoter une restriction.</span><span class="sxs-lookup"><span data-stu-id="237b8-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="237b8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="237b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="237b8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="237b8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="237b8-108">Members</span><span class="sxs-lookup"><span data-stu-id="237b8-108">Members</span></span>

 <span data-ttu-id="237b8-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="237b8-109">**cValues**</span></span>
  
> <span data-ttu-id="237b8-110">Nombre de valeurs de propriété dans le tableau pointé par **le membre lpProp.**</span><span class="sxs-lookup"><span data-stu-id="237b8-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="237b8-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="237b8-111">**lpRes**</span></span>
  
> <span data-ttu-id="237b8-112">Pointeur vers une structure [SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="237b8-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="237b8-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="237b8-113">**lpProp**</span></span>
  
> <span data-ttu-id="237b8-114">Pointeur vers un tableau de structures [SPropValue,](spropvalue.md) chacune contenant la balise de propriété et la valeur d’une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="237b8-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="237b8-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="237b8-115">Remarks</span></span>

<span data-ttu-id="237b8-116">La structure **SCommentRestriction** associe un objet à un ensemble de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="237b8-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="237b8-117">Les restrictions de commentaire sont contrairement aux autres restrictions, car elles ne sont pas évaluées.</span><span class="sxs-lookup"><span data-stu-id="237b8-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="237b8-118">Autrement dit, ils sont ignorés par la [méthode IMAPITable::Restrict.](imapitable-restrict.md)</span><span class="sxs-lookup"><span data-stu-id="237b8-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="237b8-119">Il n’y a aucun effet sur les lignes renvoyées par la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un **appel IMAPITable::Restrict** a été effectué.</span><span class="sxs-lookup"><span data-stu-id="237b8-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="237b8-120">La structure **SCommentRestriction** peut être utilisée pour conserver des informations spécifiques à l’application avec une restriction lorsqu’elle est enregistrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="237b8-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="237b8-121">Par exemple, un client qui sauvegarde le nom d’une propriété nommée utilisée dans une restriction de propriété peut le faire dans une structure **SCommentRestriction.**</span><span class="sxs-lookup"><span data-stu-id="237b8-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="237b8-122">L’enregistrement d’un nom de propriété n’est pas possible dans une restriction de propriété, car la structure [SPropertyRestriction](spropertyrestriction.md) associée contient uniquement la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="237b8-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="237b8-123">Pour plus d’informations sur la structure et les **restrictions SCommentRestriction** en général, voir [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="237b8-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="237b8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="237b8-124">See also</span></span>



[<span data-ttu-id="237b8-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="237b8-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="237b8-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="237b8-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="237b8-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="237b8-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="237b8-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="237b8-128">MAPI Structures</span></span>](mapi-structures.md)


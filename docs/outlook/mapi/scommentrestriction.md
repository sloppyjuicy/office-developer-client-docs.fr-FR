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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351414"
---
# <a name="scommentrestriction"></a><span data-ttu-id="5c5cd-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="5c5cd-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="5c5cd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c5cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c5cd-105">Décrit une restriction de commentaire, utilisée pour annoter une restriction.</span><span class="sxs-lookup"><span data-stu-id="5c5cd-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c5cd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5c5cd-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c5cd-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5c5cd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="5c5cd-108">Members</span><span class="sxs-lookup"><span data-stu-id="5c5cd-108">Members</span></span>

 <span data-ttu-id="5c5cd-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="5c5cd-109">**cValues**</span></span>
  
> <span data-ttu-id="5c5cd-110">Nombre de valeurs de propriété dans le tableau vers lequel pointe le membre **lpProp** .</span><span class="sxs-lookup"><span data-stu-id="5c5cd-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="5c5cd-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="5c5cd-111">**lpRes**</span></span>
  
> <span data-ttu-id="5c5cd-112">Pointeur vers une structure [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5cd-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="5c5cd-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="5c5cd-113">**lpProp**</span></span>
  
> <span data-ttu-id="5c5cd-114">Pointeur vers un tableau de structures [SPropValue](spropvalue.md) , chacune contenant la balise de propriété et la valeur d'une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="5c5cd-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c5cd-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c5cd-115">Remarks</span></span>

<span data-ttu-id="5c5cd-116">La structure **SCommentRestriction** associe un objet à un ensemble de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="5c5cd-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="5c5cd-117">Les restrictions de commentaire sont à la différence des autres restrictions car elles ne sont pas évaluées.</span><span class="sxs-lookup"><span data-stu-id="5c5cd-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="5c5cd-118">Autrement dit, ils sont ignorés par la méthode [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5cd-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="5c5cd-119">Il n'y a aucun effet sur les lignes renvoyées par la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) après l'appel de la méthode IMAPITable: **: Restrict** .</span><span class="sxs-lookup"><span data-stu-id="5c5cd-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="5c5cd-120">La structure **SCommentRestriction** peut être utilisée pour conserver les informations spécifiques à l'application à l'aide d'une restriction lorsqu'elle est enregistrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="5c5cd-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="5c5cd-121">Par exemple, un client enregistrant le nom d'une propriété nommée utilisée dans une restriction de propriété peut le faire dans une structure **SCommentRestriction** .</span><span class="sxs-lookup"><span data-stu-id="5c5cd-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="5c5cd-122">L'enregistrement d'un nom de propriété n'est pas possible dans une restriction de propriété car la structure [SPropertyRestriction](spropertyrestriction.md) associée contient uniquement la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="5c5cd-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="5c5cd-123">Pour plus d'informations sur la structure **SCommentRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5c5cd-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c5cd-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c5cd-124">See also</span></span>



[<span data-ttu-id="5c5cd-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5c5cd-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5c5cd-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5c5cd-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="5c5cd-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="5c5cd-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="5c5cd-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="5c5cd-128">MAPI Structures</span></span>](mapi-structures.md)


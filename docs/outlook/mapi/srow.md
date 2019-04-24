---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336514"
---
# <a name="srow"></a><span data-ttu-id="62913-103">SRow</span><span class="sxs-lookup"><span data-stu-id="62913-103">SRow</span></span>

<span data-ttu-id="62913-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62913-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62913-105">Décrit une ligne d'une table qui contient les propriétés sélectionnées d'un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="62913-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62913-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="62913-106">Header file:</span></span>  <br/> |<span data-ttu-id="62913-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="62913-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="62913-108">Members</span><span class="sxs-lookup"><span data-stu-id="62913-108">Members</span></span>

<span data-ttu-id="62913-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="62913-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="62913-110">Octets de remplissage pour aligner correctement les valeurs de propriété vers lesquelles pointe le membre **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="62913-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="62913-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="62913-111">**cValues**</span></span>
  
> <span data-ttu-id="62913-112">Nombre de valeurs de propriétés vers lesquelles pointe **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="62913-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="62913-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="62913-113">**lpProps**</span></span>
  
> <span data-ttu-id="62913-114">Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui décrivent les valeurs des propriétés des colonnes de la ligne.</span><span class="sxs-lookup"><span data-stu-id="62913-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="62913-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="62913-115">Remarks</span></span>

<span data-ttu-id="62913-116">Une structure **SRow** décrit une ligne d'un tableau.</span><span class="sxs-lookup"><span data-stu-id="62913-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="62913-117">Elle est incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) qui accompagne une notification de table.</span><span class="sxs-lookup"><span data-stu-id="62913-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="62913-118">Les structures **SRow** sont utilisées dans les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="62913-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="62913-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="62913-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="62913-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="62913-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="62913-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="62913-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="62913-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="62913-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="62913-123">[ITableData: IUnknown](itabledataiunknown.md) (nombreuses méthodes)</span><span class="sxs-lookup"><span data-stu-id="62913-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="62913-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="62913-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="62913-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="62913-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="62913-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="62913-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="62913-127">Lorsque plusieurs lignes doivent être décrites, une structure [SRowSet](srowset.md) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="62913-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="62913-128">Une structure **SRowSet** contient un tableau de structures **SRow** et un nombre de structures dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="62913-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="62913-129">L'illustration suivante montre la relation entre une structure de données **SRow** et **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="62913-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="62913-130">**Relation entre SRow et SRowSet**</span><span class="sxs-lookup"><span data-stu-id="62913-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="62913-131">![Relation entre SRow et SRowSet] (media/amapi_17.gif "Relation entre SRow et SRowSet")</span><span class="sxs-lookup"><span data-stu-id="62913-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="62913-132">Les structures **SRow** sont définies de la même manière que les structures [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="62913-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="62913-133">Par conséquent, une ligne d'une table de destinataires et une entrée dans une liste d'adresses peuvent être traitées de la même façon.</span><span class="sxs-lookup"><span data-stu-id="62913-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="62913-134">Pour plus d'informations sur la façon dont la mémoire des structures **SRow** doit être allouée, consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="62913-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="62913-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62913-135">See also</span></span>

- [<span data-ttu-id="62913-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="62913-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="62913-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="62913-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="62913-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="62913-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="62913-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="62913-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="62913-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="62913-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="62913-141">Gestion de la mémoire pour les structures ADRLIST et SRowSet</span><span class="sxs-lookup"><span data-stu-id="62913-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)


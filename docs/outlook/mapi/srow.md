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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579122"
---
# <a name="srow"></a><span data-ttu-id="a15e9-103">SRow</span><span class="sxs-lookup"><span data-stu-id="a15e9-103">SRow</span></span>

<span data-ttu-id="a15e9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a15e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a15e9-105">Décrit une ligne d’un tableau qui contient les propriétés sélectionnées pour un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="a15e9-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a15e9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a15e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="a15e9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a15e9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="a15e9-108">Members</span><span class="sxs-lookup"><span data-stu-id="a15e9-108">Members</span></span>

<span data-ttu-id="a15e9-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="a15e9-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="a15e9-110">Octets pour aligner correctement les valeurs des propriétés de remplissage vers laquelle pointe le membre **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="a15e9-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="a15e9-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a15e9-111">**cValues**</span></span>
  
> <span data-ttu-id="a15e9-112">Nombre de valeurs de propriété désignés par **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="a15e9-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="a15e9-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="a15e9-113">**lpProps**</span></span>
  
> <span data-ttu-id="a15e9-114">Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui décrivent les valeurs de propriété pour les colonnes de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a15e9-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a15e9-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a15e9-115">Remarks</span></span>

<span data-ttu-id="a15e9-116">Une structure **SRow** décrit une ligne dans une table.</span><span class="sxs-lookup"><span data-stu-id="a15e9-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="a15e9-117">Il est inclus dans la structure [TABLE_NOTIFICATION](table_notification.md) qui accompagne une notification de la table.</span><span class="sxs-lookup"><span data-stu-id="a15e9-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="a15e9-118">Structures **SRow** sont utilisés dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a15e9-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="a15e9-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="a15e9-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="a15e9-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="a15e9-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="a15e9-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a15e9-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="a15e9-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="a15e9-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="a15e9-123">[ITableData : IUnknown](itabledataiunknown.md) (de nombreuses méthodes)</span><span class="sxs-lookup"><span data-stu-id="a15e9-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="a15e9-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="a15e9-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="a15e9-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="a15e9-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="a15e9-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="a15e9-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="a15e9-127">Lorsque plusieurs lignes doit être indiqué, une structure [SRowSet](srowset.md) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a15e9-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="a15e9-128">Une structure **SRowSet** contient un tableau de structures **SRow** et le nombre de structures dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a15e9-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="a15e9-129">L’illustration suivante montre la relation entre un **SRow** et une structure de données **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="a15e9-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="a15e9-130">**Relation entre SRow et SRowSet**</span><span class="sxs-lookup"><span data-stu-id="a15e9-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="a15e9-131">![Relation entre SRow et SRowSet] (media/amapi_17.gif "Relation entre SRow et SRowSet")</span><span class="sxs-lookup"><span data-stu-id="a15e9-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="a15e9-132">Structures **SRow** sont définies les mêmes en tant que structures [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="a15e9-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="a15e9-133">Par conséquent, une ligne d’une table de destinataires et une entrée dans une liste d’adresses peut être traité.</span><span class="sxs-lookup"><span data-stu-id="a15e9-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="a15e9-134">Pour plus d’informations sur comment d’allouer de la mémoire pour les structures **SRow** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="a15e9-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a15e9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a15e9-135">See also</span></span>

- [<span data-ttu-id="a15e9-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="a15e9-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="a15e9-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a15e9-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="a15e9-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="a15e9-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="a15e9-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a15e9-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="a15e9-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="a15e9-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="a15e9-141">Gestion de la mémoire pour les structures ADRLIST et SRowSet</span><span class="sxs-lookup"><span data-stu-id="a15e9-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)


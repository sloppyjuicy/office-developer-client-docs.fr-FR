---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787263"
---
# <a name="srowset"></a><span data-ttu-id="0e2ea-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="0e2ea-103">SRowSet</span></span>

  
  
<span data-ttu-id="0e2ea-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e2ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e2ea-105">Contient un tableau de structures [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="0e2ea-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="0e2ea-106">Chaque structure **SRow** décrit une ligne d’une table.</span><span class="sxs-lookup"><span data-stu-id="0e2ea-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e2ea-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0e2ea-107">Header file:</span></span>  <br/> |<span data-ttu-id="0e2ea-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e2ea-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0e2ea-109">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="0e2ea-109">Related macros:</span></span>  <br/> |<span data-ttu-id="0e2ea-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="0e2ea-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="0e2ea-111">Membres</span><span class="sxs-lookup"><span data-stu-id="0e2ea-111">Members</span></span>

 <span data-ttu-id="0e2ea-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="0e2ea-112">**cRows**</span></span>
  
> <span data-ttu-id="0e2ea-113">Nombre de structures **SRow** dans le membre **: UGAL** .</span><span class="sxs-lookup"><span data-stu-id="0e2ea-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="0e2ea-114">**: UGAL**</span><span class="sxs-lookup"><span data-stu-id="0e2ea-114">**aRow**</span></span>
  
> <span data-ttu-id="0e2ea-115">Tableau de structures **SRow** .</span><span class="sxs-lookup"><span data-stu-id="0e2ea-115">Array of **SRow** structures.</span></span> <span data-ttu-id="0e2ea-116">Il existe une structure pour chaque ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="0e2ea-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e2ea-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e2ea-117">Remarks</span></span>

<span data-ttu-id="0e2ea-118">Une structure **SRowSet** est utilisée pour décrire plusieurs lignes de données d’une table.</span><span class="sxs-lookup"><span data-stu-id="0e2ea-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="0e2ea-119">Structures **SRowSet** sont utilisés dans les méthodes d’interface [IMAPITable](imapitableiunknown.md) [IAddrBook](iaddrbookimapiprop.md)et [ITableData](itabledataiunknown.md), outre les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e2ea-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="0e2ea-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="0e2ea-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="0e2ea-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="0e2ea-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="0e2ea-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="0e2ea-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="0e2ea-123">Les structures **SRowSet** sont définis la même que celle des structures [ADRLIST](adrlist.md) pour autoriser les lignes d’une table de destinataires et les entrées dans une liste d’adresses pour être traités de la même.</span><span class="sxs-lookup"><span data-stu-id="0e2ea-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="0e2ea-124">Les structures **SRowSet** et **ADRLIST** peuvent être transmis aux méthodes telles que [IMessage::ModifyRecipients](imessage-modifyrecipients.md) et [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="0e2ea-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="0e2ea-125">En outre, les règles pour l’allocation de mémoire pour les structures **SRowSet** sont les mêmes que pour les structures **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="0e2ea-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="0e2ea-126">Pour résumer, chaque structure [SPropValue](spropvalue.md) dans le tableau de pointe pour définir les par le membre **lpProps** de chaque ligne dans la ligne doit être alloué séparément à l’aide de [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0e2ea-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="0e2ea-127">Chaque structure de valeur de propriété doit également être libérée à l’aide de [MAPIFreeBuffer](mapifreebuffer.md) avant la libération de sa structure **SRowSet** afin que des pointeurs vers les structures **SPropValue** alloués ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="0e2ea-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="0e2ea-128">Une ligne d’allouée mémoire peuvent être conservée puis réutilisée en dehors du contexte de la structure **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="0e2ea-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="0e2ea-129">Pour plus d’informations sur comment d’allouer de la mémoire pour les structures **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="0e2ea-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e2ea-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e2ea-130">See also</span></span>



[<span data-ttu-id="0e2ea-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="0e2ea-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="0e2ea-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0e2ea-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="0e2ea-133">SRow</span><span class="sxs-lookup"><span data-stu-id="0e2ea-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="0e2ea-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0e2ea-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0e2ea-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0e2ea-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="0e2ea-136">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="0e2ea-136">MAPI Structures</span></span>](mapi-structures.md)


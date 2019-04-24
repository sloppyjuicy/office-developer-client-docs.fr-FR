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
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341635"
---
# <a name="srowset"></a><span data-ttu-id="8e707-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="8e707-103">SRowSet</span></span>

  
  
<span data-ttu-id="8e707-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e707-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e707-105">Contient un tableau de structures [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="8e707-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="8e707-106">Chaque structure **SRow** décrit une ligne d'une table.</span><span class="sxs-lookup"><span data-stu-id="8e707-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e707-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8e707-107">Header file:</span></span>  <br/> |<span data-ttu-id="8e707-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8e707-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8e707-109">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="8e707-109">Related macros:</span></span>  <br/> |<span data-ttu-id="8e707-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="8e707-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="8e707-111">Members</span><span class="sxs-lookup"><span data-stu-id="8e707-111">Members</span></span>

 <span data-ttu-id="8e707-112">**Pattes**</span><span class="sxs-lookup"><span data-stu-id="8e707-112">**cRows**</span></span>
  
> <span data-ttu-id="8e707-113">Nombre de structures **SRow** dans le membre **aRow** .</span><span class="sxs-lookup"><span data-stu-id="8e707-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="8e707-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="8e707-114">**aRow**</span></span>
  
> <span data-ttu-id="8e707-115">Tableau de structures **SRow** .</span><span class="sxs-lookup"><span data-stu-id="8e707-115">Array of **SRow** structures.</span></span> <span data-ttu-id="8e707-116">Il existe une structure pour chaque ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8e707-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e707-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e707-117">Remarks</span></span>

<span data-ttu-id="8e707-118">Une structure **SRowSet** est utilisée pour décrire plusieurs lignes de données d'un tableau.</span><span class="sxs-lookup"><span data-stu-id="8e707-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="8e707-119">Les structures **SRowSet** sont utilisées dans les méthodes d'interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)et [IMAPITable](imapitableiunknown.md) , en plus des fonctions suivantes:</span><span class="sxs-lookup"><span data-stu-id="8e707-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="8e707-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="8e707-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="8e707-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="8e707-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="8e707-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="8e707-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="8e707-123">Les structures **SRowSet** sont définies de la même façon que les structures [ADRLIST](adrlist.md) pour permettre aux lignes d'une table de destinataires et aux entrées d'une liste d'adresses d'être traitées de la même manière.</span><span class="sxs-lookup"><span data-stu-id="8e707-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="8e707-124">Les structures **SRowSet** et **ADRLIST** peuvent être transmises à des méthodes telles que [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) et [IAddrBook:: Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="8e707-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="8e707-125">En outre, les règles d'allocation de mémoire pour les structures **SRowSet** sont les mêmes que pour les structures **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="8e707-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="8e707-126">Pour résumer, chaque structure [SPropValue](spropvalue.md) dans le tableau vers lequel pointe le membre **lpProps** de chaque ligne du jeu de lignes doit être allouée séparément à l'aide de [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="8e707-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="8e707-127">Chaque structure de valeur de propriété doit également être désallouée à l'aide de [MAPIFreeBuffer](mapifreebuffer.md) avant la désaffectation de sa structure **SRowSet** afin que les pointeurs vers les structures **SPropValue** allouées ne soient pas perdues.</span><span class="sxs-lookup"><span data-stu-id="8e707-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="8e707-128">La mémoire allouée d'une ligne peut ensuite être conservée et réutilisée en dehors du contexte de la structure **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="8e707-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="8e707-129">Pour plus d'informations sur la façon dont la mémoire des structures **SRowSet** doit être allouée, consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="8e707-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e707-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e707-130">See also</span></span>



[<span data-ttu-id="8e707-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="8e707-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="8e707-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e707-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8e707-133">SRow</span><span class="sxs-lookup"><span data-stu-id="8e707-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8e707-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8e707-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8e707-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e707-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="8e707-136">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8e707-136">MAPI Structures</span></span>](mapi-structures.md)


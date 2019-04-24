---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330242"
---
# <a name="adrlist"></a><span data-ttu-id="c1af0-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c1af0-103">ADRLIST</span></span>

<span data-ttu-id="c1af0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1af0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1af0-105">Décrit zéro ou plusieurs propriétés qui appartiennent à un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="c1af0-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1af0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c1af0-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1af0-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c1af0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c1af0-108">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="c1af0-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c1af0-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="c1af0-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="c1af0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c1af0-110">Members</span></span>

<span data-ttu-id="c1af0-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="c1af0-111">**cEntries**</span></span>
  
> <span data-ttu-id="c1af0-112">Nombre d'entrées dans le tableau spécifié par le membre **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="c1af0-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="c1af0-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="c1af0-113">**aEntries**</span></span>
  
> <span data-ttu-id="c1af0-114">Tableau de structures [ADRENTRY](adrentry.md) , une structure pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="c1af0-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c1af0-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1af0-115">Remarks</span></span>

<span data-ttu-id="c1af0-116">Une structure **ADRLIST** contient une ou plusieurs structures **ADRENTRY** , chacune décrivant les propriétés d'un destinataire.</span><span class="sxs-lookup"><span data-stu-id="c1af0-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="c1af0-117">Un destinataire peut être non résolu.</span><span class="sxs-lookup"><span data-stu-id="c1af0-117">A recipient can be unresolved.</span></span> <span data-ttu-id="c1af0-118">Cela signifie qu'il manque un identificateur d'entrée dans le tableau des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="c1af0-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="c1af0-119">Un destinataire résolu signifie que la **propriété\_PR EntryID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse.</span><span class="sxs-lookup"><span data-stu-id="c1af0-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="c1af0-120">En règle générale, les destinataires résolus ont également une adresse de messagerie de la propriété **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c1af0-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="c1af0-121">Toutefois, l'adresse de messagerie n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c1af0-121">However, the email address is not required.</span></span> <span data-ttu-id="c1af0-122">Les structures **ADRLIST** sont utilisées, par exemple, pour décrire la liste des destinataires d'un message sortant et MAPI pour afficher les entrées du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c1af0-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="c1af0-123">Les structures **ADRLIST** ressemblent aux structures [SRowSet](srowset.md) les structures utilisées pour représenter les lignes dans les tableaux.</span><span class="sxs-lookup"><span data-stu-id="c1af0-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="c1af0-124">En fait, ces deux structures sont conçues de manière à ce qu'elles puissent être utilisées indifféremment.</span><span class="sxs-lookup"><span data-stu-id="c1af0-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="c1af0-125">Elles contiennent toutes deux un tableau de structures décrivant un groupe de propriétés et un nombre de valeurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="c1af0-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="c1af0-126">Contrairement à la structure **ADRLIST** , le tableau contient des structures [ADRENTRY](adrentry.md) , dans la structure **SRowSet** , le tableau contient des structures [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="c1af0-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="c1af0-127">Les structures **ADRENTRY** et **SRow** sont identiques dans la mise en page.</span><span class="sxs-lookup"><span data-stu-id="c1af0-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="c1af0-128">Étant donné que les structures **ADRLIST** et **SRowSet** suivent les mêmes règles d'allocation, une structure **SRowSet** extraite de la table de contenu d'un conteneur de carnet d'adresses peut être convertie en une structure **ADRLIST** et utilisée comme c'est le cas.</span><span class="sxs-lookup"><span data-stu-id="c1af0-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="c1af0-129">L'illustration suivante montre la disposition d'une structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="c1af0-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="c1af0-130">**Composants ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="c1af0-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="c1af0-131">![Composants ADRLIST] (media/amapi_18.gif "Composants ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="c1af0-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="c1af0-132">Les parties **ADRENTRY** et [SPropValue](spropvalue.md) dans une structure **ADRLIST** doivent être allouées et libérées indépendamment des autres parties.</span><span class="sxs-lookup"><span data-stu-id="c1af0-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="c1af0-133">Autrement dit, chaque structure **SPropValue** doit être allouée individuellement après que la mémoire de la structure **ADRENTRY** a été allouée et libérée avant la libération de la structure **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="c1af0-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="c1af0-134">Cette indépendance dans la gestion de la mémoire permet aux destinataires et aux propriétés des destinataires d'être librement ajoutés ou supprimés de la liste d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c1af0-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="c1af0-135">Les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) doivent être utilisées pour allouer et libérer la structure **ADRLIST** et tous ses composants.</span><span class="sxs-lookup"><span data-stu-id="c1af0-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="c1af0-136">Si une liste de destinataires est trop volumineuse pour tenir dans la mémoire, les clients peuvent appeler la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) pour fonctionner avec un sous-ensemble de la liste.</span><span class="sxs-lookup"><span data-stu-id="c1af0-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="c1af0-137">Dans ce cas, les clients ne doivent pas utiliser les boîtes de dialogue communes du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c1af0-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="c1af0-138">Pour plus d'informations sur la façon d'allouer de la mémoire aux structures **ADRENTRY** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="c1af0-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1af0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1af0-139">See also</span></span>

- [<span data-ttu-id="c1af0-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c1af0-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="c1af0-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="c1af0-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="c1af0-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c1af0-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="c1af0-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="c1af0-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="c1af0-144">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c1af0-144">MAPI Structures</span></span>](mapi-structures.md)


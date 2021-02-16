---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421437"
---
# <a name="adrentry"></a><span data-ttu-id="a4717-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="a4717-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="a4717-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4717-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4717-105">Décrit zéro ou plusieurs propriétés appartenant à un destinataire.</span><span class="sxs-lookup"><span data-stu-id="a4717-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4717-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a4717-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4717-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4717-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="a4717-108">Members</span><span class="sxs-lookup"><span data-stu-id="a4717-108">Members</span></span>

 <span data-ttu-id="a4717-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="a4717-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="a4717-110">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a4717-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a4717-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a4717-111">**cValues**</span></span>
  
> <span data-ttu-id="a4717-112">Nombre de propriétés dans le tableau des valeurs de propriétés pointées par le **membre rgPropVals.**</span><span class="sxs-lookup"><span data-stu-id="a4717-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="a4717-113">Le **membre cValues** peut être zéro.</span><span class="sxs-lookup"><span data-stu-id="a4717-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="a4717-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="a4717-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="a4717-115">Pointeur vers un tableau de valeurs de propriété décrivant les propriétés du destinataire.</span><span class="sxs-lookup"><span data-stu-id="a4717-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="a4717-116">Le **membre rgPropVals peut** être NULL.</span><span class="sxs-lookup"><span data-stu-id="a4717-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a4717-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4717-117">Remarks</span></span>

<span data-ttu-id="a4717-118">Une **structure ADRENTRY** décrit les propriétés qui appartiennent à un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="a4717-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="a4717-119">Les propriétés généralement utilisées pour décrire un destinataire sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4717-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="a4717-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a4717-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="a4717-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a4717-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="a4717-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a4717-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="a4717-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a4717-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="a4717-124">Lorsqu’un identificateur **d’entrée** ou PR_ENTRYID propriété s’affiche dans le tableau [SPropValue](spropvalue.md) d’un destinataire, cela indique que le destinataire a été résolu.</span><span class="sxs-lookup"><span data-stu-id="a4717-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="a4717-125">Les clients appellent la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour s’assurer que tous les destinataires de la liste des destinataires d’un message sortant ont été résolus.</span><span class="sxs-lookup"><span data-stu-id="a4717-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="a4717-126">Seuls les destinataires résolus peuvent être envoyés avec des messages.</span><span class="sxs-lookup"><span data-stu-id="a4717-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="a4717-127">Les structures **ADRENTRY** sont généralement combinées pour former un tableau pour le membre **aEntries** d’une structure [ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="a4717-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="a4717-128">Les structures **ADRENTRY** et [SRow](srow.md) sont identiques, car elles contiennent toutes deux un membre réservé, un tableau de valeurs de propriétés et un nombre de valeurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a4717-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="a4717-129">Tandis que les structures **ADRENTRY** sont combinées pour former le membre **aEntries** d’une structure **ADRLIST,** les structures **SRow** sont combinées pour former le membre **aRow** d’une structure [SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="a4717-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="a4717-130">Les deux types de structures suivent les mêmes règles d’allocation, ce qui signifie qu’une structure **SRowSet** récupérée à partir de la table des matières d’un conteneur de carnet d’adresses peut être castée vers une structure **ADRLIST** et utilisée telle qu’elle est.</span><span class="sxs-lookup"><span data-stu-id="a4717-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="a4717-131">Une **structure ADRENTRY** peut être vide.</span><span class="sxs-lookup"><span data-stu-id="a4717-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="a4717-132">Par exemple, une structure **ADRENTRY** contenue dans la structure **ADRLIST** pointée par le paramètre  _lppAdrList_ dans un appel à **IAddrBook::Address** peut être vide lorsqu’un destinataire est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a4717-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="a4717-133">Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRENTRY,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="a4717-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a4717-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4717-134">See also</span></span>



[<span data-ttu-id="a4717-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="a4717-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="a4717-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="a4717-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="a4717-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a4717-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a4717-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="a4717-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="a4717-139">SRow</span><span class="sxs-lookup"><span data-stu-id="a4717-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="a4717-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="a4717-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="a4717-141">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="a4717-141">MAPI Structures</span></span>](mapi-structures.md)


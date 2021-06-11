---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412974"
---
# <a name="flaglist"></a><span data-ttu-id="e6d79-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="e6d79-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="e6d79-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6d79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6d79-105">Contient une liste d’indicateurs utilisés pour indiquer l’état des entrées d’adresse pendant le processus de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="e6d79-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6d79-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e6d79-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6d79-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6d79-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="e6d79-108">Members</span><span class="sxs-lookup"><span data-stu-id="e6d79-108">Members</span></span>

 <span data-ttu-id="e6d79-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="e6d79-109">**cFlags**</span></span>
  
> <span data-ttu-id="e6d79-110">Nombre d’indicateurs définis par MAPI dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e6d79-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="e6d79-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e6d79-111">**ulFlags**</span></span>
  
> <span data-ttu-id="e6d79-112">Tableau d’indicateurs qui fournit l’état de l’opération de résolution de noms pour un destinataire.</span><span class="sxs-lookup"><span data-stu-id="e6d79-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="e6d79-113">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="e6d79-113">The following flags can be set:</span></span>
    
<span data-ttu-id="e6d79-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="e6d79-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="e6d79-115">Le destinataire a été résolu, mais pas en un identificateur d’entrée unique.</span><span class="sxs-lookup"><span data-stu-id="e6d79-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="e6d79-116">Les autres conteneurs de carnet d’adresses ne doivent pas essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="e6d79-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="e6d79-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="e6d79-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="e6d79-118">Le destinataire a été résolu en un identificateur d’entrée unique.</span><span class="sxs-lookup"><span data-stu-id="e6d79-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="e6d79-119">Les autres conteneurs de carnet d’adresses ne doivent pas essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="e6d79-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="e6d79-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="e6d79-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="e6d79-121">L’entrée n’a pas été résolue.</span><span class="sxs-lookup"><span data-stu-id="e6d79-121">The entry has not been resolved.</span></span> <span data-ttu-id="e6d79-122">Les autres conteneurs de carnet d’adresses doivent essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="e6d79-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6d79-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6d79-123">Remarks</span></span>

<span data-ttu-id="e6d79-124">La structure **FLAGLIST** est utilisée comme paramètre pour [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="e6d79-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="e6d79-125">Chacun des destinataires à résoudre est inclus dans une structure [ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="e6d79-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="e6d79-126">Lorsque le conteneur de carnet d’adresses tente de résoudre chaque destinataire, il définit l’indicateur approprié dans l’entrée correspondante dans la structure **FLAGLIST.**</span><span class="sxs-lookup"><span data-stu-id="e6d79-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="e6d79-127">Toutes les entrées de la structure **FLAGLIST** sont dans le même ordre que les entrées de la structure **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="e6d79-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="e6d79-128">Cela facilite l’association d’un paramètre d’indicateur à un destinataire.</span><span class="sxs-lookup"><span data-stu-id="e6d79-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6d79-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6d79-129">See also</span></span>



[<span data-ttu-id="e6d79-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e6d79-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="e6d79-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e6d79-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="e6d79-132">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e6d79-132">MAPI Structures</span></span>](mapi-structures.md)


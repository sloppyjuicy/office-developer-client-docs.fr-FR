---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418091"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="442fa-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="442fa-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="442fa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="442fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="442fa-105">Indique si Microsoft Office Outlook doit analyser les dossiers d'une banque et les archiver automatiquement.</span><span class="sxs-lookup"><span data-stu-id="442fa-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="442fa-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="442fa-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="442fa-107">Exposé sur:</span><span class="sxs-lookup"><span data-stu-id="442fa-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="442fa-108">[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="442fa-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="442fa-109">Créé par:</span><span class="sxs-lookup"><span data-stu-id="442fa-109">Created by:</span></span>  <br/> |<span data-ttu-id="442fa-110">Fournisseur de magasin</span><span class="sxs-lookup"><span data-stu-id="442fa-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="442fa-111">Accès par:</span><span class="sxs-lookup"><span data-stu-id="442fa-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="442fa-112">Outlook et d'autres clients</span><span class="sxs-lookup"><span data-stu-id="442fa-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="442fa-113">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="442fa-113">Property type:</span></span>  <br/> |<span data-ttu-id="442fa-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="442fa-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="442fa-115">Type d'accès:</span><span class="sxs-lookup"><span data-stu-id="442fa-115">Access type:</span></span>  <br/> |<span data-ttu-id="442fa-116">Lecture seule ou lecture/écriture en fonction du fournisseur de la Banque</span><span class="sxs-lookup"><span data-stu-id="442fa-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="442fa-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="442fa-117">Remarks</span></span>

<span data-ttu-id="442fa-118">Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="442fa-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="442fa-119">Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="442fa-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="442fa-120">Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="442fa-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="442fa-121">Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="442fa-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="442fa-122">Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="442fa-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="442fa-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="442fa-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="442fa-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="442fa-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="442fa-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="442fa-125">ulKind:</span></span>  <br/> |<span data-ttu-id="442fa-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="442fa-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="442fa-127">Kind. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="442fa-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="442fa-128">L "ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="442fa-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="442fa-129">Cette propriété permet aux fournisseurs de magasin de spécifier si Outlook doit analyser les dossiers d'une banque et les archiver automatiquement.</span><span class="sxs-lookup"><span data-stu-id="442fa-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="442fa-130">Par défaut, cette propriété n'est pas exposée sur un magasin, ce qui signifie qu'Outlook peut analyser les dossiers de la Banque.</span><span class="sxs-lookup"><span data-stu-id="442fa-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="442fa-131">Si la propriété est exposée, les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="442fa-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="442fa-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="442fa-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="442fa-133">Outlook peut analyser les dossiers de la Banque.</span><span class="sxs-lookup"><span data-stu-id="442fa-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="442fa-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="442fa-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="442fa-135">Outlook ne doit pas analyser les dossiers de la Banque.</span><span class="sxs-lookup"><span data-stu-id="442fa-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="442fa-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="442fa-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="442fa-137">Ne pas autoriser les clients à modifier cette propriété sur le magasin.</span><span class="sxs-lookup"><span data-stu-id="442fa-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="442fa-138">Notez que la constante **ASM_CLIENT_DO_NOT_CHANGE** est destinée à des fins de référence ultérieure et qu'elle n'est pas actuellement implémentée.</span><span class="sxs-lookup"><span data-stu-id="442fa-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="442fa-139">Pour le moment, un magasin peut empêcher les clients de modifier cet indicateur en codage en dur la valeur renvoyée par la Banque pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="442fa-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    


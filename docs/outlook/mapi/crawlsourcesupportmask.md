---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420912"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="79539-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="79539-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="79539-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79539-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79539-105">Spécifie si Microsoft Office Outlook doit analyser les dossiers d’une boutique, y compris les dossiers Contacts, Calendrier et Tâches, au démarrage pour remplir le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="79539-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79539-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="79539-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79539-107">Exposé sur :</span><span class="sxs-lookup"><span data-stu-id="79539-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="79539-108">[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="79539-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="79539-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="79539-109">Created by:</span></span>  <br/> |<span data-ttu-id="79539-110">Fournisseur du Store</span><span class="sxs-lookup"><span data-stu-id="79539-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="79539-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="79539-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="79539-112">Outlook et d’autres clients</span><span class="sxs-lookup"><span data-stu-id="79539-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="79539-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="79539-113">Property type:</span></span>  <br/> |<span data-ttu-id="79539-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="79539-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="79539-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="79539-115">Access type:</span></span>  <br/> |<span data-ttu-id="79539-116">En lecture seule ou en lecture/écriture en fonction du fournisseur du magasin</span><span class="sxs-lookup"><span data-stu-id="79539-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79539-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="79539-117">Remarks</span></span>

<span data-ttu-id="79539-118">Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="79539-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="79539-119">Lorsque la balise de propriété de l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasins doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="79539-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="79539-120">Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="79539-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="79539-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="79539-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="79539-122">Lorsque vous appelez [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="79539-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79539-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="79539-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="79539-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="79539-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="79539-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="79539-125">ulKind:</span></span>  <br/> |<span data-ttu-id="79539-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="79539-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="79539-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="79539-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="79539-128">L"CrawlSourceSupportMask »</span><span class="sxs-lookup"><span data-stu-id="79539-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="79539-129">Cette propriété permet aux fournisseurs de magasins de spécifier si Outlook doit analyser différents dossiers dans une boutique.</span><span class="sxs-lookup"><span data-stu-id="79539-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="79539-130">Il est utilisé au démarrage lorsqu’Outlook analyse les dossiers existants sur chaque magasin ouvert pour remplir le volet **de** navigation . Outlook vérifie la présence et la valeur de cette propriété dans une boutique avant de lancer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="79539-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="79539-131">Par défaut, cette propriété n’est pas exposée dans une boutique, ce qui signifie qu’Outlook peut analyser les dossiers de la boutique.</span><span class="sxs-lookup"><span data-stu-id="79539-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="79539-132">Si la propriété est exposée, les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="79539-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="79539-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="79539-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="79539-134">Outlook peut analyser les dossiers de la boutique.</span><span class="sxs-lookup"><span data-stu-id="79539-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="79539-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="79539-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="79539-136">Outlook ne doit pas analyser les dossiers de la boutique.</span><span class="sxs-lookup"><span data-stu-id="79539-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="79539-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="79539-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="79539-138">N’autorisez pas les clients à modifier cette propriété sur le store.</span><span class="sxs-lookup"><span data-stu-id="79539-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="79539-139">Notez que la constante **CSM_CLIENT_DO_NOT_CHANGE** est à des références futures et n’est pas implémentée actuellement.</span><span class="sxs-lookup"><span data-stu-id="79539-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="79539-140">Pour l’instant, un magasin peut empêcher les clients de modifier cet indicateur en encodant en dur la valeur que la boutique renvoie pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="79539-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    


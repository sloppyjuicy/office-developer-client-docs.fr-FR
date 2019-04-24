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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333046"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="d19be-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="d19be-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="d19be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d19be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d19be-105">Indique si Microsoft Office Outlook doit analyser les dossiers d'une banque, y compris les dossiers contacts, calendrier et tâches, au démarrage pour renseigner le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="d19be-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d19be-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d19be-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d19be-107">Exposé sur:</span><span class="sxs-lookup"><span data-stu-id="d19be-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="d19be-108">[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d19be-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="d19be-109">Créé par:</span><span class="sxs-lookup"><span data-stu-id="d19be-109">Created by:</span></span>  <br/> |<span data-ttu-id="d19be-110">Fournisseur de magasin</span><span class="sxs-lookup"><span data-stu-id="d19be-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="d19be-111">Accès par:</span><span class="sxs-lookup"><span data-stu-id="d19be-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="d19be-112">Outlook et d'autres clients</span><span class="sxs-lookup"><span data-stu-id="d19be-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="d19be-113">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="d19be-113">Property type:</span></span>  <br/> |<span data-ttu-id="d19be-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d19be-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d19be-115">Type d'accès:</span><span class="sxs-lookup"><span data-stu-id="d19be-115">Access type:</span></span>  <br/> |<span data-ttu-id="d19be-116">Lecture seule ou lecture/écriture en fonction du fournisseur de la Banque</span><span class="sxs-lookup"><span data-stu-id="d19be-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d19be-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d19be-117">Remarks</span></span>

<span data-ttu-id="d19be-118">Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="d19be-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="d19be-119">Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="d19be-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="d19be-120">Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d19be-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="d19be-121">Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="d19be-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="d19be-122">Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="d19be-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d19be-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="d19be-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="d19be-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d19be-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d19be-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="d19be-125">ulKind:</span></span>  <br/> |<span data-ttu-id="d19be-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d19be-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="d19be-127">Kind. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="d19be-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="d19be-128">L "CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="d19be-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="d19be-129">Cette propriété permet aux fournisseurs de magasins de spécifier si Outlook doit analyser les différents dossiers d'une banque.</span><span class="sxs-lookup"><span data-stu-id="d19be-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="d19be-130">Elle est utilisée au démarrage quand Outlook analyse les dossiers existants sur chaque banque ouverte pour remplir le volet de **navigation** ; Outlook vérifie la présence et la valeur de cette propriété sur un magasin avant de lancer l'analyse.</span><span class="sxs-lookup"><span data-stu-id="d19be-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="d19be-131">Par défaut, cette propriété n'est pas exposée sur un magasin, ce qui signifie qu'Outlook peut analyser les dossiers de la Banque.</span><span class="sxs-lookup"><span data-stu-id="d19be-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="d19be-132">Si la propriété est exposée, les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="d19be-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="d19be-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d19be-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="d19be-134">Outlook peut analyser les dossiers de la Banque.</span><span class="sxs-lookup"><span data-stu-id="d19be-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="d19be-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="d19be-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="d19be-136">Outlook ne doit pas analyser les dossiers de la Banque.</span><span class="sxs-lookup"><span data-stu-id="d19be-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="d19be-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d19be-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="d19be-138">Ne pas autoriser les clients à modifier cette propriété sur le magasin.</span><span class="sxs-lookup"><span data-stu-id="d19be-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="d19be-139">Notez que la constante **CSM_CLIENT_DO_NOT_CHANGE** est destinée à des fins de référence ultérieure et qu'elle n'est pas actuellement implémentée.</span><span class="sxs-lookup"><span data-stu-id="d19be-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="d19be-140">Pour le moment, un magasin peut empêcher les clients de modifier cet indicateur en codage en dur la valeur renvoyée par la Banque pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d19be-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    


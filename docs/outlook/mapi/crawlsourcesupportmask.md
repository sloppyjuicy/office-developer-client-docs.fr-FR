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
ms.openlocfilehash: a1754a7c82d7164617c97df97b762efb1555ccda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783096"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="256dc-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="256dc-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="256dc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="256dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="256dc-105">Spécifie si Microsoft Office Outlook doit analyser les dossiers d’une banque, y compris les dossiers Contacts, calendrier et tâches au démarrage pour remplir le volet de Navigation.</span><span class="sxs-lookup"><span data-stu-id="256dc-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="256dc-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="256dc-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="256dc-107">Exposée sur :</span><span class="sxs-lookup"><span data-stu-id="256dc-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="256dc-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet</span><span class="sxs-lookup"><span data-stu-id="256dc-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="256dc-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="256dc-109">Created by:</span></span>  <br/> |<span data-ttu-id="256dc-110">Fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="256dc-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="256dc-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="256dc-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="256dc-112">Outlook et autres clients</span><span class="sxs-lookup"><span data-stu-id="256dc-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="256dc-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="256dc-113">Property type:</span></span>  <br/> |<span data-ttu-id="256dc-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="256dc-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="256dc-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="256dc-115">Access type:</span></span>  <br/> |<span data-ttu-id="256dc-116">En lecture seule ou en lecture/écriture, selon le fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="256dc-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="256dc-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="256dc-117">Remarks</span></span>

<span data-ttu-id="256dc-118">Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="256dc-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="256dc-119">Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate.</span><span class="sxs-lookup"><span data-stu-id="256dc-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="256dc-120">Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="256dc-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="256dc-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="256dc-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="256dc-122">Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="256dc-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="256dc-123">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="256dc-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="256dc-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="256dc-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="256dc-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="256dc-125">ulKind:</span></span>  <br/> |<span data-ttu-id="256dc-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="256dc-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="256dc-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="256dc-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="256dc-128">L « CrawlSourceSupportMask »</span><span class="sxs-lookup"><span data-stu-id="256dc-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="256dc-129">Cette propriété fournit un moyen pour les fournisseurs de banque spécifier si Outlook doit rechercher les différents dossiers d’une banque.</span><span class="sxs-lookup"><span data-stu-id="256dc-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="256dc-130">Il est utilisé au démarrage lorsqu’Outlook analyse les dossiers existants sur chaque magasin ouvert pour remplir le volet de **Navigation** ; Outlook vérifie la présence et la valeur de cette propriété sur une banque avant de lancer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="256dc-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="256dc-131">Par défaut, cette propriété n’est pas exposée dans une banque, ce qui signifie qu’Outlook peut analyser les dossiers sur le magasin.</span><span class="sxs-lookup"><span data-stu-id="256dc-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="256dc-132">Si la propriété est exposée, les valeurs possibles sont les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="256dc-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="256dc-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="256dc-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="256dc-134">Outlook peut analyser les dossiers sur le magasin.</span><span class="sxs-lookup"><span data-stu-id="256dc-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="256dc-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="256dc-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="256dc-136">Outlook n’a pas doit analyser les dossiers sur le magasin.</span><span class="sxs-lookup"><span data-stu-id="256dc-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="256dc-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="256dc-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="256dc-138">Ne pas autoriser les clients à modifier cette propriété dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="256dc-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="256dc-139">Notez que la constante **CSM_CLIENT_DO_NOT_CHANGE** est pour servir ultérieurement de référence et n’est pas implémenté actuellement.</span><span class="sxs-lookup"><span data-stu-id="256dc-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="256dc-140">À ce stade, un magasin peut empêcher les clients cet indicateur à coder la valeur de cette propriété renvoie le magasin.</span><span class="sxs-lookup"><span data-stu-id="256dc-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    


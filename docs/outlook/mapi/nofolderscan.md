---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436809"
---
# <a name="nofolderscan"></a><span data-ttu-id="0bb78-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="0bb78-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="0bb78-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bb78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bb78-105">Indique si Microsoft Office Outlook doit analyser les dossiers de contacts d'une banque d'information.</span><span class="sxs-lookup"><span data-stu-id="0bb78-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0bb78-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0bb78-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bb78-107">Exposé sur:</span><span class="sxs-lookup"><span data-stu-id="0bb78-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="0bb78-108">[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="0bb78-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="0bb78-109">Créé par:</span><span class="sxs-lookup"><span data-stu-id="0bb78-109">Created by:</span></span>  <br/> |<span data-ttu-id="0bb78-110">Fournisseur de magasin</span><span class="sxs-lookup"><span data-stu-id="0bb78-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="0bb78-111">Accès par:</span><span class="sxs-lookup"><span data-stu-id="0bb78-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="0bb78-112">Outlook et d'autres clients</span><span class="sxs-lookup"><span data-stu-id="0bb78-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="0bb78-113">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="0bb78-113">Property type:</span></span>  <br/> |<span data-ttu-id="0bb78-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0bb78-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0bb78-115">Type d'accès:</span><span class="sxs-lookup"><span data-stu-id="0bb78-115">Access type:</span></span>  <br/> |<span data-ttu-id="0bb78-116">Lecture seule ou lecture/écriture en fonction du fournisseur de la Banque</span><span class="sxs-lookup"><span data-stu-id="0bb78-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bb78-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="0bb78-117">Remarks</span></span>

<span data-ttu-id="0bb78-118">Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="0bb78-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="0bb78-119">Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="0bb78-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="0bb78-120">Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0bb78-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="0bb78-121">Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="0bb78-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="0bb78-122">Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="0bb78-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bb78-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="0bb78-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="0bb78-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0bb78-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0bb78-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="0bb78-125">ulKind:</span></span>  <br/> |<span data-ttu-id="0bb78-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="0bb78-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="0bb78-127">Kind. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="0bb78-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="0bb78-128">L "NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="0bb78-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="0bb78-129">Cette propriété permet aux fournisseurs de magasin de spécifier à Outlook de ne pas analyser les dossiers de contacts dans le magasin pour éviter une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="0bb78-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="0bb78-130">Elle est utilisée dans les opérations de fusion et publipostage au cours desquelles Outlook vérifie la présence et la valeur de cette propriété avant de lancer l'analyse.</span><span class="sxs-lookup"><span data-stu-id="0bb78-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="0bb78-131">Par défaut, cette propriété n'est pas exposée sur un magasin, ce qui signifie qu'Outlook peut analyser le dossier contacts de la Banque.</span><span class="sxs-lookup"><span data-stu-id="0bb78-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="0bb78-132">Si la propriété est exposée, les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="0bb78-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="0bb78-133">Zéro (0): Outlook peut effectuer l'analyse.</span><span class="sxs-lookup"><span data-stu-id="0bb78-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="0bb78-134">Valeur non nulle: Outlook ne doit pas analyser les dossiers de contacts de la Banque.</span><span class="sxs-lookup"><span data-stu-id="0bb78-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    


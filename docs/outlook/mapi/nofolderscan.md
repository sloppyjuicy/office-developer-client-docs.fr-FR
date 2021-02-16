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
# <a name="nofolderscan"></a><span data-ttu-id="d1f84-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="d1f84-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="d1f84-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1f84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1f84-105">Spécifie si Microsoft Office Outlook doit analyser les dossiers Contacts d’une boutique.</span><span class="sxs-lookup"><span data-stu-id="d1f84-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d1f84-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d1f84-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1f84-107">Exposé sur :</span><span class="sxs-lookup"><span data-stu-id="d1f84-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="d1f84-108">[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d1f84-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="d1f84-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="d1f84-109">Created by:</span></span>  <br/> |<span data-ttu-id="d1f84-110">Fournisseur du Store</span><span class="sxs-lookup"><span data-stu-id="d1f84-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="d1f84-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="d1f84-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="d1f84-112">Outlook et d’autres clients</span><span class="sxs-lookup"><span data-stu-id="d1f84-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="d1f84-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="d1f84-113">Property type:</span></span>  <br/> |<span data-ttu-id="d1f84-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d1f84-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d1f84-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="d1f84-115">Access type:</span></span>  <br/> |<span data-ttu-id="d1f84-116">En lecture seule ou en lecture/écriture en fonction du fournisseur du magasin</span><span class="sxs-lookup"><span data-stu-id="d1f84-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1f84-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1f84-117">Remarks</span></span>

<span data-ttu-id="d1f84-118">Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="d1f84-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="d1f84-119">Lorsque la balise de propriété de l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasins doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="d1f84-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="d1f84-120">Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d1f84-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="d1f84-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="d1f84-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="d1f84-122">Lorsque vous appelez [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="d1f84-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1f84-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="d1f84-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="d1f84-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d1f84-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d1f84-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="d1f84-125">ulKind:</span></span>  <br/> |<span data-ttu-id="d1f84-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d1f84-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="d1f84-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="d1f84-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="d1f84-128">L"NoFolderScan »</span><span class="sxs-lookup"><span data-stu-id="d1f84-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="d1f84-129">Cette propriété permet aux fournisseurs de magasins de spécifier à Outlook de ne pas analyser les dossiers contacts de la boutique afin d’éviter une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="d1f84-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="d1f84-130">Il est utilisé dans les opérations de fusion et publipostage au cours des lesquelles Outlook vérifie la présence et la valeur de cette propriété avant de lancer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="d1f84-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="d1f84-131">Par défaut, cette propriété n’est pas exposée dans une boutique, ce qui signifie qu’Outlook peut analyser le dossier Contacts de la boutique.</span><span class="sxs-lookup"><span data-stu-id="d1f84-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="d1f84-132">Si la propriété est exposée, les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1f84-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="d1f84-133">Zéro (0) : Outlook peut effectuer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="d1f84-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="d1f84-134">Valeur non nulle : Outlook ne doit pas analyser les dossiers contacts de la boutique.</span><span class="sxs-lookup"><span data-stu-id="d1f84-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    


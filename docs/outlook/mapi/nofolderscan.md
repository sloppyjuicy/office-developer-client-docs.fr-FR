---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3416bc50e4628df2be09f9fe1a22d19530bcdff8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578051"
---
# <a name="nofolderscan"></a><span data-ttu-id="74946-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="74946-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="74946-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74946-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74946-105">Spécifie si Microsoft Office Outlook doit analyser les dossiers sur un magasin de Contacts.</span><span class="sxs-lookup"><span data-stu-id="74946-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="74946-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="74946-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74946-107">Exposée sur :</span><span class="sxs-lookup"><span data-stu-id="74946-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="74946-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet</span><span class="sxs-lookup"><span data-stu-id="74946-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="74946-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="74946-109">Created by:</span></span>  <br/> |<span data-ttu-id="74946-110">Fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="74946-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="74946-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="74946-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="74946-112">Outlook et autres clients</span><span class="sxs-lookup"><span data-stu-id="74946-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="74946-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="74946-113">Property type:</span></span>  <br/> |<span data-ttu-id="74946-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74946-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74946-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="74946-115">Access type:</span></span>  <br/> |<span data-ttu-id="74946-116">En lecture seule ou en lecture/écriture, selon le fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="74946-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74946-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="74946-117">Remarks</span></span>

<span data-ttu-id="74946-118">Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="74946-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="74946-119">Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate.</span><span class="sxs-lookup"><span data-stu-id="74946-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="74946-120">Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="74946-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="74946-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="74946-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="74946-122">Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="74946-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74946-123">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="74946-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="74946-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="74946-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="74946-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="74946-125">ulKind:</span></span>  <br/> |<span data-ttu-id="74946-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="74946-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="74946-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="74946-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="74946-128">L « NoFolderScan »</span><span class="sxs-lookup"><span data-stu-id="74946-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="74946-129">Cette propriété permet de pour les fournisseurs de banque indiquer à Outlook ne pas analyser les dossiers de Contacts dans le magasin afin d’éviter une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="74946-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="74946-130">Il est utilisé dans les opérations de fusion et publipostage au cours de laquelle Outlook vérifie la présence et la valeur de cette propriété avant de lancer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="74946-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="74946-131">Par défaut, cette propriété n’est pas exposée dans une banque, ce qui signifie qu’Outlook peut analyser le dossier Contacts dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="74946-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="74946-132">Si la propriété est exposée, les valeurs possibles sont les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="74946-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="74946-133">Zéro (0) : Outlook peut effectuer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="74946-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="74946-134">Valeur non nulle : Outlook n’a pas doit analyser les dossiers sur le magasin de Contacts.</span><span class="sxs-lookup"><span data-stu-id="74946-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    


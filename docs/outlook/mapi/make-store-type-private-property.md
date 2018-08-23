---
title: Propriété de privatisation du type de magasin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2d927b00391725d8804e41b66b1ec8c384f98e7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568832"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="5243e-103">Propriété de privatisation du type de magasin</span><span class="sxs-lookup"><span data-stu-id="5243e-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="5243e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5243e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5243e-105">Traite un stockage secondaire comme privée.</span><span class="sxs-lookup"><span data-stu-id="5243e-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5243e-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5243e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5243e-107">Exposée sur :</span><span class="sxs-lookup"><span data-stu-id="5243e-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="5243e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet</span><span class="sxs-lookup"><span data-stu-id="5243e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="5243e-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="5243e-109">Created by:</span></span>  <br/> |<span data-ttu-id="5243e-110">Fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="5243e-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="5243e-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="5243e-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="5243e-112">Outlook et autres clients</span><span class="sxs-lookup"><span data-stu-id="5243e-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="5243e-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="5243e-113">Property type:</span></span>  <br/> |<span data-ttu-id="5243e-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5243e-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5243e-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="5243e-115">Access type:</span></span>  <br/> |<span data-ttu-id="5243e-116">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="5243e-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5243e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="5243e-117">Remarks</span></span>

<span data-ttu-id="5243e-118">Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="5243e-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="5243e-119">Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate.</span><span class="sxs-lookup"><span data-stu-id="5243e-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="5243e-120">Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5243e-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="5243e-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="5243e-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="5243e-122">Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="5243e-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5243e-123">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="5243e-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="5243e-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="5243e-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="5243e-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="5243e-125">ulKind:</span></span>  <br/> |<span data-ttu-id="5243e-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5243e-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="5243e-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="5243e-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="5243e-128">L « urn : schemas-microsoft-com:office:outlook #storetypeprivate »</span><span class="sxs-lookup"><span data-stu-id="5243e-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="5243e-129">Un fournisseur de magasin de cette propriété permet à Outlook de traiter comme privée lorsqu’il s’agit d’un magasin secondaire pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5243e-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="5243e-130">Par défaut, Outlook traite un stockage secondaire de la même manière comme une banque déléguée et éléments dans le magasin secondaire sont privés uniquement si l’utilisateur les marque spécifiquement comme étant privé.</span><span class="sxs-lookup"><span data-stu-id="5243e-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="5243e-131">Lorsque cette propriété a la **valeur true**, les éléments supprimés à partir d’un stockage secondaire sont déplacés vers le dossier **Éléments supprimés** dans le magasin principal.</span><span class="sxs-lookup"><span data-stu-id="5243e-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="5243e-132">Éléments marqués comme privés ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="5243e-132">Items marked private are not displayed.</span></span> <span data-ttu-id="5243e-133">Brouillons sont stockés dans le dossier Brouillons dans le magasin principal.</span><span class="sxs-lookup"><span data-stu-id="5243e-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="5243e-134">Cette propriété est ignorée si la version d’Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="5243e-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  


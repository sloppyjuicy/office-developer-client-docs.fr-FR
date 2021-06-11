---
title: Make Store Type Private, propriété
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428542"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="f5af5-103">Make Store Type Private, propriété</span><span class="sxs-lookup"><span data-stu-id="f5af5-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="f5af5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5af5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5af5-105">Traite un magasin secondaire comme privé.</span><span class="sxs-lookup"><span data-stu-id="f5af5-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5af5-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f5af5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5af5-107">Exposé sur :</span><span class="sxs-lookup"><span data-stu-id="f5af5-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="f5af5-108">[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f5af5-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="f5af5-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="f5af5-109">Created by:</span></span>  <br/> |<span data-ttu-id="f5af5-110">Fournisseur du Store</span><span class="sxs-lookup"><span data-stu-id="f5af5-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="f5af5-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="f5af5-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="f5af5-112">Outlook clients et autres clients</span><span class="sxs-lookup"><span data-stu-id="f5af5-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="f5af5-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="f5af5-113">Property type:</span></span>  <br/> |<span data-ttu-id="f5af5-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f5af5-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f5af5-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="f5af5-115">Access type:</span></span>  <br/> |<span data-ttu-id="f5af5-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f5af5-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5af5-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5af5-117">Remarks</span></span>

<span data-ttu-id="f5af5-118">Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="f5af5-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="f5af5-119">Lorsque la balise de propriété pour l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasin doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="f5af5-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="f5af5-120">Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f5af5-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="f5af5-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="f5af5-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="f5af5-122">Lorsque vous appelez [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="f5af5-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5af5-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="f5af5-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="f5af5-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="f5af5-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="f5af5-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="f5af5-125">ulKind:</span></span>  <br/> |<span data-ttu-id="f5af5-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="f5af5-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="f5af5-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="f5af5-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="f5af5-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate »</span><span class="sxs-lookup"><span data-stu-id="f5af5-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="f5af5-129">Un fournisseur de banque d’informations peut utiliser cette propriété Outlook la traiter comme privée lorsqu’il s’agit d’un magasin secondaire pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5af5-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="f5af5-130">Par défaut, Outlook traite une banque secondaire de la même manière qu’un magasin de délégués, et les éléments de la banque secondaire sont privés uniquement si l’utilisateur les marque spécifiquement comme privés.</span><span class="sxs-lookup"><span data-stu-id="f5af5-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="f5af5-131">Lorsque cette propriété est **true,** les éléments supprimés d’une magasin secondaire sont déplacés vers le **dossier** Éléments supprimés dans la boutique principale.</span><span class="sxs-lookup"><span data-stu-id="f5af5-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="f5af5-132">Les éléments marqués comme privés ne sont pas affichés.</span><span class="sxs-lookup"><span data-stu-id="f5af5-132">Items marked private are not displayed.</span></span> <span data-ttu-id="f5af5-133">Les brouillons sont stockés dans le dossier Brouillons de la boutique principale.</span><span class="sxs-lookup"><span data-stu-id="f5af5-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="f5af5-134">Cette propriété est ignorée si la version de Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="f5af5-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  


---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413380"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="36abf-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36abf-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="36abf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36abf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36abf-105">Gère les objets associés à une session d’ouverture de session MAPI.</span><span class="sxs-lookup"><span data-stu-id="36abf-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36abf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="36abf-106">Header file:</span></span>  <br/> |<span data-ttu-id="36abf-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="36abf-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="36abf-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="36abf-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="36abf-109">Objets de session</span><span class="sxs-lookup"><span data-stu-id="36abf-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="36abf-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="36abf-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="36abf-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="36abf-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="36abf-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="36abf-112">Called by:</span></span>  <br/> |<span data-ttu-id="36abf-113">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="36abf-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="36abf-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="36abf-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="36abf-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="36abf-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="36abf-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="36abf-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="36abf-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="36abf-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="36abf-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="36abf-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="36abf-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="36abf-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="36abf-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente.</span><span class="sxs-lookup"><span data-stu-id="36abf-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="36abf-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="36abf-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="36abf-122">Permet d’accéder à la table de la boutique de messages qui contient des informations sur tous les magasins de messages dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="36abf-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="36abf-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="36abf-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="36abf-124">Ouvre une magasin de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="36abf-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="36abf-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="36abf-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="36abf-126">Ouvre le carnet d’adresses intégré MAPI, en renvoyant un [pointeur IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="36abf-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="36abf-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="36abf-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="36abf-128">Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="36abf-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="36abf-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="36abf-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="36abf-130">Permet d’accéder à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session.</span><span class="sxs-lookup"><span data-stu-id="36abf-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="36abf-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="36abf-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="36abf-132">Ouvre un objet et renvoie un pointeur d’interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="36abf-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="36abf-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="36abf-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="36abf-134">Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="36abf-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="36abf-135">Conseiller</span><span class="sxs-lookup"><span data-stu-id="36abf-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="36abf-136">S’inscrit pour recevoir une notification des événements spécifiés qui affectent la session.</span><span class="sxs-lookup"><span data-stu-id="36abf-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="36abf-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="36abf-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="36abf-138">Annule l’envoi de notifications précédemment définies avec un appel à la **méthode Advise.**</span><span class="sxs-lookup"><span data-stu-id="36abf-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="36abf-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="36abf-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="36abf-140">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="36abf-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="36abf-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="36abf-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="36abf-142">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="36abf-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="36abf-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="36abf-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="36abf-144">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="36abf-144">Deprecated.</span></span> <span data-ttu-id="36abf-145">Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session.</span><span class="sxs-lookup"><span data-stu-id="36abf-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="36abf-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="36abf-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="36abf-147">Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session.</span><span class="sxs-lookup"><span data-stu-id="36abf-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="36abf-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="36abf-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="36abf-149">Met fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="36abf-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="36abf-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="36abf-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="36abf-151">Établit une magasin de messages comme magasin de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="36abf-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="36abf-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="36abf-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="36abf-153">Renvoie un [pointeur IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de message.</span><span class="sxs-lookup"><span data-stu-id="36abf-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="36abf-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="36abf-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="36abf-155">Affiche un formulaire.</span><span class="sxs-lookup"><span data-stu-id="36abf-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="36abf-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="36abf-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="36abf-157">Crée un jeton numérique que la **méthode ShowForm** utilise pour accéder à un message.</span><span class="sxs-lookup"><span data-stu-id="36abf-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36abf-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36abf-158">See also</span></span>



[<span data-ttu-id="36abf-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="36abf-159">MAPI Interfaces</span></span>](mapi-interfaces.md)


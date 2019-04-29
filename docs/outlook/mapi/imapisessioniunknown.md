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
# <a name="imapisession--iunknown"></a><span data-ttu-id="4380a-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4380a-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="4380a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4380a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4380a-105">Gère les objets associés à une ouverture de session MAPI.</span><span class="sxs-lookup"><span data-stu-id="4380a-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4380a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4380a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4380a-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="4380a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="4380a-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="4380a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4380a-109">Objets de session</span><span class="sxs-lookup"><span data-stu-id="4380a-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="4380a-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="4380a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4380a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4380a-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="4380a-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="4380a-112">Called by:</span></span>  <br/> |<span data-ttu-id="4380a-113">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="4380a-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="4380a-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="4380a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4380a-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="4380a-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="4380a-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="4380a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4380a-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="4380a-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4380a-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="4380a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4380a-119">Généré</span><span class="sxs-lookup"><span data-stu-id="4380a-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="4380a-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur de session précédente.</span><span class="sxs-lookup"><span data-stu-id="4380a-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="4380a-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="4380a-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="4380a-122">Fournit l'accès à la table de banque de messages qui contient des informations sur toutes les banques de messages dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="4380a-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="4380a-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="4380a-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="4380a-124">Ouvre une banque de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="4380a-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="4380a-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="4380a-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="4380a-126">Ouvre le carnet d'adresses intégré MAPI, en renvoyant un pointeur [IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="4380a-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="4380a-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="4380a-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="4380a-128">Ouvre une section du profil actif et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="4380a-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="4380a-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="4380a-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="4380a-130">Fournit l'accès à la table d'État, un tableau qui contient des informations sur toutes les ressources MAPI de la session.</span><span class="sxs-lookup"><span data-stu-id="4380a-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="4380a-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4380a-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="4380a-132">Ouvre un objet et renvoie un pointeur d'interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="4380a-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="4380a-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4380a-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="4380a-134">Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="4380a-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="4380a-135">Recommander</span><span class="sxs-lookup"><span data-stu-id="4380a-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="4380a-136">S'inscrit pour recevoir des notifications d'événements spécifiques affectant la session.</span><span class="sxs-lookup"><span data-stu-id="4380a-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="4380a-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="4380a-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="4380a-138">Annule l'envoi de notifications précédemment configurées avec un appel à \*\*\*\* la méthode Advise.</span><span class="sxs-lookup"><span data-stu-id="4380a-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="4380a-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="4380a-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="4380a-140">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="4380a-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="4380a-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="4380a-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="4380a-142">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="4380a-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="4380a-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="4380a-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="4380a-144">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="4380a-144">Deprecated.</span></span> <span data-ttu-id="4380a-145">Renvoie les types d'adresses qui peuvent être gérées par tous les fournisseurs de transport dans la session.</span><span class="sxs-lookup"><span data-stu-id="4380a-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="4380a-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="4380a-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="4380a-147">Renvoie l'identificateur d'entrée de l'objet qui fournit l'identité principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="4380a-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="4380a-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="4380a-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="4380a-149">Met fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="4380a-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="4380a-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="4380a-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="4380a-151">Établit une banque de messages comme banque de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="4380a-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="4380a-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="4380a-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="4380a-153">Renvoie un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4380a-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="4380a-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="4380a-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="4380a-155">Affiche un formulaire.</span><span class="sxs-lookup"><span data-stu-id="4380a-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="4380a-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4380a-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="4380a-157">Crée un jeton numérique que la méthode **ShowForm** utilise pour accéder à un message.</span><span class="sxs-lookup"><span data-stu-id="4380a-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4380a-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4380a-158">See also</span></span>



[<span data-ttu-id="4380a-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4380a-159">MAPI Interfaces</span></span>](mapi-interfaces.md)


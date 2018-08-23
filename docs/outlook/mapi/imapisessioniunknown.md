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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 163bce38d665a8566fd703420ff1f7b2f44f7c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571807"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="6a2b6-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a2b6-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="6a2b6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a2b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a2b6-105">Gère les objets associés à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a2b6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6a2b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a2b6-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="6a2b6-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6a2b6-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="6a2b6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6a2b6-109">Objets de session</span><span class="sxs-lookup"><span data-stu-id="6a2b6-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="6a2b6-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6a2b6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a2b6-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a2b6-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a2b6-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6a2b6-112">Called by:</span></span>  <br/> |<span data-ttu-id="6a2b6-113">Les applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="6a2b6-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="6a2b6-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="6a2b6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6a2b6-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="6a2b6-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="6a2b6-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="6a2b6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6a2b6-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="6a2b6-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6a2b6-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="6a2b6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6a2b6-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="6a2b6-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="6a2b6-120">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="6a2b6-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="6a2b6-122">Permet d’accéder à la table de magasin de message qui contient des informations sur toutes les banques de messages dans le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="6a2b6-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="6a2b6-124">Ouvre une banque de messages et retourne un pointeur [IMsgStore](imsgstoreimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="6a2b6-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="6a2b6-126">Ouvre le carnet d’adresses intégré MAPI, qui retourne un pointeur [IAddrBook](iaddrbookimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="6a2b6-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="6a2b6-128">Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="6a2b6-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="6a2b6-130">Fournit l’accès à la table d’état, une table qui contient des informations sur toutes les ressources MAPI dans la session.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6a2b6-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="6a2b6-132">Ouvre un objet et retourne un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6a2b6-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="6a2b6-134">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-135">Conseiller</span><span class="sxs-lookup"><span data-stu-id="6a2b6-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="6a2b6-136">Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la session.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-137">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="6a2b6-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="6a2b6-138">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **Advise** .</span><span class="sxs-lookup"><span data-stu-id="6a2b6-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="6a2b6-139">**Options des messages**</span><span class="sxs-lookup"><span data-stu-id="6a2b6-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="6a2b6-140">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="6a2b6-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="6a2b6-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="6a2b6-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="6a2b6-142">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="6a2b6-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="6a2b6-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="6a2b6-144">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-144">Deprecated.</span></span> <span data-ttu-id="6a2b6-145">Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="6a2b6-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="6a2b6-147">Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité du principale pour la session.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="6a2b6-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="6a2b6-149">Met fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="6a2b6-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="6a2b6-151">Établissement d’une banque de messages comme banque de messages par défaut pour la session.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="6a2b6-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="6a2b6-153">Retourne un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications à des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="6a2b6-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="6a2b6-155">Affiche un formulaire.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="6a2b6-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="6a2b6-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="6a2b6-157">Crée un jeton numérique que la méthode **ShowForm** utilise pour accéder à un message.</span><span class="sxs-lookup"><span data-stu-id="6a2b6-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a2b6-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a2b6-158">See also</span></span>



[<span data-ttu-id="6a2b6-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6a2b6-159">MAPI Interfaces</span></span>](mapi-interfaces.md)


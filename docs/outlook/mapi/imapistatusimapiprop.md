---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783965"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="44970-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="44970-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="44970-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44970-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44970-105">Fournit des informations d’état sur le sous-système MAPI, le carnet d’adresses intégré et le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="44970-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="44970-106">Un fournisseur de services implémente **IMAPIStatus** pour fournir des informations sur son propre état.</span><span class="sxs-lookup"><span data-stu-id="44970-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44970-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="44970-107">Header file:</span></span>  <br/> |<span data-ttu-id="44970-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44970-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="44970-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="44970-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="44970-110">Objets d’état</span><span class="sxs-lookup"><span data-stu-id="44970-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="44970-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="44970-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="44970-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="44970-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="44970-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="44970-113">Called by:</span></span>  <br/> |<span data-ttu-id="44970-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="44970-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="44970-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="44970-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="44970-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="44970-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="44970-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="44970-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="44970-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="44970-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="44970-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="44970-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="44970-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="44970-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="44970-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="44970-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="44970-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="44970-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="44970-123">Vérifie les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="44970-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="44970-124">Dialogue</span><span class="sxs-lookup"><span data-stu-id="44970-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="44970-125">Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="44970-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="44970-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="44970-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="44970-127">Modifie le mot de passe d’un fournisseur de services sans afficher l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44970-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="44970-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="44970-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="44970-129">Force tous les messages en attente d’être envoyés ou reçus pour être immédiatement téléchargé ou téléchargé.</span><span class="sxs-lookup"><span data-stu-id="44970-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="44970-130">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="44970-130">**Required properties**</span></span>|<span data-ttu-id="44970-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="44970-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44970-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-133">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="44970-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="44970-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-135">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="44970-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="44970-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44970-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="44970-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44970-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="44970-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44970-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="44970-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44970-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="44970-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44970-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44970-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44970-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44970-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="44970-146">Remarks</span></span>

<span data-ttu-id="44970-147">Les objets d’état qui implémente MAPI prennent en charge les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="44970-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="44970-148">**Objet d’état**</span><span class="sxs-lookup"><span data-stu-id="44970-148">**Status object**</span></span>|<span data-ttu-id="44970-149">**Méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="44970-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44970-150">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="44970-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="44970-151">**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="44970-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="44970-152">Carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="44970-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="44970-153">**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="44970-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="44970-154">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="44970-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="44970-155">**ValidateState** et **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="44970-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="44970-156">Les objets d’état qui implémente MAPI sont requis pour une version en lecture seule des méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et pour prendre en charge la méthode **ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="44970-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="44970-157">Fournisseurs de transport doivent également en charge **FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="44970-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="44970-158">Tous les fournisseurs doivent prendre en charge de **dialogue**; prise en charge **ChangePassword** est facultative.</span><span class="sxs-lookup"><span data-stu-id="44970-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="44970-159">Clients utilisent les objets d’état pour effectuer la configuration et en savoir plus sur l’état de la session.</span><span class="sxs-lookup"><span data-stu-id="44970-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="44970-160">Ils accéder à un objet d’état en appelant la méthode **OpenStatusEntry** d’un objet de connexion de fournisseur de service ou la méthode [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="44970-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44970-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44970-161">See also</span></span>



[<span data-ttu-id="44970-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="44970-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


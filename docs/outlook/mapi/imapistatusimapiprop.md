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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408298"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="88c79-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="88c79-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="88c79-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88c79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88c79-105">Fournit des informations d’état sur le sous-système MAPI, le carnet d’adresses intégré et lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="88c79-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="88c79-106">Un fournisseur de services implémente **IMAPIStatus** pour fournir des informations sur son propre état.</span><span class="sxs-lookup"><span data-stu-id="88c79-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88c79-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="88c79-107">Header file:</span></span>  <br/> |<span data-ttu-id="88c79-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88c79-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="88c79-109">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="88c79-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="88c79-110">Objets de statut</span><span class="sxs-lookup"><span data-stu-id="88c79-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="88c79-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="88c79-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="88c79-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="88c79-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="88c79-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="88c79-113">Called by:</span></span>  <br/> |<span data-ttu-id="88c79-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="88c79-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="88c79-115">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="88c79-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="88c79-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="88c79-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="88c79-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="88c79-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="88c79-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="88c79-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="88c79-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="88c79-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="88c79-120">Non traduit</span><span class="sxs-lookup"><span data-stu-id="88c79-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="88c79-121">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="88c79-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="88c79-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="88c79-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="88c79-123">Confirme les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="88c79-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="88c79-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="88c79-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="88c79-125">Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="88c79-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="88c79-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="88c79-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="88c79-127">Modifie le mot de passe d’un fournisseur de services sans afficher d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c79-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="88c79-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="88c79-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="88c79-129">Force le téléchargement immédiat de tous les messages en attente d’envoi ou de réception.</span><span class="sxs-lookup"><span data-stu-id="88c79-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="88c79-130">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="88c79-130">**Required properties**</span></span>|<span data-ttu-id="88c79-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="88c79-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88c79-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="88c79-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="88c79-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="88c79-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="88c79-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88c79-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="88c79-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88c79-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="88c79-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88c79-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="88c79-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88c79-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="88c79-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88c79-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88c79-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88c79-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88c79-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="88c79-146">Remarks</span></span>

<span data-ttu-id="88c79-147">Les objets d’état implémentés par MAPI supportent les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c79-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="88c79-148">**Objet Status**</span><span class="sxs-lookup"><span data-stu-id="88c79-148">**Status object**</span></span>|<span data-ttu-id="88c79-149">**Méthodes prise en charge**</span><span class="sxs-lookup"><span data-stu-id="88c79-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88c79-150">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="88c79-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="88c79-151">**ValidateState** uniquement</span><span class="sxs-lookup"><span data-stu-id="88c79-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="88c79-152">Carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="88c79-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="88c79-153">**ValidateState** uniquement</span><span class="sxs-lookup"><span data-stu-id="88c79-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="88c79-154">Pooler MAPI</span><span class="sxs-lookup"><span data-stu-id="88c79-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="88c79-155">**ValidateState** et **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="88c79-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="88c79-156">Les objets d’état implémentés par MAPI doivent avoir une version en lecture seule des méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et prendre en charge la **méthode ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="88c79-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="88c79-157">Les fournisseurs de transport doivent également prendre **en charge FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="88c79-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="88c79-158">Tous les fournisseurs doivent prendre en charge **SettingsDialog**; la prise **en charge de ChangePassword** est facultative.</span><span class="sxs-lookup"><span data-stu-id="88c79-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="88c79-159">Les clients utilisent des objets d’état pour effectuer la configuration et pour en savoir plus sur l’état de la session.</span><span class="sxs-lookup"><span data-stu-id="88c79-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="88c79-160">Ils accèdent à un objet d’état en appelant la méthode **OpenStatusEntry** d’un objet d’ouverture de connecté de fournisseur de services ou la méthode [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="88c79-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88c79-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88c79-161">See also</span></span>



[<span data-ttu-id="88c79-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="88c79-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


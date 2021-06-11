---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418105"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="2f860-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f860-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="2f860-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f860-105">Prend en charge l’accès Microsoft Exchange Server objets table, en particulier les objets de table de liste de contrôle d’accès système (SACL) et les objets de table de règles sur Microsoft Exchange Server dossiers.</span><span class="sxs-lookup"><span data-stu-id="2f860-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="2f860-106">Cette interface ressemble à l’interface [IMAPITable : IUnknown,](imapitableiunknown.md) mais elle ajoute la prise en charge des structures spécifiques Microsoft Exchange Server utilisées pour contrôler les règles et les saclabes.</span><span class="sxs-lookup"><span data-stu-id="2f860-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f860-107">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="2f860-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="2f860-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="2f860-108">None</span></span>  <br/> |
|<span data-ttu-id="2f860-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2f860-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f860-110">Objets de table de serveur</span><span class="sxs-lookup"><span data-stu-id="2f860-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="2f860-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2f860-111">Called by:</span></span>  <br/> |<span data-ttu-id="2f860-112">MAPI et applications clientes</span><span class="sxs-lookup"><span data-stu-id="2f860-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="2f860-113">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="2f860-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2f860-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="2f860-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="2f860-115">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="2f860-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="2f860-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="2f860-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="2f860-117">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="2f860-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="2f860-118">Transacted</span><span class="sxs-lookup"><span data-stu-id="2f860-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2f860-119">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="2f860-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2f860-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2f860-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="2f860-121">Renvoie des informations sur la dernière erreur qui s’est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="2f860-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="2f860-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="2f860-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="2f860-123">Renvoie un pointeur vers une interface pour un objet table MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f860-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="2f860-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="2f860-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="2f860-125">Met à jour un objet table MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f860-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="2f860-126">**Propriétés utilisées pour modifier une table de règles**</span><span class="sxs-lookup"><span data-stu-id="2f860-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="2f860-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="2f860-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f860-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="2f860-148">**Propriétés utilisées pour modifier une table SACL**</span><span class="sxs-lookup"><span data-stu-id="2f860-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="2f860-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="2f860-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f860-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="2f860-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2f860-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2f860-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f860-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f860-158">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f860-158">Remarks</span></span>

<span data-ttu-id="2f860-159">Pour obtenir l’interface **IExchangeModifyTable,** appelez la méthode MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet dossier.</span><span class="sxs-lookup"><span data-stu-id="2f860-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="2f860-160">Lorsque vous appelez **la méthode OpenProperty,** passez la **valeur IID_IExchangeModifyTable** dans le _paramètre lpiid._</span><span class="sxs-lookup"><span data-stu-id="2f860-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2f860-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f860-161">See also</span></span>



[<span data-ttu-id="2f860-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2f860-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 51a83e1e28534cc237419d9c4ae475c1d719c5de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565073"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="3e866-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e866-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="3e866-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e866-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e866-105">Prend en charge l’accès aux objets de table de Microsoft Exchange Server, spécifiquement l’accès système contrôler des objets liste (SACL) du tableau objets de la table des dossiers Microsoft Exchange Server de la règle.</span><span class="sxs-lookup"><span data-stu-id="3e866-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="3e866-106">Cette interface ressemble à la [IMAPITable : IUnknown](imapitableiunknown.md) interface, mais elle ajoute la prise en charge pour les structures spécifiques à Microsoft Exchange Server qui sont utilisés pour contrôler les règles et SACL.</span><span class="sxs-lookup"><span data-stu-id="3e866-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e866-107">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="3e866-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="3e866-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="3e866-108">None</span></span>  <br/> |
|<span data-ttu-id="3e866-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="3e866-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="3e866-110">Objets de table de serveur</span><span class="sxs-lookup"><span data-stu-id="3e866-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="3e866-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="3e866-111">Called by:</span></span>  <br/> |<span data-ttu-id="3e866-112">Applications MAPI et client</span><span class="sxs-lookup"><span data-stu-id="3e866-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="3e866-113">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="3e866-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3e866-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="3e866-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="3e866-115">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="3e866-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="3e866-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="3e866-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="3e866-117">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="3e866-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="3e866-118">Traitées</span><span class="sxs-lookup"><span data-stu-id="3e866-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3e866-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="3e866-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3e866-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3e866-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="3e866-121">Retourne des informations sur la dernière erreur qui s’est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="3e866-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="3e866-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="3e866-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="3e866-123">Retourne un pointeur vers une interface pour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e866-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="3e866-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="3e866-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="3e866-125">Met à jour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e866-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="3e866-126">**Propriétés utilisées pour modifier une table de règles**</span><span class="sxs-lookup"><span data-stu-id="3e866-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="3e866-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="3e866-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e866-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="3e866-148">**Propriétés utilisées pour modifier une table SACL**</span><span class="sxs-lookup"><span data-stu-id="3e866-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="3e866-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="3e866-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e866-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="3e866-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e866-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3e866-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e866-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e866-158">Remarques</span><span class="sxs-lookup"><span data-stu-id="3e866-158">Remarks</span></span>

<span data-ttu-id="3e866-159">Pour obtenir l’interface **IExchangeModifyTable** , appelez la méthode MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet folder.</span><span class="sxs-lookup"><span data-stu-id="3e866-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="3e866-160">Lorsque vous appelez la méthode **OpenProperty** , transmettez la valeur **IID_IExchangeModifyTable** dans le paramètre _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="3e866-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e866-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e866-161">See also</span></span>



[<span data-ttu-id="3e866-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3e866-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


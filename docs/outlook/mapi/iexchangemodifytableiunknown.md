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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783677"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="3442f-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3442f-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="3442f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3442f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3442f-105">Prend en charge l’accès aux objets de table de Microsoft Exchange Server, spécifiquement l’accès système contrôler des objets liste (SACL) du tableau objets de la table des dossiers Microsoft Exchange Server de la règle.</span><span class="sxs-lookup"><span data-stu-id="3442f-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="3442f-106">Cette interface ressemble à la [IMAPITable : IUnknown](imapitableiunknown.md) interface, mais elle ajoute la prise en charge pour les structures spécifiques à Microsoft Exchange Server qui sont utilisés pour contrôler les règles et SACL.</span><span class="sxs-lookup"><span data-stu-id="3442f-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3442f-107">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="3442f-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="3442f-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="3442f-108">None</span></span>  <br/> |
|<span data-ttu-id="3442f-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="3442f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="3442f-110">Objets de table de serveur</span><span class="sxs-lookup"><span data-stu-id="3442f-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="3442f-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="3442f-111">Called by:</span></span>  <br/> |<span data-ttu-id="3442f-112">Applications MAPI et client</span><span class="sxs-lookup"><span data-stu-id="3442f-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="3442f-113">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="3442f-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3442f-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="3442f-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="3442f-115">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="3442f-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="3442f-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="3442f-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="3442f-117">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="3442f-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="3442f-118">Traitées</span><span class="sxs-lookup"><span data-stu-id="3442f-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3442f-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="3442f-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3442f-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3442f-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="3442f-121">Retourne des informations sur la dernière erreur qui s’est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="3442f-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="3442f-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="3442f-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="3442f-123">Retourne un pointeur vers une interface pour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="3442f-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="3442f-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="3442f-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="3442f-125">Met à jour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="3442f-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="3442f-126">**Propriétés utilisées pour modifier une table de règles**</span><span class="sxs-lookup"><span data-stu-id="3442f-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="3442f-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="3442f-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3442f-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="3442f-148">**Propriétés utilisées pour modifier une table SACL**</span><span class="sxs-lookup"><span data-stu-id="3442f-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="3442f-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="3442f-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3442f-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="3442f-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3442f-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3442f-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3442f-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3442f-158">Remarques</span><span class="sxs-lookup"><span data-stu-id="3442f-158">Remarks</span></span>

<span data-ttu-id="3442f-159">Pour obtenir l’interface **IExchangeModifyTable** , appelez la méthode MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet folder.</span><span class="sxs-lookup"><span data-stu-id="3442f-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="3442f-160">Lorsque vous appelez la méthode **OpenProperty** , transmettez la valeur **IID_IExchangeModifyTable** dans le paramètre _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="3442f-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3442f-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3442f-161">See also</span></span>



[<span data-ttu-id="3442f-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3442f-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


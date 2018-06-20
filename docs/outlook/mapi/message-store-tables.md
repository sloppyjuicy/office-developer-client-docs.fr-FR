---
title: Tables de la banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784895"
---
# <a name="message-store-tables"></a><span data-ttu-id="33c34-103">Tables de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="33c34-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="33c34-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33c34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33c34-105">La table contient des informations sur les fournisseurs de banque de messages dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="33c34-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="33c34-106">Il existe une table de banque de messages pour chaque session MAPI, implémentés par MAPI et utilisé par les clients.</span><span class="sxs-lookup"><span data-stu-id="33c34-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="33c34-107">Clients peuvent utiliser ce tableau, par exemple, pour rechercher toutes les instances d’un fournisseur spécifique ou pour localiser un message spécifique.</span><span class="sxs-lookup"><span data-stu-id="33c34-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="33c34-108">La table est dynamique.</span><span class="sxs-lookup"><span data-stu-id="33c34-108">The message store table is dynamic.</span></span> <span data-ttu-id="33c34-109">Si l’utilisateur d’une application cliente modifie le profil, modification de la banque de messages par défaut, par exemple, les valeurs de l' **PR_DEFAULT_STORE** pour les banques de messages affectés sont immédiatement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="33c34-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="33c34-110">Clients accèdent à la table en appelant la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="33c34-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="33c34-111">Les propriétés suivantes constituent la colonne requise dans la table de la banque de message :</span><span class="sxs-lookup"><span data-stu-id="33c34-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33c34-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33c34-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33c34-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33c34-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33c34-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33c34-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33c34-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33c34-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33c34-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33c34-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33c34-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33c34-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33c34-122">See also</span></span>



[<span data-ttu-id="33c34-123">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="33c34-123">MAPI Tables</span></span>](mapi-tables.md)


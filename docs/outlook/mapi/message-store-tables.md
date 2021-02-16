---
title: Tables de la boutique de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405351"
---
# <a name="message-store-tables"></a><span data-ttu-id="11f91-103">Tables de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="11f91-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="11f91-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11f91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11f91-105">La table de la boutique de messages contient des informations sur les fournisseurs de magasins de messages dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="11f91-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="11f91-106">Il existe une table de magasin de messages pour chaque session MAPI, implémentée par MAPI et utilisée par les clients.</span><span class="sxs-lookup"><span data-stu-id="11f91-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="11f91-107">Les clients peuvent utiliser cette table, par exemple, pour localiser toutes les instances d’un fournisseur particulier ou pour localiser une magasin de messages spécifique.</span><span class="sxs-lookup"><span data-stu-id="11f91-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="11f91-108">La table de la boutique de messages est dynamique.</span><span class="sxs-lookup"><span data-stu-id="11f91-108">The message store table is dynamic.</span></span> <span data-ttu-id="11f91-109">Si l’utilisateur d’une application cliente modifie le profil, en modifiant la boutique de messages par défaut, par exemple, les valeurs des propriétés **PR_DEFAULT_STORE** des magasins de messages affectés sont immédiatement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="11f91-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="11f91-110">Les clients accèdent à la table de la boutique de messages en appelant la méthode [IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md)</span><span class="sxs-lookup"><span data-stu-id="11f91-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="11f91-111">Les propriétés suivantes définissent la colonne requise dans la table de la boutique de messages :</span><span class="sxs-lookup"><span data-stu-id="11f91-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11f91-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="11f91-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="11f91-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="11f91-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="11f91-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="11f91-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="11f91-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="11f91-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="11f91-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="11f91-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="11f91-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11f91-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11f91-122">See also</span></span>



[<span data-ttu-id="11f91-123">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="11f91-123">MAPI Tables</span></span>](mapi-tables.md)


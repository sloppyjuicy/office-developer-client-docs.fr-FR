---
title: Tables de banque de messages
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
# <a name="message-store-tables"></a><span data-ttu-id="c7f3a-103">Tables de banque de messages</span><span class="sxs-lookup"><span data-stu-id="c7f3a-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="c7f3a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7f3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7f3a-105">La table de banque de messages contient des informations sur les fournisseurs de banques de messages dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="c7f3a-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="c7f3a-106">Il existe une table de banque de messages pour chaque session MAPI, implémentée par MAPI et utilisée par les clients.</span><span class="sxs-lookup"><span data-stu-id="c7f3a-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="c7f3a-107">Les clients peuvent utiliser cette table, par exemple, pour rechercher toutes les instances d'un fournisseur particulier ou pour localiser une banque de messages spécifique.</span><span class="sxs-lookup"><span data-stu-id="c7f3a-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="c7f3a-108">La table de banque de messages est dynamique.</span><span class="sxs-lookup"><span data-stu-id="c7f3a-108">The message store table is dynamic.</span></span> <span data-ttu-id="c7f3a-109">Si l'utilisateur d'une application cliente modifie le profil, en modifiant la Banque de messages par défaut, par exemple, les valeurs des propriétés **PR_DEFAULT_STORE** pour les banques de messages affectées sont immédiatement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="c7f3a-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="c7f3a-110">Les clients accèdent à la table de banque de messages en appelant la méthode [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="c7f3a-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="c7f3a-111">Les propriétés suivantes constituent le jeu de colonnes obligatoire dans la table de banque de messages:</span><span class="sxs-lookup"><span data-stu-id="c7f3a-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7f3a-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c7f3a-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="c7f3a-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c7f3a-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="c7f3a-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c7f3a-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="c7f3a-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c7f3a-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="c7f3a-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c7f3a-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7f3a-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7f3a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7f3a-122">See also</span></span>



[<span data-ttu-id="c7f3a-123">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="c7f3a-123">MAPI Tables</span></span>](mapi-tables.md)


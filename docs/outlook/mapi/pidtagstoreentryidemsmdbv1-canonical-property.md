---
title: Propriété canonique PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 505ea9ba5d7105f20f335035e42286fdab1cb1aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576322"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="621eb-103">Propriété canonique PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="621eb-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="621eb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="621eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="621eb-105">Contient l’ancien style (Microsoft Outlook 2002 et versions antérieures) de l’identificateur d’entrée d’une banque de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="621eb-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="621eb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="621eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="621eb-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="621eb-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="621eb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="621eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="621eb-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="621eb-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="621eb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="621eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="621eb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="621eb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="621eb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="621eb-112">Area:</span></span>  <br/> |<span data-ttu-id="621eb-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="621eb-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="621eb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="621eb-114">Remarks</span></span>

<span data-ttu-id="621eb-115">À partir de Microsoft Outlook 2003, le nom de domaine complet ont été intégrées aux identificateurs d’entrée, en évitant RPC supplémentaires pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="621eb-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="621eb-116">Toutefois, cela rend plus identificateurs d’entrée et présente d’autres scénarios où la méthode **CompareEntryIDs** doit être utilisée pour déterminer si l’entrée deux ID sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="621eb-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="621eb-117">Le PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) propriété accède à l’ancien format de l’identificateur d’entrée Exchange Server utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="621eb-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="621eb-118">Vous pouvez économiser de l’espace et également réduire le nombre d’appels **CompareEntryIDs** nécessaires pour déterminer le moment de l’entrée ID sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="621eb-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="621eb-119">Notez que pour ouvrir une boîte aux lettres à l’aide de l’identificateur d’entrée plus ancien peut entraîner des appels RPC supplémentaires si une référence est requise.</span><span class="sxs-lookup"><span data-stu-id="621eb-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="621eb-120">Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez ignorer le cache à l’aide de l’indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="621eb-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="621eb-121">Si **PR_STORE_ENTRYID_EMSMDB_V1** n’est pas disponible, le code doit revient à PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="621eb-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="621eb-122">Uniquement Outlook 2003 par le biais de Microsoft Outlook 2013 prend en charge la propriété PR_STORE_ENTRYID_EMSMDB_V1.</span><span class="sxs-lookup"><span data-stu-id="621eb-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="621eb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="621eb-123">See also</span></span>



[<span data-ttu-id="621eb-124">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="621eb-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="621eb-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="621eb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="621eb-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="621eb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="621eb-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="621eb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="621eb-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="621eb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


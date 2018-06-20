---
title: Propriété canonique PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786837"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="6c38c-103">Propriété canonique PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="6c38c-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="6c38c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c38c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c38c-105">Contient l’ancien style (Microsoft Outlook 2002 et versions antérieures) de l’identificateur d’entrée d’une banque de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6c38c-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c38c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6c38c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c38c-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="6c38c-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="6c38c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6c38c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c38c-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="6c38c-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="6c38c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6c38c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c38c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6c38c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6c38c-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6c38c-112">Area:</span></span>  <br/> |<span data-ttu-id="6c38c-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="6c38c-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c38c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c38c-114">Remarks</span></span>

<span data-ttu-id="6c38c-115">À partir de Microsoft Outlook 2003, le nom de domaine complet ont été intégrées aux identificateurs d’entrée, en évitant RPC supplémentaires pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="6c38c-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="6c38c-116">Toutefois, cela rend plus identificateurs d’entrée et présente d’autres scénarios où la méthode **CompareEntryIDs** doit être utilisée pour déterminer si l’entrée deux ID sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="6c38c-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="6c38c-117">Le PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) propriété accède à l’ancien format de l’identificateur d’entrée Exchange Server utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="6c38c-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="6c38c-118">Vous pouvez économiser de l’espace et également réduire le nombre d’appels **CompareEntryIDs** nécessaires pour déterminer le moment de l’entrée ID sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="6c38c-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="6c38c-119">Notez que pour ouvrir une boîte aux lettres à l’aide de l’identificateur d’entrée plus ancien peut entraîner des appels RPC supplémentaires si une référence est requise.</span><span class="sxs-lookup"><span data-stu-id="6c38c-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="6c38c-120">Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez ignorer le cache à l’aide de l’indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="6c38c-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="6c38c-121">Si **PR_STORE_ENTRYID_EMSMDB_V1** n’est pas disponible, le code doit revient à PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="6c38c-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="6c38c-122">Uniquement Outlook 2003 par le biais de Microsoft Outlook 2013 prend en charge la propriété PR_STORE_ENTRYID_EMSMDB_V1.</span><span class="sxs-lookup"><span data-stu-id="6c38c-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c38c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c38c-123">See also</span></span>



[<span data-ttu-id="6c38c-124">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="6c38c-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="6c38c-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6c38c-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c38c-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6c38c-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c38c-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6c38c-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c38c-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6c38c-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


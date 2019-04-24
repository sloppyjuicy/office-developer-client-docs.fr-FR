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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278770"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="a60d4-103">Propriété canonique PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="a60d4-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="a60d4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a60d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a60d4-105">Contient l'ancien style (Microsoft Outlook 2002 et versions antérieures) de l'identificateur d'entrée d'une banque de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a60d4-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a60d4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a60d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a60d4-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="a60d4-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="a60d4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a60d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a60d4-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="a60d4-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="a60d4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a60d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="a60d4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a60d4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a60d4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a60d4-112">Area:</span></span>  <br/> |<span data-ttu-id="a60d4-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="a60d4-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a60d4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a60d4-114">Remarks</span></span>

<span data-ttu-id="a60d4-115">À partir de Microsoft Outlook 2003, les noms de domaine complets du serveur ont été intégrés aux identificateurs d'entrée, ce qui permet d'éviter les appels RPC supplémentaires pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="a60d4-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="a60d4-116">Toutefois, cela complique davantage les ID d'entrée et présente des scénarios dans lesquels la méthode **CompareEntryIDs** doit être utilisée pour déterminer si deux identificateurs d'entrée sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="a60d4-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="a60d4-117">La propriété PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) accède à l'ancien format de l'ID d'entrée du serveur Exchange utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="a60d4-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="a60d4-118">Cela permet d'économiser de l'espace et de réduire le nombre d'appels **CompareEntryIDs** nécessaires pour déterminer quand les ID d'entrée sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="a60d4-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="a60d4-119">Notez que l'utilisation des anciens ID d'entrée pour ouvrir une boîte aux lettres peut entraîner des appels RPC supplémentaires si une référence est requise.</span><span class="sxs-lookup"><span data-stu-id="a60d4-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="a60d4-120">Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez ignorer le cache à l'aide de l'indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a60d4-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="a60d4-121">Si **PR_STORE_ENTRYID_EMSMDB_V1** n'est pas disponible, le code doit revenir à PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="a60d4-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="a60d4-122">Seul Outlook 2003 via Microsoft Outlook 2013 prend en charge la propriété PR_STORE_ENTRYID_EMSMDB_V1.</span><span class="sxs-lookup"><span data-stu-id="a60d4-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a60d4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a60d4-123">See also</span></span>



[<span data-ttu-id="a60d4-124">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="a60d4-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="a60d4-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a60d4-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a60d4-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a60d4-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a60d4-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a60d4-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a60d4-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a60d4-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


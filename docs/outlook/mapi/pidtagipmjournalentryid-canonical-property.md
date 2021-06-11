---
title: Propriété canonique PidTagIpmJournalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmJournalEntryId
api_type:
- HeaderDef
ms.assetid: a3765b9d-a108-46d7-a97c-a825ae3980be
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b5dfc378a2558e906bec018608e2d2c776090c06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327908"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a><span data-ttu-id="67a91-103">Propriété canonique PidTagIpmJournalEntryId</span><span class="sxs-lookup"><span data-stu-id="67a91-103">PidTagIpmJournalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="67a91-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67a91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67a91-105">Contient **l’EntryID** du dossier Outlook Journal.</span><span class="sxs-lookup"><span data-stu-id="67a91-105">Contains the **EntryID** of the Outlook Journal folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67a91-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="67a91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67a91-107">PR_IPM_JOURNAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="67a91-107">PR_IPM_JOURNAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="67a91-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="67a91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67a91-109">0x36D2</span><span class="sxs-lookup"><span data-stu-id="67a91-109">0x36D2</span></span>  <br/> |
|<span data-ttu-id="67a91-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="67a91-110">Data type:</span></span>  <br/> |<span data-ttu-id="67a91-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="67a91-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="67a91-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="67a91-112">Area:</span></span>  <br/> |<span data-ttu-id="67a91-113">Dossier</span><span class="sxs-lookup"><span data-stu-id="67a91-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67a91-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="67a91-114">Remarks</span></span>

<span data-ttu-id="67a91-115">Cette propriété est stockée dans le dossier Boîte de réception, ainsi que dans le dossier racine de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="67a91-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="67a91-116">Pour accéder à la propriété d’une magasin de messages spécifique, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="67a91-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="67a91-117">Tout d’abord, recherchez la propriété dans le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="67a91-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="67a91-118">Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **EntryID** pour le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="67a91-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="67a91-119">Si **IMsgStore::GetReceiveFolder** réussit, utilisez la référence à **EntryID** de la boîte de réception et [de l’IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et obtenir une référence à un objet **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="67a91-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="67a91-120">Si **IMsgStore::OpenEntry** réussit, utilisez la référence renvoyée à l’objet **IMAPIFolder** et [à IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="67a91-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="67a91-121">Si l’étape 1, 2 ou 3 échoue, recherchez la propriété dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="67a91-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="67a91-122">Pour ce faire, utilisez **IMsgStore::OpenEntry**, en spécifiant NULL pour **lpEntryID,** pour ouvrir le dossier racine de la magasin de messages et obtenir une référence à l’objet **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="67a91-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="67a91-123">Si l’ouverture du dossier racine réussit, utilisez la référence renvoyée à l’objet **IMAPIFolder** et **à IMAPIProp::GetProps** pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="67a91-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="67a91-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="67a91-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67a91-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="67a91-125">Protocol specifications</span></span>

<span data-ttu-id="67a91-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67a91-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67a91-127">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="67a91-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67a91-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67a91-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67a91-129">Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="67a91-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="67a91-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67a91-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67a91-131">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67a91-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67a91-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="67a91-132">Header files</span></span>

<span data-ttu-id="67a91-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67a91-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="67a91-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="67a91-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="67a91-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67a91-135">Mapitags.h</span></span>
  
> <span data-ttu-id="67a91-136">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="67a91-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67a91-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67a91-137">See also</span></span>



[<span data-ttu-id="67a91-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="67a91-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67a91-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="67a91-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67a91-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="67a91-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67a91-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="67a91-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


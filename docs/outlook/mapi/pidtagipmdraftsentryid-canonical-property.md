---
title: Propriété canonique PidTagIpmDraftsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e259c86803147d782469c8d86b23694d8b54e69d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386396"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a><span data-ttu-id="a7ea1-103">Propriété canonique PidTagIpmDraftsEntryId</span><span class="sxs-lookup"><span data-stu-id="a7ea1-103">PidTagIpmDraftsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a7ea1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7ea1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7ea1-105">Contient **propriété EntryID** du dossier Brouillons d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-105">Contains the **EntryID** of the Outlook Drafts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7ea1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7ea1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7ea1-107">PR_IPM_DRAFTS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a7ea1-107">PR_IPM_DRAFTS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a7ea1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a7ea1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7ea1-109">0x36D7</span><span class="sxs-lookup"><span data-stu-id="a7ea1-109">0x36D7</span></span>  <br/> |
|<span data-ttu-id="a7ea1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7ea1-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7ea1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a7ea1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a7ea1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a7ea1-112">Area:</span></span>  <br/> |<span data-ttu-id="a7ea1-113">Folder</span><span class="sxs-lookup"><span data-stu-id="a7ea1-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7ea1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7ea1-114">Remarks</span></span>

<span data-ttu-id="a7ea1-115">Cette propriété est stockée dans le dossier boîte de réception, ainsi que le dossier racine de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="a7ea1-116">Pour accéder à la propriété sur une banque de messages spécifique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a7ea1-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="a7ea1-117">Tout d’abord, recherchez la propriété dans le dossier boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="a7ea1-118">Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **propriété EntryID** du dossier boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="a7ea1-119">Si **IMsgStore::GetReceiveFolder** se déroule correctement, puis utilisez la référence à **propriété EntryID** de la boîte de réception et [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et d’obtenir une référence à un objet **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="a7ea1-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="a7ea1-120">Si **IMsgStore::OpenEntry** se déroule correctement, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="a7ea1-121">En cas d’échec de l’étape 1, 2 ou 3, recherchez la propriété dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="a7ea1-122">Pour cela, utilisez **IMsgStore::OpenEntry**, spécifiant la valeur NULL pour **lpEntryID**, pour ouvrir le dossier racine de la banque de messages et d’obtenir une référence à l’objet **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="a7ea1-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="a7ea1-123">Si le dossier racine est réussi, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et **IMAPIProp::GetProps** pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="a7ea1-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7ea1-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7ea1-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a7ea1-125">Protocol specifications</span></span>

<span data-ttu-id="a7ea1-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ea1-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ea1-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7ea1-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ea1-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ea1-129">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7ea1-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a7ea1-130">Header files</span></span>

<span data-ttu-id="a7ea1-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7ea1-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7ea1-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7ea1-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a7ea1-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a7ea1-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="a7ea1-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7ea1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7ea1-135">See also</span></span>



[<span data-ttu-id="a7ea1-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ea1-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7ea1-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ea1-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7ea1-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ea1-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7ea1-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a7ea1-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


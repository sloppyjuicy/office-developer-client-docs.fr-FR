---
title: Propriété canonique PidTagIpmNoteEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1d46110585fb5075041942560b3a8bd5d0b125a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786154"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a><span data-ttu-id="ff326-103">Propriété canonique PidTagIpmNoteEntryId</span><span class="sxs-lookup"><span data-stu-id="ff326-103">PidTagIpmNoteEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ff326-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff326-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff326-105">Contient **propriété EntryID** du dossier Notes Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff326-105">Contains the **EntryID** of the Outlook Notes folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff326-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ff326-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff326-107">PR_IPM_NOTE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ff326-107">PR_IPM_NOTE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ff326-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ff326-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff326-109">0x36D3</span><span class="sxs-lookup"><span data-stu-id="ff326-109">0x36D3</span></span>  <br/> |
|<span data-ttu-id="ff326-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ff326-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff326-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff326-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff326-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ff326-112">Area:</span></span>  <br/> |<span data-ttu-id="ff326-113">Folder</span><span class="sxs-lookup"><span data-stu-id="ff326-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff326-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff326-114">Remarks</span></span>

<span data-ttu-id="ff326-115">Cette propriété est stockée dans le dossier boîte de réception, ainsi que le dossier racine de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ff326-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="ff326-116">Pour accéder à la propriété sur une banque de messages spécifique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ff326-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="ff326-117">Tout d’abord, recherchez la propriété dans le dossier boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="ff326-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="ff326-118">Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **propriété EntryID** du dossier boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="ff326-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="ff326-119">Si ** IMsgStore::GetReceiveFolder ** se déroule correctement, puis utilisez la référence à **propriété EntryID** de la boîte de réception et [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et d’obtenir une référence à un objet **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="ff326-119">If ** IMsgStore::GetReceiveFolder ** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="ff326-120">Si **IMsgStore::OpenEntry** se déroule correctement, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ff326-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="ff326-121">En cas d’échec de l’étape 1, 2 ou 3, recherchez la propriété dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="ff326-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="ff326-122">Pour cela, utilisez **IMsgStore::OpenEntry**, spécifiant la valeur NULL pour **lpEntryID**, pour ouvrir le dossier racine de la banque de messages et d’obtenir une référence à l’objet **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="ff326-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="ff326-123">Si le dossier racine est réussi, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et **IMAPIProp::GetProps** pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ff326-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="ff326-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ff326-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff326-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ff326-125">Protocol specifications</span></span>

<span data-ttu-id="ff326-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff326-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff326-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ff326-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff326-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff326-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff326-129">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ff326-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="ff326-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff326-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff326-131">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff326-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff326-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ff326-132">Header files</span></span>

<span data-ttu-id="ff326-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff326-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff326-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ff326-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff326-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ff326-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ff326-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ff326-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff326-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff326-137">See also</span></span>



[<span data-ttu-id="ff326-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ff326-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff326-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ff326-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff326-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ff326-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff326-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ff326-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriété canonique PidTagIpmAppointmentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d27506edf6eb40f6b244733336b8b381ea941442
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327915"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a><span data-ttu-id="54585-103">Propriété canonique PidTagIpmAppointmentEntryId</span><span class="sxs-lookup"><span data-stu-id="54585-103">PidTagIpmAppointmentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="54585-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54585-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54585-105">Contient **l’EntryID** du dossier Calendrier Outlook dossier.</span><span class="sxs-lookup"><span data-stu-id="54585-105">Contains the **EntryID** of the Outlook Calendar folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54585-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="54585-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54585-107">PR_IPM_APPOINTMENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="54585-107">PR_IPM_APPOINTMENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="54585-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="54585-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54585-109">0x36D0</span><span class="sxs-lookup"><span data-stu-id="54585-109">0x36D0</span></span>  <br/> |
|<span data-ttu-id="54585-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="54585-110">Data type:</span></span>  <br/> |<span data-ttu-id="54585-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="54585-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="54585-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="54585-112">Area:</span></span>  <br/> |<span data-ttu-id="54585-113">Dossier</span><span class="sxs-lookup"><span data-stu-id="54585-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54585-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="54585-114">Remarks</span></span>

<span data-ttu-id="54585-115">Cette propriété est stockée dans le dossier Boîte de réception et dans le dossier racine de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="54585-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="54585-116">Pour accéder à la propriété sur une magasin de messages spécifique, faites ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="54585-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="54585-117">Tout d’abord, recherchez la propriété dans le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="54585-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="54585-118">Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **EntryID** pour le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="54585-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="54585-119">Si **IMsgStore::GetReceiveFolder** réussit, utilisez la référence à **EntryID** de la boîte de réception et [de l’IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et obtenir une référence à un objet **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="54585-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="54585-120">Si **IMsgStore::OpenEntry** réussit, utilisez la référence renvoyée à l’objet **IMAPIFolder** et [à IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="54585-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="54585-121">Si l’étape 1, 2 ou 3 échoue, recherchez la propriété dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="54585-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="54585-122">Pour ce faire, utilisez **IMsgStore::OpenEntry**, en spécifiant NULL pour **lpEntryID,** pour ouvrir le dossier racine de la magasin de messages et obtenir une référence à l’objet **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="54585-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="54585-123">Si l’ouverture du dossier racine réussit, utilisez la référence renvoyée à l’objet **IMAPIFolder** et **à IMAPIProp::GetProps** pour obtenir la propriété souhaitée.</span><span class="sxs-lookup"><span data-stu-id="54585-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="54585-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="54585-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54585-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="54585-125">Protocol specifications</span></span>

<span data-ttu-id="54585-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54585-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54585-127">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="54585-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54585-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54585-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54585-129">Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="54585-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54585-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="54585-130">Header files</span></span>

<span data-ttu-id="54585-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54585-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="54585-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="54585-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="54585-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54585-133">Mapitags.h</span></span>
  
> <span data-ttu-id="54585-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="54585-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54585-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54585-135">See also</span></span>



[<span data-ttu-id="54585-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="54585-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54585-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="54585-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54585-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="54585-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54585-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="54585-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


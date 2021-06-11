---
title: Propriété canonique PidTagStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278749"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="dcc46-103">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="dcc46-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="dcc46-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcc46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcc46-105">Contient l’identificateur d’entrée unique de la boutique de messages où réside un objet.</span><span class="sxs-lookup"><span data-stu-id="dcc46-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcc46-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="dcc46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcc46-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="dcc46-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="dcc46-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="dcc46-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dcc46-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="dcc46-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="dcc46-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dcc46-110">Data type:</span></span>  <br/> |<span data-ttu-id="dcc46-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dcc46-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dcc46-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dcc46-112">Area:</span></span>  <br/> |<span data-ttu-id="dcc46-113">Propriétés de l’ID</span><span class="sxs-lookup"><span data-stu-id="dcc46-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcc46-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="dcc46-114">Remarks</span></span>

<span data-ttu-id="dcc46-115">Cette propriété permet d’ouvrir une magasin de messages avec la méthode [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="dcc46-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="dcc46-116">Il est également utilisé pour ouvrir tout objet qui appartient à la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="dcc46-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="dcc46-117">Pour une magasin de messages, cette propriété est identique à la propriété PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dcc46-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="dcc46-118">Une application cliente peut comparer les deux propriétés à l’aide de la méthode [IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="dcc46-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dcc46-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dcc46-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcc46-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="dcc46-120">Protocol specifications</span></span>

<span data-ttu-id="dcc46-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcc46-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcc46-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="dcc46-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcc46-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcc46-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcc46-124">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="dcc46-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="dcc46-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcc46-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcc46-126">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="dcc46-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="dcc46-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcc46-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcc46-128">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="dcc46-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="dcc46-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcc46-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcc46-130">Partage des dossiers de boîte aux lettres entre clients.</span><span class="sxs-lookup"><span data-stu-id="dcc46-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcc46-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dcc46-131">Header files</span></span>

<span data-ttu-id="dcc46-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dcc46-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcc46-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dcc46-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="dcc46-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dcc46-134">Mapitags.h</span></span>
  
> <span data-ttu-id="dcc46-135">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="dcc46-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcc46-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcc46-136">See also</span></span>



[<span data-ttu-id="dcc46-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dcc46-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcc46-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dcc46-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcc46-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dcc46-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcc46-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dcc46-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


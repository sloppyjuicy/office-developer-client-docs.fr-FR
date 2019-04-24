---
title: Propriété canonique PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316127"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="aced9-103">Propriété canonique PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="aced9-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="aced9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aced9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aced9-105">Contient la valeur TRUE si un message contient au moins une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="aced9-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aced9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aced9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aced9-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="aced9-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="aced9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aced9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aced9-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="aced9-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="aced9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aced9-110">Data type:</span></span>  <br/> |<span data-ttu-id="aced9-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="aced9-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="aced9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="aced9-112">Area:</span></span>  <br/> |<span data-ttu-id="aced9-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="aced9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aced9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aced9-114">Remarks</span></span>

<span data-ttu-id="aced9-115">La Banque de messages copie cette propriété à partir de l'indicateur **MSGFLAG_HASATTACH** de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aced9-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="aced9-116">Une application cliente peut ensuite utiliser **PR_HASATTACH** pour trier les pièces jointes des messages dans une visionneuse de messages.</span><span class="sxs-lookup"><span data-stu-id="aced9-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="aced9-117">La valeur de cette propriété est mise à jour à l'aide de la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="aced9-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aced9-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="aced9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aced9-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="aced9-119">Protocol specifications</span></span>

<span data-ttu-id="aced9-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aced9-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aced9-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="aced9-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aced9-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="aced9-122">Header files</span></span>

<span data-ttu-id="aced9-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="aced9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="aced9-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aced9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="aced9-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="aced9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="aced9-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="aced9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aced9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aced9-127">See also</span></span>



[<span data-ttu-id="aced9-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aced9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aced9-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aced9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aced9-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aced9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aced9-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="aced9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


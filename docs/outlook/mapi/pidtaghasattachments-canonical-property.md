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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397603"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="0842c-103">Propriété canonique PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="0842c-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="0842c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0842c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0842c-105">Contient la valeur TRUE si un message contient au moins une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="0842c-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0842c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0842c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0842c-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="0842c-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="0842c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0842c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0842c-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="0842c-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="0842c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0842c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0842c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0842c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0842c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0842c-112">Area:</span></span>  <br/> |<span data-ttu-id="0842c-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="0842c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0842c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0842c-114">Remarks</span></span>

<span data-ttu-id="0842c-115">La banque de messages copie cette propriété à partir de l’indicateur **MSGFLAG_HASATTACH** de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0842c-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="0842c-116">Une application cliente pouvez ensuite utiliser **PR_HASATTACH** pour effectuer un tri sur les pièces jointes des messages dans l’Observateur d’un message.</span><span class="sxs-lookup"><span data-stu-id="0842c-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="0842c-117">La valeur de que cette propriété est mis à jour avec la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="0842c-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0842c-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0842c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0842c-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0842c-119">Protocol specifications</span></span>

<span data-ttu-id="0842c-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0842c-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0842c-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="0842c-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0842c-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0842c-122">Header files</span></span>

<span data-ttu-id="0842c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0842c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0842c-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0842c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0842c-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0842c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0842c-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0842c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0842c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0842c-127">See also</span></span>



[<span data-ttu-id="0842c-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0842c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0842c-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0842c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0842c-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0842c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0842c-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0842c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


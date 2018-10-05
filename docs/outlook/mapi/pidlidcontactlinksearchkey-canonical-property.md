---
title: Propriété canonique PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387495"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="894c6-103">Propriété canonique PidLidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="894c6-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="894c6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="894c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="894c6-105">Contient la liste des **SearchKeys** pour le contact associé à cet objet de message.</span><span class="sxs-lookup"><span data-stu-id="894c6-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="894c6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="894c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="894c6-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="894c6-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="894c6-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="894c6-108">Property set:</span></span>  <br/> |<span data-ttu-id="894c6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="894c6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="894c6-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="894c6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="894c6-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="894c6-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="894c6-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="894c6-112">Data type:</span></span>  <br/> |<span data-ttu-id="894c6-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="894c6-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="894c6-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="894c6-114">Area:</span></span>  <br/> |<span data-ttu-id="894c6-115">Contact</span><span class="sxs-lookup"><span data-stu-id="894c6-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="894c6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="894c6-116">Remarks</span></span>

|<span data-ttu-id="894c6-117">**Longueur en octets**</span><span class="sxs-lookup"><span data-stu-id="894c6-117">**Length in bytes**</span></span>|<span data-ttu-id="894c6-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="894c6-118">**Description**</span></span>|<span data-ttu-id="894c6-119">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="894c6-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="894c6-120">2</span><span class="sxs-lookup"><span data-stu-id="894c6-120">2</span></span>  <br/> |<span data-ttu-id="894c6-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="894c6-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="894c6-122">Aucune</span><span class="sxs-lookup"><span data-stu-id="894c6-122">None</span></span>  <br/> |
|<span data-ttu-id="894c6-123">variable</span><span class="sxs-lookup"><span data-stu-id="894c6-123">variable</span></span>  <br/> |<span data-ttu-id="894c6-124">Données CléRecherche</span><span class="sxs-lookup"><span data-stu-id="894c6-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="894c6-125">Répète fois ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="894c6-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="894c6-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="894c6-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="894c6-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="894c6-127">Protocol specifications</span></span>

<span data-ttu-id="894c6-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="894c6-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="894c6-129">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="894c6-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="894c6-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="894c6-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="894c6-131">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="894c6-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="894c6-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="894c6-132">Header files</span></span>

<span data-ttu-id="894c6-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="894c6-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="894c6-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="894c6-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="894c6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="894c6-135">See also</span></span>

- [<span data-ttu-id="894c6-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="894c6-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="894c6-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="894c6-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="894c6-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="894c6-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="894c6-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="894c6-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


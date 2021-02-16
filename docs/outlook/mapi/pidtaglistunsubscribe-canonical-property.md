---
title: Propriété canonique PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278878"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="1fadc-103">Propriété canonique PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="1fadc-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="1fadc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fadc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fadc-105">Contient la valeur du champ d’en-tête MIME (Multipurpose Internet Mail Extensions) List-Unsubscribe'en-tête.</span><span class="sxs-lookup"><span data-stu-id="1fadc-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1fadc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1fadc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fadc-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="1fadc-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="1fadc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1fadc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fadc-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="1fadc-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="1fadc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1fadc-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fadc-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1fadc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1fadc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1fadc-112">Area:</span></span>  <br/> |<span data-ttu-id="1fadc-113">Divers</span><span class="sxs-lookup"><span data-stu-id="1fadc-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fadc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1fadc-114">Remarks</span></span>

<span data-ttu-id="1fadc-115">Pour générer un champ List-Unsubscribe'en-tête, les clients doivent définir ces propriétés sur la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="1fadc-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="1fadc-116">Les rédacteurs MIME doivent copier la valeur de ces propriétés dans le List-Unsubscribe d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="1fadc-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="1fadc-117">Pour définir la valeur de ces propriétés liées au serveur de liste, les clients MIME doivent écrire les champs d’en-tête comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1fadc-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="1fadc-118">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="1fadc-118">**Property**</span></span>|<span data-ttu-id="1fadc-119">**Nom de champ d’en-tête préféré**</span><span class="sxs-lookup"><span data-stu-id="1fadc-119">**Preferred header field name**</span></span>|<span data-ttu-id="1fadc-120">**Autre nom de champ d’en-tête**</span><span class="sxs-lookup"><span data-stu-id="1fadc-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1fadc-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="1fadc-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="1fadc-122">List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1fadc-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="1fadc-123">X-List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1fadc-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1fadc-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1fadc-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1fadc-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="1fadc-125">Protocol specifications</span></span>

<span data-ttu-id="1fadc-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fadc-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fadc-127">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="1fadc-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1fadc-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fadc-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fadc-129">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="1fadc-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1fadc-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1fadc-130">Header files</span></span>

<span data-ttu-id="1fadc-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fadc-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fadc-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1fadc-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fadc-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1fadc-133">Mapitags.h</span></span>
  
> <span data-ttu-id="1fadc-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="1fadc-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fadc-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fadc-135">See also</span></span>



[<span data-ttu-id="1fadc-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1fadc-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fadc-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1fadc-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fadc-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1fadc-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fadc-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1fadc-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


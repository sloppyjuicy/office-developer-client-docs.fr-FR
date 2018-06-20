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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 87f5c3fc8475f9795847e4680babb26682608a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786193"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="4a5ec-103">Propriété canonique PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="4a5ec-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="4a5ec-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a5ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a5ec-105">Contient la valeur du champ d’en-tête d’un message Multipurpose Internet Mail Extensions (MIME) vous désinscrire de liste.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a5ec-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4a5ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a5ec-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="4a5ec-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="4a5ec-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4a5ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a5ec-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="4a5ec-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="4a5ec-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4a5ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a5ec-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a5ec-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a5ec-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="4a5ec-112">Area:</span></span>  <br/> |<span data-ttu-id="4a5ec-113">Divers</span><span class="sxs-lookup"><span data-stu-id="4a5ec-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a5ec-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a5ec-114">Remarks</span></span>

<span data-ttu-id="4a5ec-115">Pour générer un champ d’en-tête vous désinscrire de liste, les clients doivent définir ces propriétés à la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="4a5ec-116">Rédacteurs MIME doivent copier la valeur de ces propriétés sur le champ d’en-tête vous désinscrire de liste.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="4a5ec-117">Pour définir la valeur de ces propriétés liées au serveur de la liste, les clients MIME doivent écrire les champs d’en-tête tel que spécifié dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="4a5ec-118">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="4a5ec-118">**Property**</span></span>|<span data-ttu-id="4a5ec-119">**Nom de champ d’en-tête par défaut**</span><span class="sxs-lookup"><span data-stu-id="4a5ec-119">**Preferred header field name**</span></span>|<span data-ttu-id="4a5ec-120">**Nom de champ d’en-tête de substitution**</span><span class="sxs-lookup"><span data-stu-id="4a5ec-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a5ec-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="4a5ec-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="4a5ec-122">Vous désinscrire de liste</span><span class="sxs-lookup"><span data-stu-id="4a5ec-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="4a5ec-123">X-liste-Annuler l’abonnement</span><span class="sxs-lookup"><span data-stu-id="4a5ec-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4a5ec-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4a5ec-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a5ec-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4a5ec-125">Protocol specifications</span></span>

<span data-ttu-id="4a5ec-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a5ec-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a5ec-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a5ec-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a5ec-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a5ec-129">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a5ec-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4a5ec-130">Header files</span></span>

<span data-ttu-id="4a5ec-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a5ec-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a5ec-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a5ec-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4a5ec-133">Mapitags.h</span></span>
  
> <span data-ttu-id="4a5ec-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4a5ec-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a5ec-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a5ec-135">See also</span></span>



[<span data-ttu-id="4a5ec-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4a5ec-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a5ec-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4a5ec-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a5ec-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4a5ec-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a5ec-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4a5ec-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


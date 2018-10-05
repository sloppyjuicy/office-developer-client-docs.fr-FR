---
title: Propriété canonique PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389602"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="c0451-103">Propriété canonique PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="c0451-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="c0451-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0451-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0451-105">Contient la valeur du champ d’en-tête d’un message Multipurpose Internet Mail Extensions (MIME) abonner à la liste.</span><span class="sxs-lookup"><span data-stu-id="c0451-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0451-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c0451-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0451-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="c0451-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="c0451-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c0451-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0451-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="c0451-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="c0451-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c0451-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0451-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0451-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c0451-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c0451-112">Area:</span></span>  <br/> |<span data-ttu-id="c0451-113">Divers</span><span class="sxs-lookup"><span data-stu-id="c0451-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0451-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0451-114">Remarks</span></span>

<span data-ttu-id="c0451-115">Pour générer un champ d’en-tête abonner à la liste, les clients doivent définir la valeur de ces propriétés à la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c0451-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="c0451-116">Rédacteurs MIME doivent copier la valeur de ces propriétés sur le champ en-tête de liste d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0451-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="c0451-117">Pour définir la valeur de propriétés liées au serveur comme celles-ci, les clients MIME doivent écrire les champs d’en-tête tel que spécifié dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c0451-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="c0451-118">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="c0451-118">**Property**</span></span>|<span data-ttu-id="c0451-119">**Nom de champ d’en-tête par défaut**</span><span class="sxs-lookup"><span data-stu-id="c0451-119">**Preferred header field name**</span></span>|<span data-ttu-id="c0451-120">**Nom de champ d’en-tête de substitution**</span><span class="sxs-lookup"><span data-stu-id="c0451-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0451-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="c0451-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="c0451-122">Liste d’abonnement</span><span class="sxs-lookup"><span data-stu-id="c0451-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="c0451-123">S’abonner X-liste</span><span class="sxs-lookup"><span data-stu-id="c0451-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c0451-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c0451-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0451-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c0451-125">Protocol specifications</span></span>

<span data-ttu-id="c0451-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0451-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0451-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c0451-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0451-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0451-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0451-129">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="c0451-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0451-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c0451-130">Header files</span></span>

<span data-ttu-id="c0451-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0451-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0451-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c0451-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0451-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c0451-133">Mapitags.h</span></span>
  
> <span data-ttu-id="c0451-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c0451-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0451-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0451-135">See also</span></span>



[<span data-ttu-id="c0451-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c0451-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0451-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c0451-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0451-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c0451-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0451-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c0451-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


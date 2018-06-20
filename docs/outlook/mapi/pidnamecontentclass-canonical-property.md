---
title: Propriété canonique PidNameContentClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1ad4f83cb9021cef82ce62b6b6f5616a3fc3d118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785582"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="6c754-103">Propriété canonique PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="6c754-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="6c754-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c754-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c754-105">Contient une valeur de champ d’en-tête Content-Class [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="6c754-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c754-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="6c754-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="6c754-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="6c754-107">None</span></span>  <br/> |
|<span data-ttu-id="6c754-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="6c754-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c754-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="6c754-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="6c754-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="6c754-110">Property name:</span></span>  <br/> |<span data-ttu-id="6c754-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="6c754-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="6c754-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6c754-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c754-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c754-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6c754-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="6c754-114">Area:</span></span>  <br/> |<span data-ttu-id="6c754-115">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="6c754-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c754-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c754-116">Remarks</span></span>

<span data-ttu-id="6c754-117">Pour définir la valeur de cette propriété, les clients Message Extensions MIME (Multipurpose Internet) doivent écrire un champ d’en-tête Content-Class avec la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="6c754-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="6c754-118">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Class sur la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6c754-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c754-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6c754-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c754-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6c754-120">Protocol specifications</span></span>

<span data-ttu-id="6c754-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c754-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c754-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="6c754-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c754-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c754-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c754-124">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="6c754-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6c754-125">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c754-125">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c754-126">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="6c754-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c754-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6c754-127">Header files</span></span>

<span data-ttu-id="6c754-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c754-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c754-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6c754-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c754-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c754-130">See also</span></span>



[<span data-ttu-id="6c754-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6c754-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c754-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6c754-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c754-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6c754-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c754-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6c754-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


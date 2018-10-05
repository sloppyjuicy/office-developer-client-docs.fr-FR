---
title: Propriété canonique PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387243"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="edf64-103">Propriété canonique PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="edf64-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="edf64-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edf64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edf64-105">Contient une valeur de champ d’en-tête Accept-Language [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="edf64-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edf64-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="edf64-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="edf64-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="edf64-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="edf64-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="edf64-108">Property set:</span></span>  <br/> |<span data-ttu-id="edf64-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="edf64-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="edf64-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="edf64-110">Property name:</span></span>  <br/> |<span data-ttu-id="edf64-111">Langue acceptée</span><span class="sxs-lookup"><span data-stu-id="edf64-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="edf64-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="edf64-112">Data type:</span></span>  <br/> |<span data-ttu-id="edf64-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="edf64-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="edf64-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="edf64-114">Area:</span></span>  <br/> |<span data-ttu-id="edf64-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="edf64-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edf64-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="edf64-116">Remarks</span></span>

<span data-ttu-id="edf64-117">Pour définir la valeur de cette propriété, les clients Message Extensions MIME (Multipurpose Internet) doivent écrire un champ d’en-tête Accept-Language avec la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="edf64-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="edf64-118">Clients MIME peuvent écrire un champ d’en-tête X-Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="edf64-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="edf64-119">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête à la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="edf64-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="edf64-120">Si les deux champs d’en-tête sont présentes, lecteurs MIME doivent utiliser le champ d’en-tête Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="edf64-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edf64-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="edf64-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edf64-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="edf64-122">Protocol specifications</span></span>

<span data-ttu-id="edf64-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edf64-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edf64-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="edf64-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edf64-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edf64-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edf64-126">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="edf64-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edf64-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="edf64-127">Header files</span></span>

<span data-ttu-id="edf64-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edf64-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="edf64-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="edf64-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edf64-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edf64-130">See also</span></span>



[<span data-ttu-id="edf64-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="edf64-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edf64-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="edf64-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edf64-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="edf64-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edf64-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="edf64-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


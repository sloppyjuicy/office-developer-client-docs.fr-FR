---
title: Propriété canonique PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397792"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="a1670-103">Propriété canonique PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="a1670-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="a1670-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1670-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1670-105">Contient une valeur de champ d’en-tête Content-Base [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="a1670-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1670-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="a1670-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="a1670-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="a1670-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="a1670-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a1670-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1670-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="a1670-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="a1670-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="a1670-110">Property name:</span></span>  <br/> |<span data-ttu-id="a1670-111">Base de contenu</span><span class="sxs-lookup"><span data-stu-id="a1670-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="a1670-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a1670-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1670-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1670-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a1670-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a1670-114">Area:</span></span>  <br/> |<span data-ttu-id="a1670-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="a1670-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1670-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a1670-116">Remarks</span></span>

<span data-ttu-id="a1670-117">Pour définir la valeur de cette propriété, les clients Message Extensions MIME (Multipurpose Internet) doivent écrire la valeur souhaitée pour un champ d’en-tête Content-Base sur une entité MIME qui mappe sur un corps de message.</span><span class="sxs-lookup"><span data-stu-id="a1670-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="a1670-118">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Base sur ce une entité MIME sur la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a1670-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1670-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a1670-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1670-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a1670-120">Protocol specifications</span></span>

<span data-ttu-id="a1670-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1670-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1670-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a1670-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1670-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1670-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1670-124">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="a1670-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1670-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a1670-125">Header files</span></span>

<span data-ttu-id="a1670-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1670-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1670-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a1670-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1670-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1670-128">See also</span></span>



[<span data-ttu-id="a1670-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a1670-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1670-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a1670-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1670-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a1670-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1670-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a1670-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


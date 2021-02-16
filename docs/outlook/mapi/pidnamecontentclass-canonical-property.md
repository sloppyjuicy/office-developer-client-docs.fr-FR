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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356349"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="3e952-103">Propriété canonique PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="3e952-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="3e952-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e952-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e952-105">Contient une valeur de champ d’en-tête de classe de contenu [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="3e952-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e952-106">Noms convivial :</span><span class="sxs-lookup"><span data-stu-id="3e952-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3e952-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="3e952-107">None</span></span>  <br/> |
|<span data-ttu-id="3e952-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3e952-108">Property set:</span></span>  <br/> |<span data-ttu-id="3e952-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="3e952-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="3e952-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="3e952-110">Property name:</span></span>  <br/> |<span data-ttu-id="3e952-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="3e952-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="3e952-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3e952-112">Data type:</span></span>  <br/> |<span data-ttu-id="3e952-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3e952-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3e952-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3e952-114">Area:</span></span>  <br/> |<span data-ttu-id="3e952-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="3e952-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e952-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3e952-116">Remarks</span></span>

<span data-ttu-id="3e952-117">Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message Extensions) doivent écrire un champ d’en-tête Content-Class avec la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3e952-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="3e952-118">Les lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Class sur la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3e952-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3e952-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3e952-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e952-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3e952-120">Protocol specifications</span></span>

<span data-ttu-id="3e952-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e952-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e952-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="3e952-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e952-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e952-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e952-124">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="3e952-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="3e952-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e952-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e952-126">Spécifie les propriétés des messages codés gérés par des droits.</span><span class="sxs-lookup"><span data-stu-id="3e952-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e952-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3e952-127">Header files</span></span>

<span data-ttu-id="3e952-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e952-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e952-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3e952-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e952-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e952-130">See also</span></span>



[<span data-ttu-id="3e952-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3e952-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e952-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3e952-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e952-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3e952-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e952-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3e952-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


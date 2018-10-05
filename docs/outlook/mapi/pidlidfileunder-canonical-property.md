---
title: Propriété canonique PidLidFileUnder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393566"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="62ed5-103">Propriété canonique PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="62ed5-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="62ed5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62ed5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62ed5-105">Spécifie le nom sous lequel le contact est déposé lors de l’affichage d’une liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="62ed5-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62ed5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="62ed5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62ed5-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="62ed5-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="62ed5-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="62ed5-108">Property set:</span></span>  <br/> |<span data-ttu-id="62ed5-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="62ed5-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="62ed5-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="62ed5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="62ed5-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="62ed5-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="62ed5-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="62ed5-112">Data type:</span></span>  <br/> |<span data-ttu-id="62ed5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="62ed5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="62ed5-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="62ed5-114">Area:</span></span>  <br/> |<span data-ttu-id="62ed5-115">Contact</span><span class="sxs-lookup"><span data-stu-id="62ed5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62ed5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="62ed5-116">Remarks</span></span>

<span data-ttu-id="62ed5-117">L’application doit traiter cette propriété comme un PT_UNICODE vide s’il est absent du contact.</span><span class="sxs-lookup"><span data-stu-id="62ed5-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62ed5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="62ed5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62ed5-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="62ed5-119">Protocol specifications</span></span>

<span data-ttu-id="62ed5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62ed5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62ed5-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="62ed5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62ed5-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62ed5-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62ed5-123">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="62ed5-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62ed5-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="62ed5-124">Header files</span></span>

<span data-ttu-id="62ed5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62ed5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="62ed5-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="62ed5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62ed5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62ed5-127">See also</span></span>



[<span data-ttu-id="62ed5-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="62ed5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62ed5-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="62ed5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62ed5-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="62ed5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62ed5-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="62ed5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


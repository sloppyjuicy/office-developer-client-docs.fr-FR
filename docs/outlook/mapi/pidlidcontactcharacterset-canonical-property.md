---
title: Propriété canonique PidLidContactCharacterSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9706d1060347609708070140aae51d9dcadbb9c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785122"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="97b90-103">Propriété canonique PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="97b90-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="97b90-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97b90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97b90-105">Spécifie le jeu de caractères utilisé pour ce contact.</span><span class="sxs-lookup"><span data-stu-id="97b90-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97b90-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="97b90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97b90-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="97b90-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="97b90-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="97b90-108">Property set:</span></span>  <br/> |<span data-ttu-id="97b90-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="97b90-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="97b90-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="97b90-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="97b90-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="97b90-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="97b90-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="97b90-112">Data type:</span></span>  <br/> |<span data-ttu-id="97b90-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97b90-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97b90-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="97b90-114">Area:</span></span>  <br/> |<span data-ttu-id="97b90-115">Contact</span><span class="sxs-lookup"><span data-stu-id="97b90-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97b90-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="97b90-116">Remarks</span></span>

<span data-ttu-id="97b90-117">Les applications peuvent utiliser cette propriété à l’aide de la génération d’une liste de dépendante de jeu de caractères de choix pour les **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) et **dispidFileUnderId **Propriétés ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="97b90-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="97b90-118">Si la valeur de la propriété est « 0 x 00000000 » ou « 0 x 00000001 », les applications doivent traiter la propriété comme n’est ne pas défini.</span><span class="sxs-lookup"><span data-stu-id="97b90-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97b90-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="97b90-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97b90-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="97b90-120">Protocol specifications</span></span>

<span data-ttu-id="97b90-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b90-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b90-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="97b90-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97b90-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b90-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b90-124">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="97b90-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97b90-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="97b90-125">Header files</span></span>

<span data-ttu-id="97b90-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97b90-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="97b90-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="97b90-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97b90-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97b90-128">See also</span></span>



[<span data-ttu-id="97b90-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="97b90-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97b90-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="97b90-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97b90-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="97b90-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97b90-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="97b90-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


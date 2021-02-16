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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319704"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="6c279-103">Propriété canonique PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6c279-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="6c279-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c279-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c279-105">Spécifie le jeu de caractères utilisé pour ce contact.</span><span class="sxs-lookup"><span data-stu-id="6c279-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c279-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6c279-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c279-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="6c279-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="6c279-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="6c279-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c279-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6c279-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6c279-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="6c279-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c279-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="6c279-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="6c279-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6c279-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c279-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c279-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c279-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6c279-114">Area:</span></span>  <br/> |<span data-ttu-id="6c279-115">Contact</span><span class="sxs-lookup"><span data-stu-id="6c279-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c279-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c279-116">Remarks</span></span>

<span data-ttu-id="6c279-117">Les applications peuvent utiliser cette propriété pour générer une liste de choix dépendant du jeu de caractères pour les propriétés **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) et **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6c279-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="6c279-118">Si la valeur de la propriété est « 0x00000000 » ou « 0x00000001 », les applications doivent la traiter comme n’étant pas définie.</span><span class="sxs-lookup"><span data-stu-id="6c279-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c279-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6c279-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c279-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6c279-120">Protocol specifications</span></span>

<span data-ttu-id="6c279-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c279-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c279-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="6c279-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c279-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c279-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c279-124">Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="6c279-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c279-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6c279-125">Header files</span></span>

<span data-ttu-id="6c279-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c279-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c279-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6c279-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c279-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c279-128">See also</span></span>



[<span data-ttu-id="6c279-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6c279-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c279-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6c279-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c279-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6c279-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c279-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6c279-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriété canonique PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784980"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="78734-103">Propriété canonique PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="78734-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="78734-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78734-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78734-105">Spécifie les propriétés de l’adresse électronique du contact.</span><span class="sxs-lookup"><span data-stu-id="78734-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78734-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="78734-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78734-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="78734-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="78734-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="78734-108">Property set:</span></span>  <br/> |<span data-ttu-id="78734-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="78734-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="78734-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="78734-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="78734-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="78734-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="78734-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="78734-112">Data type:</span></span>  <br/> |<span data-ttu-id="78734-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="78734-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="78734-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="78734-114">Area:</span></span>  <br/> |<span data-ttu-id="78734-115">Contact</span><span class="sxs-lookup"><span data-stu-id="78734-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78734-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="78734-116">Remarks</span></span>

<span data-ttu-id="78734-117">Chaque valeur PT_LONG dans cette propriété doit être unique dans la propriété et doit être défini sur une des valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="78734-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="78734-118">Si cette propriété est définie, la propriété **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="78734-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="78734-119">Ces deux propriétés doivent être conservées synchronisées entre eux.</span><span class="sxs-lookup"><span data-stu-id="78734-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="78734-120">Par exemple, si une des valeurs de **dispidABPEmailList** est « 0 x 00000000 », puis **dispidABPArrayType** doit avoir le bit « 0 x 00000001 » défini.</span><span class="sxs-lookup"><span data-stu-id="78734-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="78734-121">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="78734-121">**Value**</span></span>|<span data-ttu-id="78734-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="78734-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78734-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78734-123">0x00000000</span></span>  <br/> |<span data-ttu-id="78734-124">E-mail1 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="78734-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="78734-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78734-125">0x00000001</span></span>  <br/> |<span data-ttu-id="78734-126">2 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="78734-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="78734-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="78734-127">0x00000002</span></span>  <br/> |<span data-ttu-id="78734-128">Messagerie3 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="78734-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="78734-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="78734-129">0x00000003</span></span>  <br/> |<span data-ttu-id="78734-130">Télécopie (bureau) est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="78734-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="78734-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="78734-131">0x00000004</span></span>  <br/> |<span data-ttu-id="78734-132">Télécopie (domicile) est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="78734-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="78734-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="78734-133">0x00000005</span></span>  <br/> |<span data-ttu-id="78734-134">Télécopie principal est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="78734-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="78734-135">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="78734-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78734-136">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="78734-136">Protocol specifications</span></span>

<span data-ttu-id="78734-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78734-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78734-138">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="78734-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78734-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78734-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78734-140">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="78734-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78734-141">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="78734-141">Header files</span></span>

<span data-ttu-id="78734-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78734-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="78734-143">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="78734-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78734-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78734-144">See also</span></span>



[<span data-ttu-id="78734-145">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="78734-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78734-146">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="78734-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78734-147">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="78734-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78734-148">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="78734-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


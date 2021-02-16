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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348481"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="462aa-103">Propriété canonique PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="462aa-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="462aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="462aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="462aa-105">Spécifie les propriétés d’adresse électronique définies sur le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="462aa-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="462aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="462aa-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="462aa-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="462aa-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="462aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="462aa-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="462aa-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="462aa-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="462aa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="462aa-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="462aa-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="462aa-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="462aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="462aa-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="462aa-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="462aa-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="462aa-114">Area:</span></span>  <br/> |<span data-ttu-id="462aa-115">Contact</span><span class="sxs-lookup"><span data-stu-id="462aa-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="462aa-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="462aa-116">Remarks</span></span>

<span data-ttu-id="462aa-117">Chaque PT_LONG de cette propriété doit être unique dans la propriété et doit être définie sur l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="462aa-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="462aa-118">Si cette propriété est définie, la propriété **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="462aa-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="462aa-119">Ces deux propriétés doivent être synchronisées l’une avec l’autre.</span><span class="sxs-lookup"><span data-stu-id="462aa-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="462aa-120">Par exemple, si l’une des valeurs dans **dispidABPEmailList** est « 0x00000000 », **dispidABPArrayType** doit avoir le bit « 0x00000001 » définie.</span><span class="sxs-lookup"><span data-stu-id="462aa-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="462aa-121">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="462aa-121">**Value**</span></span>|<span data-ttu-id="462aa-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="462aa-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="462aa-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="462aa-123">0x00000000</span></span>  <br/> |<span data-ttu-id="462aa-124">Email1 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="462aa-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="462aa-125">0x00000001</span></span>  <br/> |<span data-ttu-id="462aa-126">Email2 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="462aa-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="462aa-127">0x00000002</span></span>  <br/> |<span data-ttu-id="462aa-128">Email3 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="462aa-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="462aa-129">0x00000003</span></span>  <br/> |<span data-ttu-id="462aa-130">La télécopie professionnelle est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="462aa-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="462aa-131">0x00000004</span></span>  <br/> |<span data-ttu-id="462aa-132">La télécopie à domicile est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="462aa-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="462aa-133">0x00000005</span></span>  <br/> |<span data-ttu-id="462aa-134">La télécopie principale est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="462aa-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="462aa-135">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="462aa-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="462aa-136">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="462aa-136">Protocol specifications</span></span>

<span data-ttu-id="462aa-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="462aa-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="462aa-138">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="462aa-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="462aa-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="462aa-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="462aa-140">Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="462aa-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="462aa-141">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="462aa-141">Header files</span></span>

<span data-ttu-id="462aa-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="462aa-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="462aa-143">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="462aa-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="462aa-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="462aa-144">See also</span></span>



[<span data-ttu-id="462aa-145">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="462aa-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="462aa-146">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="462aa-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="462aa-147">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="462aa-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="462aa-148">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="462aa-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriété canonique PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d0d5ca3b40f6d46641b805593794827fa99b7fb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593381"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="22ecf-103">Propriété canonique PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="22ecf-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="22ecf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22ecf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22ecf-105">Spécifie l’état de l’adresse électronique du contact et représente un ensemble d’indicateurs de bits.</span><span class="sxs-lookup"><span data-stu-id="22ecf-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22ecf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="22ecf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22ecf-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="22ecf-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="22ecf-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="22ecf-108">Property set:</span></span>  <br/> |<span data-ttu-id="22ecf-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="22ecf-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="22ecf-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="22ecf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="22ecf-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="22ecf-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="22ecf-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="22ecf-112">Data type:</span></span>  <br/> |<span data-ttu-id="22ecf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22ecf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22ecf-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="22ecf-114">Area:</span></span>  <br/> |<span data-ttu-id="22ecf-115">Contact</span><span class="sxs-lookup"><span data-stu-id="22ecf-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22ecf-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="22ecf-116">Remarks</span></span>

<span data-ttu-id="22ecf-117">La valeur de la propriété **dispidABPArrayType** doit être une combinaison des indicateurs qui spécifient l’état de l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="22ecf-118">Indicateurs individuels sont spécifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22ecf-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="22ecf-119">Si cette propriété est définie, la propriété **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) doit être définie.</span><span class="sxs-lookup"><span data-stu-id="22ecf-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="22ecf-120">Ces deux propriétés doivent être conservées synchronisées entre eux.</span><span class="sxs-lookup"><span data-stu-id="22ecf-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="22ecf-121">Par exemple, si **dispidABPArrayType** a le bit « 0 x 00000001 set », une des valeurs de **dispidABPEmailList** doit être « 0 x 00000000 ».</span><span class="sxs-lookup"><span data-stu-id="22ecf-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="22ecf-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="22ecf-122">**Bit**</span></span>|<span data-ttu-id="22ecf-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="22ecf-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22ecf-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="22ecf-124">0x00000001</span></span>  <br/> |<span data-ttu-id="22ecf-125">E-mail1 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="22ecf-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="22ecf-126">0x00000002</span></span>  <br/> |<span data-ttu-id="22ecf-127">2 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="22ecf-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="22ecf-128">0x00000004</span></span>  <br/> |<span data-ttu-id="22ecf-129">Messagerie3 est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="22ecf-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="22ecf-130">0x00000008</span></span>  <br/> |<span data-ttu-id="22ecf-131">Télécopie (bureau) est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="22ecf-132">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="22ecf-132">0x00000010</span></span>  <br/> |<span data-ttu-id="22ecf-133">Télécopie (domicile) est définie pour le contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="22ecf-134">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="22ecf-134">0x00000020</span></span>  <br/> |<span data-ttu-id="22ecf-135">Télécopie principal est défini pour le contact.</span><span class="sxs-lookup"><span data-stu-id="22ecf-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="22ecf-136">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="22ecf-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22ecf-137">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="22ecf-137">Protocol specifications</span></span>

<span data-ttu-id="22ecf-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22ecf-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22ecf-139">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="22ecf-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22ecf-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22ecf-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22ecf-141">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="22ecf-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22ecf-142">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="22ecf-142">Header files</span></span>

<span data-ttu-id="22ecf-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22ecf-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="22ecf-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="22ecf-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22ecf-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22ecf-145">See also</span></span>



[<span data-ttu-id="22ecf-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="22ecf-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22ecf-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="22ecf-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22ecf-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="22ecf-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22ecf-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="22ecf-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


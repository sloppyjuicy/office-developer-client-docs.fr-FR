---
title: Propriété canonique PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357616"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="8a7b0-103">Propriété canonique PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="8a7b0-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="8a7b0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a7b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a7b0-105">Masque de masque qui spécifie le mode de personnalisation d'un message, par exemple, enregistré avec des propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="8a7b0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8a7b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a7b0-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="8a7b0-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="8a7b0-108">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="8a7b0-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8a7b0-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="8a7b0-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="8a7b0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8a7b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a7b0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8a7b0-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a7b0-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a7b0-112">Remarks</span></span>

<span data-ttu-id="8a7b0-113">Pour récupérer la valeur de cette propriété, utilisez d'abord **[IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)** pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans **[IMAPIProp:: GetProps](imapiprop-getprops.md)** pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="8a7b0-114">Les indicateurs possibles sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="8a7b0-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="8a7b0-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="8a7b0-115">**Constant**</span></span>|<span data-ttu-id="8a7b0-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8a7b0-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a7b0-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="8a7b0-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="8a7b0-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="8a7b0-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="8a7b0-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="8a7b0-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="8a7b0-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="8a7b0-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="8a7b0-121">Lors de l'appel de **IMAPIProp:: GetIDsFromNames**, spécifiez les valeurs suivantes pour la structure **[MAPINAMEID](mapinameid.md)** vers laquelle pointe le paramètre d'entrée *lppPropNames* .</span><span class="sxs-lookup"><span data-stu-id="8a7b0-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="8a7b0-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="8a7b0-122">**Member**</span></span>|<span data-ttu-id="8a7b0-123">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8a7b0-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a7b0-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="8a7b0-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="8a7b0-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8a7b0-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8a7b0-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="8a7b0-126">ulKind:</span></span>  <br/> |<span data-ttu-id="8a7b0-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="8a7b0-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="8a7b0-128">Type. couvercle:</span><span class="sxs-lookup"><span data-stu-id="8a7b0-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="8a7b0-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="8a7b0-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8a7b0-130">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="8a7b0-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a7b0-131">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8a7b0-131">Protocol specifications</span></span>

<span data-ttu-id="8a7b0-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a7b0-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a7b0-133">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a7b0-134">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="8a7b0-134">Header files</span></span>

<span data-ttu-id="8a7b0-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8a7b0-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a7b0-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a7b0-137">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8a7b0-137">Mapitags.h</span></span>
  
> <span data-ttu-id="8a7b0-138">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a7b0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a7b0-139">See also</span></span>



[<span data-ttu-id="8a7b0-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8a7b0-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a7b0-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8a7b0-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a7b0-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8a7b0-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a7b0-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8a7b0-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


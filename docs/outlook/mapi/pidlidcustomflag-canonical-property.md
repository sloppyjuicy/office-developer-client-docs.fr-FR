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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cba4989ec3b1afcadb0caddd4af444cc9c96ebda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565955"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="64639-103">Propriété canonique PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="64639-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="64639-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64639-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64639-105">Masque de bits qui spécifie la façon dont un message personnalisé, par exemple, enregistré avec des propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="64639-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="64639-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="64639-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64639-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="64639-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="64639-108">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="64639-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64639-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="64639-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="64639-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="64639-110">Data type:</span></span>  <br/> |<span data-ttu-id="64639-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="64639-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64639-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="64639-112">Remarks</span></span>

<span data-ttu-id="64639-113">Pour récupérer la valeur de cette propriété, tout d’abord utiliser **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans **[IMAPIProp::GetProps](imapiprop-getprops.md)** pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="64639-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="64639-114">Indicateurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="64639-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="64639-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="64639-115">**Constant**</span></span>|<span data-ttu-id="64639-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="64639-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64639-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="64639-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="64639-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="64639-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="64639-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="64639-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="64639-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="64639-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="64639-121">Lors de l’appel **IMAPIProp::GetIDsFromNames**, spécifiez les valeurs suivantes pour la structure **[MAPINAMEID](mapinameid.md)** désignés par le paramètre d’entrée *lppPropNames* .</span><span class="sxs-lookup"><span data-stu-id="64639-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="64639-122">**Membre**</span><span class="sxs-lookup"><span data-stu-id="64639-122">**Member**</span></span>|<span data-ttu-id="64639-123">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="64639-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64639-124">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="64639-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="64639-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="64639-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="64639-126">ulKind :</span><span class="sxs-lookup"><span data-stu-id="64639-126">ulKind:</span></span>  <br/> |<span data-ttu-id="64639-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="64639-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="64639-128">Kind.lID :</span><span class="sxs-lookup"><span data-stu-id="64639-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="64639-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="64639-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="64639-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="64639-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64639-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="64639-131">Protocol specifications</span></span>

<span data-ttu-id="64639-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64639-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64639-133">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="64639-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64639-134">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="64639-134">Header files</span></span>

<span data-ttu-id="64639-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64639-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="64639-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="64639-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="64639-137">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="64639-137">Mapitags.h</span></span>
  
> <span data-ttu-id="64639-138">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="64639-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64639-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64639-139">See also</span></span>



[<span data-ttu-id="64639-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="64639-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64639-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="64639-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64639-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="64639-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64639-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="64639-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


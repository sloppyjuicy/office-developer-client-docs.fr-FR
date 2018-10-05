---
title: Propriété canonique PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400805"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="63dbc-103">Propriété canonique PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="63dbc-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="63dbc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63dbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63dbc-105">Permet d’afficher les informations de contact.</span><span class="sxs-lookup"><span data-stu-id="63dbc-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63dbc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="63dbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63dbc-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="63dbc-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="63dbc-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="63dbc-108">Property set:</span></span>  <br/> |<span data-ttu-id="63dbc-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="63dbc-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="63dbc-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="63dbc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63dbc-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="63dbc-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="63dbc-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="63dbc-112">Data type:</span></span>  <br/> |<span data-ttu-id="63dbc-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="63dbc-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="63dbc-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="63dbc-114">Area:</span></span>  <br/> |<span data-ttu-id="63dbc-115">Contact</span><span class="sxs-lookup"><span data-stu-id="63dbc-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63dbc-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="63dbc-116">Remarks</span></span>

<span data-ttu-id="63dbc-117">S’il est présent, la propriété doit avoir six entrées, chacun correspondant à un champ visible dans l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="63dbc-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="63dbc-118">**Index de base 1 dans la propriété à valeurs multiples**</span><span class="sxs-lookup"><span data-stu-id="63dbc-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="63dbc-119">**La valeur doit être une des options suivantes**</span><span class="sxs-lookup"><span data-stu-id="63dbc-119">**The value must be one of the following**</span></span>|<span data-ttu-id="63dbc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="63dbc-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63dbc-121">1</span><span class="sxs-lookup"><span data-stu-id="63dbc-121">1</span></span>  <br/> |<span data-ttu-id="63dbc-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63dbc-122">0x00000001</span></span>  <br/> |<span data-ttu-id="63dbc-123">L’application doit afficher l’adresse du contact personnel.</span><span class="sxs-lookup"><span data-stu-id="63dbc-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="63dbc-124">1</span><span class="sxs-lookup"><span data-stu-id="63dbc-124">1</span></span>  <br/> |<span data-ttu-id="63dbc-125">0 x 00000002 ou 0 x 00000000</span><span class="sxs-lookup"><span data-stu-id="63dbc-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="63dbc-126">L’application doit afficher le travail du contact.</span><span class="sxs-lookup"><span data-stu-id="63dbc-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="63dbc-127">1</span><span class="sxs-lookup"><span data-stu-id="63dbc-127">1</span></span>  <br/> |<span data-ttu-id="63dbc-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="63dbc-128">0x00000003</span></span>  <br/> |<span data-ttu-id="63dbc-129">L’application doit afficher le contact de l’autre adresse.</span><span class="sxs-lookup"><span data-stu-id="63dbc-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="63dbc-130">2</span><span class="sxs-lookup"><span data-stu-id="63dbc-130">2</span></span>  <br/> |<span data-ttu-id="63dbc-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="63dbc-131">0x00008080</span></span>  <br/> |<span data-ttu-id="63dbc-132">L’application doit afficher les messages électroniques 1.</span><span class="sxs-lookup"><span data-stu-id="63dbc-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="63dbc-133">2</span><span class="sxs-lookup"><span data-stu-id="63dbc-133">2</span></span>  <br/> |<span data-ttu-id="63dbc-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="63dbc-134">0x00008090</span></span>  <br/> |<span data-ttu-id="63dbc-135">L’application doit afficher 2.</span><span class="sxs-lookup"><span data-stu-id="63dbc-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="63dbc-136">2</span><span class="sxs-lookup"><span data-stu-id="63dbc-136">2</span></span>  <br/> |<span data-ttu-id="63dbc-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="63dbc-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="63dbc-138">L’application doit afficher messagerie3.</span><span class="sxs-lookup"><span data-stu-id="63dbc-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="63dbc-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="63dbc-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="63dbc-140">PropertyID de toutes les propriétés de téléphone ou l’un des numéros de télécopie sont spécifiés dans [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="63dbc-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="63dbc-141">L’application doit afficher la propriété correspondante.</span><span class="sxs-lookup"><span data-stu-id="63dbc-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="63dbc-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="63dbc-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63dbc-143">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="63dbc-143">Protocol specifications</span></span>

<span data-ttu-id="63dbc-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63dbc-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63dbc-145">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="63dbc-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63dbc-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63dbc-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63dbc-147">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="63dbc-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63dbc-148">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="63dbc-148">Header files</span></span>

<span data-ttu-id="63dbc-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63dbc-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="63dbc-150">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="63dbc-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63dbc-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63dbc-151">See also</span></span>



[<span data-ttu-id="63dbc-152">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="63dbc-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63dbc-153">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="63dbc-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63dbc-154">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="63dbc-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63dbc-155">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="63dbc-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


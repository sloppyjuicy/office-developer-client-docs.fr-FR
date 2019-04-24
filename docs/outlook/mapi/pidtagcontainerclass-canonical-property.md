---
title: Propriété canonique PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283148"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="abbf8-103">Propriété canonique PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="abbf8-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="abbf8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abbf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abbf8-105">Contient une chaîne de texte décrivant le type d'un dossier.</span><span class="sxs-lookup"><span data-stu-id="abbf8-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="abbf8-106">Bien que cette propriété soit généralement ignorée, les versions de Microsoft ® Exchange Server antérieures à Exchange Server 2003 gestionnaire de boîtes aux lettres s'attendent à ce que cette propriété soit présente.</span><span class="sxs-lookup"><span data-stu-id="abbf8-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abbf8-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="abbf8-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="abbf8-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="abbf8-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="abbf8-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="abbf8-109">Identifier:</span></span>  <br/> |<span data-ttu-id="abbf8-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="abbf8-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="abbf8-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="abbf8-111">Data type:</span></span>  <br/> |<span data-ttu-id="abbf8-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="abbf8-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="abbf8-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="abbf8-113">Area:</span></span>  <br/> |<span data-ttu-id="abbf8-114">Container</span><span class="sxs-lookup"><span data-stu-id="abbf8-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abbf8-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="abbf8-115">Remarks</span></span>

<span data-ttu-id="abbf8-116">Ces propriétés ne sont pas normalement utilisées par Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="abbf8-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="abbf8-117">Toutefois, Microsoft Office Outlook ® les joint à des dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="abbf8-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="abbf8-118">En outre, les versions d'Exchange Server antérieures à Exchange Server 2003 Mailbox Manager peuvent gérer de manière incorrecte les dossiers qui ne possèdent pas ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="abbf8-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="abbf8-119">Ces propriétés peuvent être assignées aux valeurs de chaîne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="abbf8-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="abbf8-120">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="abbf8-120">**Value**</span></span>|<span data-ttu-id="abbf8-121">**Contenu du dossier**</span><span class="sxs-lookup"><span data-stu-id="abbf8-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abbf8-122">Page. Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="abbf8-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="abbf8-123">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="abbf8-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="abbf8-124">Page. Prenez</span><span class="sxs-lookup"><span data-stu-id="abbf8-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="abbf8-125">Contacts</span><span class="sxs-lookup"><span data-stu-id="abbf8-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="abbf8-126">Page. N</span><span class="sxs-lookup"><span data-stu-id="abbf8-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="abbf8-127">Entrées du journal Outlook</span><span class="sxs-lookup"><span data-stu-id="abbf8-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="abbf8-128">Page. Note</span><span class="sxs-lookup"><span data-stu-id="abbf8-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="abbf8-129">Messages électroniques et notes</span><span class="sxs-lookup"><span data-stu-id="abbf8-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="abbf8-130">Page. StickyNote</span><span class="sxs-lookup"><span data-stu-id="abbf8-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="abbf8-131">Pense-bête Outlook</span><span class="sxs-lookup"><span data-stu-id="abbf8-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="abbf8-132">Page. Tâche</span><span class="sxs-lookup"><span data-stu-id="abbf8-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="abbf8-133">Tâches Outlook</span><span class="sxs-lookup"><span data-stu-id="abbf8-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="abbf8-134">Pour les dossiers qui contiennent des messages électroniques, ces propriétés doivent être définies sur IPF. Note.</span><span class="sxs-lookup"><span data-stu-id="abbf8-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abbf8-135">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="abbf8-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abbf8-136">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="abbf8-136">Protocol specifications</span></span>

<span data-ttu-id="abbf8-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abbf8-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abbf8-138">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="abbf8-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abbf8-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abbf8-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abbf8-140">Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="abbf8-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="abbf8-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abbf8-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abbf8-142">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="abbf8-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="abbf8-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abbf8-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abbf8-144">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de liste de distribution personnelle et de contact.</span><span class="sxs-lookup"><span data-stu-id="abbf8-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abbf8-145">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="abbf8-145">Header files</span></span>

<span data-ttu-id="abbf8-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="abbf8-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="abbf8-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="abbf8-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="abbf8-148">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="abbf8-148">Mapitags.h</span></span>
  
> <span data-ttu-id="abbf8-149">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="abbf8-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abbf8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abbf8-150">See also</span></span>



[<span data-ttu-id="abbf8-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="abbf8-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abbf8-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="abbf8-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abbf8-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="abbf8-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abbf8-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="abbf8-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


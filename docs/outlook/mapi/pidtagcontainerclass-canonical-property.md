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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283148"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="e0064-103">Propriété canonique PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="e0064-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="e0064-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0064-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0064-105">Contient une chaîne de texte décrivant le type d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="e0064-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="e0064-106">Bien que cette propriété soit généralement ignorée, les versions de Microsoft® Exchange Server antérieures à Exchange Server 2003 Mailbox Manager s’attendent à ce que cette propriété soit présente.</span><span class="sxs-lookup"><span data-stu-id="e0064-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0064-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e0064-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0064-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="e0064-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="e0064-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e0064-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e0064-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="e0064-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="e0064-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e0064-111">Data type:</span></span>  <br/> |<span data-ttu-id="e0064-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e0064-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e0064-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e0064-113">Area:</span></span>  <br/> |<span data-ttu-id="e0064-114">Container</span><span class="sxs-lookup"><span data-stu-id="e0064-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0064-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0064-115">Remarks</span></span>

<span data-ttu-id="e0064-116">Ces propriétés ne sont généralement pas utilisées par les Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e0064-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="e0064-117">Toutefois, Microsoft Office Outlook® les joint à des dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e0064-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="e0064-118">En outre, les versions de Exchange Server antérieures à Exchange Server 2003 Mailbox Manager peuvent gérer de manière incorrecte les dossiers qui n’ont pas ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e0064-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="e0064-119">Ces propriétés peuvent être affectées aux valeurs de chaîne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e0064-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="e0064-120">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e0064-120">**Value**</span></span>|<span data-ttu-id="e0064-121">**Contenu du dossier**</span><span class="sxs-lookup"><span data-stu-id="e0064-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0064-122">IPF. Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="e0064-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="e0064-123">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="e0064-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="e0064-124">IPF. Contact</span><span class="sxs-lookup"><span data-stu-id="e0064-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="e0064-125">Contacts</span><span class="sxs-lookup"><span data-stu-id="e0064-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="e0064-126">IPF. Journal</span><span class="sxs-lookup"><span data-stu-id="e0064-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="e0064-127">Outlook Entrées de journal</span><span class="sxs-lookup"><span data-stu-id="e0064-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="e0064-128">IPF. Remarque</span><span class="sxs-lookup"><span data-stu-id="e0064-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="e0064-129">Messages électroniques et notes</span><span class="sxs-lookup"><span data-stu-id="e0064-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="e0064-130">IPF. StickyNote</span><span class="sxs-lookup"><span data-stu-id="e0064-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="e0064-131">Outlook Pense-bêtes</span><span class="sxs-lookup"><span data-stu-id="e0064-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="e0064-132">IPF. Tâche</span><span class="sxs-lookup"><span data-stu-id="e0064-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="e0064-133">Tâches Outlook</span><span class="sxs-lookup"><span data-stu-id="e0064-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="e0064-134">Pour les dossiers qui contiennent des messages électroniques, ces propriétés doivent être définies sur IPF. Remarque.</span><span class="sxs-lookup"><span data-stu-id="e0064-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0064-135">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e0064-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0064-136">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e0064-136">Protocol specifications</span></span>

<span data-ttu-id="e0064-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0064-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0064-138">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="e0064-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0064-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0064-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0064-140">Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e0064-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="e0064-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0064-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0064-142">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="e0064-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e0064-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0064-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0064-144">Spécifie les propriétés et opérations autorisées pour les objets de liste de distribution personnelle et de contact.</span><span class="sxs-lookup"><span data-stu-id="e0064-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0064-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e0064-145">Header files</span></span>

<span data-ttu-id="e0064-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0064-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0064-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e0064-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0064-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0064-148">Mapitags.h</span></span>
  
> <span data-ttu-id="e0064-149">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="e0064-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0064-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0064-150">See also</span></span>



[<span data-ttu-id="e0064-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e0064-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0064-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e0064-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0064-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e0064-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0064-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e0064-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


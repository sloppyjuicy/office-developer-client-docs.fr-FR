---
title: Propriété canonique PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321321"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="aa801-103">Propriété canonique PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="aa801-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="aa801-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa801-105">Contient une liste de blocs de données qui représentent des réunions refusées.</span><span class="sxs-lookup"><span data-stu-id="aa801-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa801-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aa801-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa801-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="aa801-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="aa801-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aa801-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa801-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="aa801-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="aa801-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aa801-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa801-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aa801-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aa801-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="aa801-112">Area:</span></span>  <br/> |<span data-ttu-id="aa801-113">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="aa801-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa801-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aa801-114">Remarks</span></span>

<span data-ttu-id="aa801-115">Les blocs de données commencent par un en-tête de valeurs de bit 32 défini comme suit:</span><span class="sxs-lookup"><span data-stu-id="aa801-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="aa801-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="aa801-116">**Value**</span></span>|<span data-ttu-id="aa801-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="aa801-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa801-118">Identifier</span><span class="sxs-lookup"><span data-stu-id="aa801-118">Identifier</span></span>  <br/> |<span data-ttu-id="aa801-119">Ce champ doit être la valeur 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="aa801-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="aa801-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="aa801-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="aa801-121">Ce champ doit avoir la valeur 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="aa801-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="aa801-122">Version</span><span class="sxs-lookup"><span data-stu-id="aa801-122">Version</span></span>  <br/> |<span data-ttu-id="aa801-123">Ce champ doit avoir la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="aa801-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="aa801-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="aa801-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="aa801-125">Nombre d'enregistrements qui suivent.</span><span class="sxs-lookup"><span data-stu-id="aa801-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="aa801-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="aa801-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="aa801-127">Ce champ doit avoir la valeur 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="aa801-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="aa801-128">L'en-tête est suivi par des entrées de **RecordsCount** de 32 bits définies comme suit:</span><span class="sxs-lookup"><span data-stu-id="aa801-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="aa801-129">**Value**</span><span class="sxs-lookup"><span data-stu-id="aa801-129">**Value**</span></span>|<span data-ttu-id="aa801-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="aa801-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa801-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="aa801-131">StartTime</span></span>  <br/> |<span data-ttu-id="aa801-132">Heure de début de l'objet de réunion, en minutes, depuis minuit, le 1er janvier 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="aa801-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="aa801-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="aa801-133">EndTime</span></span>  <br/> |<span data-ttu-id="aa801-134">Heure de fin de l'objet de réunion, en minutes, depuis minuit, le 1er janvier 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="aa801-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="aa801-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="aa801-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="aa801-136">Taille, en octets, du champ GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="aa801-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="aa801-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="aa801-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="aa801-138">Valeur de la propriété **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la réunion représentée par cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="aa801-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="aa801-139">UserName</span><span class="sxs-lookup"><span data-stu-id="aa801-139">UserName</span></span>  <br/> |<span data-ttu-id="aa801-140">Les deux premiers octets correspondent à la longueur de la chaîne PT_STRING8 qui suit.</span><span class="sxs-lookup"><span data-stu-id="aa801-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="aa801-141">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="aa801-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa801-142">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="aa801-142">Protocol specifications</span></span>

<span data-ttu-id="aa801-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa801-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa801-144">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="aa801-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aa801-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa801-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa801-146">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="aa801-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa801-147">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="aa801-147">Header files</span></span>

<span data-ttu-id="aa801-148">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="aa801-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa801-149">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aa801-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa801-150">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="aa801-150">Mapitags.h</span></span>
  
> <span data-ttu-id="aa801-151">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="aa801-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa801-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa801-152">See also</span></span>



[<span data-ttu-id="aa801-153">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aa801-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa801-154">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aa801-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa801-155">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aa801-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa801-156">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="aa801-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


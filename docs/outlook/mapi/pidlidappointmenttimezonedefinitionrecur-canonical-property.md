---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345352"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="d066b-103">Propriété canonique PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="d066b-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="d066b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d066b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d066b-105">Contient un flux qui ma visite le format persistant d’une structure [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) qui stocke la description du fuseau horaire utilisé lors de la création d’un rendez-vous périodique ou d’une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="d066b-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d066b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d066b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d066b-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="d066b-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="d066b-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d066b-108">Property set:</span></span>  <br/> |<span data-ttu-id="d066b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d066b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d066b-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="d066b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d066b-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="d066b-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="d066b-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d066b-112">Data type:</span></span>  <br/> |<span data-ttu-id="d066b-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d066b-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d066b-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d066b-114">Area:</span></span>  <br/> |<span data-ttu-id="d066b-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="d066b-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d066b-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d066b-116">Remarks</span></span>

<span data-ttu-id="d066b-117">Les versions de Microsoft Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO (Collaboration Data Objects) 1.2.1 qui exécutent l’outil de mise à jour du calendrier Outlook ou Exchange Server utilisent les propriétés **dispidApptTZDefRecur** et **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) pour déterminer si la réunion périodique doit être ajustée si les règles du fuseau horaire changent.</span><span class="sxs-lookup"><span data-stu-id="d066b-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="d066b-118">Ces propriétés doivent être synchronisées, car les clients plus anciens peuvent toujours manipuler la **propriété dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="d066b-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="d066b-119">Pour détecter si les deux propriétés sont synchronisées, le membre **wFlags** de la règle qui correspond à **dispidTimeZoneStruct** doit avoir l’indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG définie.</span><span class="sxs-lookup"><span data-stu-id="d066b-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="d066b-120">Si cet indicateur n’est pas définie ou si elle est définie et que la règle dans la propriété **dispidTimeZoneStruct** ne correspond pas à la règle marquée, la propriété **dispidApptTZDefRecur** doit être ignorée et **dispidTimeZoneStruct** doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="d066b-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="d066b-121">Lorsque vous écrivez les propriétés **dispidApptTZDefRecur** et **dispidTimeZoneStruct** dans une nouvelle réunion périodique, ou lorsque vous faites un choix arbitraire d’utiliser la propriété **dispidTimeZoneStruct,** la définition actuelle du fuseau horaire (conformément au Registre Windows) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d066b-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="d066b-122">Un robot doit être prudent lorsqu’il lit un flux qui est obtenu à partir de **dispidApptTZDefRecur** ou lorsqu’il persiste **TZDEFINITION** dans un flux pour s’engager auprès d’une propriété binaire telle que **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="d066b-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="d066b-123">Pour plus d’informations, voir [À propos de la persistance de TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)dans un flux à valider dans une propriété binaire.</span><span class="sxs-lookup"><span data-stu-id="d066b-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="d066b-124">**dispidApptTZDefRecur** spécifie les informations de fuseau horaire qui décrivent comment convertir la date et l’heure de la réunion d’une série périodique vers et à partir du temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="d066b-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d066b-125">Si cette propriété est définie mais qu’elle possède des données incohérentes avec les données représentées par **dispidTimeZoneStruct**, le client doit utiliser **dispidTimeZoneStruct** au lieu de **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="d066b-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="d066b-126">Si **dispidApptTZDefRecur** n’est pas définie, la propriété **PidLidTimeZoneStruct** sera utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="d066b-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="d066b-127">Les champs de ce BLOB sont codés dans l’ordre des petits bouts.</span><span class="sxs-lookup"><span data-stu-id="d066b-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d066b-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d066b-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d066b-129">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d066b-129">Protocol specifications</span></span>

<span data-ttu-id="d066b-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d066b-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d066b-131">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="d066b-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d066b-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d066b-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d066b-133">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="d066b-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d066b-134">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d066b-134">Header files</span></span>

<span data-ttu-id="d066b-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d066b-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="d066b-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d066b-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d066b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d066b-137">See also</span></span>



[<span data-ttu-id="d066b-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d066b-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d066b-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d066b-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d066b-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d066b-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d066b-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d066b-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


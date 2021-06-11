---
title: Propriété canonique PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346374"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="7104c-103">Propriété canonique PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="7104c-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="7104c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7104c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7104c-105">Contient un flux qui masgue le format persistant d’une structure [TZREG,](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) qui décrit le fuseau horaire à utiliser pour l’heure de début et de fin d’un rendez-vous périodique ou d’une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="7104c-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7104c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7104c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7104c-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="7104c-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="7104c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="7104c-108">Property set:</span></span>  <br/> |<span data-ttu-id="7104c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7104c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7104c-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="7104c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7104c-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="7104c-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="7104c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7104c-112">Data type:</span></span>  <br/> |<span data-ttu-id="7104c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7104c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7104c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7104c-114">Area:</span></span>  <br/> |<span data-ttu-id="7104c-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="7104c-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7104c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7104c-116">Remarks</span></span>

<span data-ttu-id="7104c-117">Microsoft Office Outlook 2003, les versions antérieures de Outlook et les applications basées sur CDO (Collaboration Data Objects) 1.21 dont les utilisateurs n’ont pas exécuté l’outil de mise à jour du calendrier fourni par Outlook ou Exchange Server stockent l’heure de début et l’heure de fin d’un rendez-vous périodique ou d’une demande de réunion en tant qu’heure relative, et stockent le fuseau horaire où la demande de rendez-vous ou de réunion est créée dans **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="7104c-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="7104c-118">Toutefois, ce schéma ignore qu’au fil du temps, les règles de fuseau horaire peuvent changer, ce qui entraîne des rendez-vous et des réunions que les utilisateurs ont programmés avant que les règles ne changent et se produisent à des moments incorrects.</span><span class="sxs-lookup"><span data-stu-id="7104c-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="7104c-119">Les utilisateurs et les administrateurs qui n’exécutent pas Windows Vista ou qui n’ont pas de mise à jour automatique doivent utiliser les outils de rebasing de calendrier fournis par Outlook ou Exchange Server pour ajuster l’heure de ces rendez-vous et demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="7104c-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="7104c-120">Pour plus d’informations sur ces outils de rebasing de calendrier et les API qui rebasent les calendriers, voir à propos de [la rebasing](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx) de calendriers par programme pour l’heure d’été</span><span class="sxs-lookup"><span data-stu-id="7104c-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="7104c-121">Utilisez le format little-endian suivant lors de l’utilisation d’un flux obtenu à partir de **dispidTimeZoneStruct** ou lors de la persistance de la structure **TZREG** dans un flux à valider dans la propriété binaire **dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="7104c-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="7104c-122">Cette propriété est définie sur une série périodique pour spécifier des informations de fuseau horaire et indique comment convertir des champs horaires entre l’heure locale et le temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="7104c-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7104c-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7104c-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7104c-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7104c-124">Protocol specifications</span></span>

<span data-ttu-id="7104c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7104c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7104c-126">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="7104c-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7104c-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7104c-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7104c-128">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="7104c-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7104c-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7104c-129">Header files</span></span>

<span data-ttu-id="7104c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7104c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7104c-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7104c-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7104c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7104c-132">See also</span></span>



[<span data-ttu-id="7104c-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7104c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7104c-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7104c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7104c-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7104c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7104c-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7104c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


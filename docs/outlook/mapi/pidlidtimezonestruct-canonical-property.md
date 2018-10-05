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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401614"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="64749-103">Propriété canonique PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="64749-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="64749-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64749-105">Contient un flux qui mappe sur le format persistant d’une structure [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , qui décrit le fuseau horaire à utiliser pour l’heure de début et de fin d’une demande de réunion ou un rendez-vous périodique.</span><span class="sxs-lookup"><span data-stu-id="64749-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64749-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="64749-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64749-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="64749-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="64749-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="64749-108">Property set:</span></span>  <br/> |<span data-ttu-id="64749-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="64749-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="64749-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="64749-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64749-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="64749-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="64749-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="64749-112">Data type:</span></span>  <br/> |<span data-ttu-id="64749-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="64749-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="64749-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="64749-114">Area:</span></span>  <br/> |<span data-ttu-id="64749-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="64749-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64749-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="64749-116">Remarks</span></span>

<span data-ttu-id="64749-117">Microsoft Office Outlook 2003, les versions antérieures d’Outlook et les applications basées sur Collaboration Data Objects (CDO) 1.21 dont les utilisateurs n’ont pas exécuter l’outil de mise à jour de calendrier fournie par Outlook ou Exchange Server stockent l’heure de début et heure de fin d’un périodique rendez-vous ou une demande de réunion en tant qu’heure relative et de stocker le fuseau horaire dans lequel la demande de réunion ou de rendez-vous est créée dans **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="64749-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="64749-118">Toutefois, ce schéma ignore qu’au fil du temps, les règles de fuseau horaire peuvent changer, entraînant des rendez-vous et des réunions que les utilisateurs avant les règles modifiées et se produisent à des moments incorrectes.</span><span class="sxs-lookup"><span data-stu-id="64749-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="64749-119">Les utilisateurs et les administrateurs qui n’exécutent pas Windows Vista ou qui n’ont pas de mises à jour automatiques activées doivent utiliser le calendrier redéfinition des outils fournis par Outlook ou Exchange Server pour régler l’heure de ces rendez-vous et des demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="64749-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="64749-120">Pour plus d’informations sur ces outils de redéfinition de calendrier et les API qui redéfinir des calendriers, voir [à propos des calendriers de redéfinition par programme à l’heure](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64749-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="64749-121">Utilisez le format little-endian suivant lors de l’analyse d’un flux de données obtenu à partir de **dispidTimeZoneStruct**, ou lors de la persistance de la structure **TZREG** dans un flux pour valider à la propriété binaire **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="64749-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="64749-122">Cette propriété est définie sur une série périodique pour spécifier les informations de fuseau horaire et indique comment convertir les champs de temps entre l’heure locale et le temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="64749-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64749-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="64749-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64749-124">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="64749-124">Protocol specifications</span></span>

<span data-ttu-id="64749-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64749-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64749-126">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="64749-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64749-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64749-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64749-128">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="64749-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64749-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="64749-129">Header files</span></span>

<span data-ttu-id="64749-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64749-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="64749-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="64749-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64749-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64749-132">See also</span></span>



[<span data-ttu-id="64749-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="64749-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64749-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="64749-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64749-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="64749-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64749-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="64749-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


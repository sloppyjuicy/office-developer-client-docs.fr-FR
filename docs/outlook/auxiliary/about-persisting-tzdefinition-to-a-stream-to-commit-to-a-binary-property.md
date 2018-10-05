---
title: À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Les propriétés de fuseau horaire, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur et PidLidAppointmentTimeZoneDefinitionStartDisplay sont binaire nommé de propriétés, chacun d'entre eux contient un flux qui mappe sur le format persistant d’une structure TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398618"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="2e34b-103">À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire</span><span class="sxs-lookup"><span data-stu-id="2e34b-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="2e34b-104">Les propriétés de fuseau horaire, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)et [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sont binaire nommé de propriétés, chacun d'entre eux contient un flux qui mappe sur le format d’une structure [TZDEFINITION](tzdefinition.md) persistant.</span><span class="sxs-lookup"><span data-stu-id="2e34b-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="2e34b-105">Cette rubrique décrit un format endian peu qui peut être utilisé lors de la persistance **TZDEFINITION** dans un flux pour valider une des trois propriétés binaires.</span><span class="sxs-lookup"><span data-stu-id="2e34b-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="2e34b-106">Utilisez le même format de primauté dans un analyseur pour interpréter une valeur de flux de données obtenue à partir d’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2e34b-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

<span data-ttu-id="2e34b-107">Le numéro de version principal est utilisé pour modifier une minute.</span><span class="sxs-lookup"><span data-stu-id="2e34b-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="2e34b-108">Les clients qui ne sont pas familiarisés avec le numéro de version principal doivent traiter la propriété comme si elle n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="2e34b-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="2e34b-109">Écriture de la structure des clients doivent spécifier la constante **TZ_BIN_VERSION_MAJOR**.</span><span class="sxs-lookup"><span data-stu-id="2e34b-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="2e34b-110">Le numéro de version secondaire est utilisé pour l’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="2e34b-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="2e34b-111">Les clients qui ne sont pas familiarisés avec le numéro de version secondaire doivent lire les données qu’ils comprennent et ignorer les données qui peuvent être ajoutées à chaque règle ou dans le flux global.</span><span class="sxs-lookup"><span data-stu-id="2e34b-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="2e34b-112">Écriture de la structure des clients doivent spécifier la constante **TZ_BIN_VERSION_MINOR**.</span><span class="sxs-lookup"><span data-stu-id="2e34b-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="2e34b-113">Si un analyseur ne comprend pas la version principale de l’en-tête, il ne doit pas lire le reste de la structure et se comportent comme si les données sont manquantes.</span><span class="sxs-lookup"><span data-stu-id="2e34b-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="2e34b-114">Si un analyseur ne comprend pas la version secondaire de l’en-tête, elle doit utiliser **cbHeader** d’ignorer les parties qu’il ne comprend pas avance pour lire les parties du flux de données qu’il comprend.</span><span class="sxs-lookup"><span data-stu-id="2e34b-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="2e34b-115">La valeur de **wFlags** est toujours **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="2e34b-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="2e34b-116">Nom de la clé a une taille maximale de **MAX_PATH**.</span><span class="sxs-lookup"><span data-stu-id="2e34b-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="2e34b-117">Si un analyseur ne reconnaît pas la version principale d’une règle, le client doit ignorer la règle et permet de passer à la règle suivante **cbRule** .</span><span class="sxs-lookup"><span data-stu-id="2e34b-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="2e34b-118">Si un analyseur ne reconnaît pas la version secondaire d’une règle, le client doit analyser uniquement les composants de la règle qu’il comprend.</span><span class="sxs-lookup"><span data-stu-id="2e34b-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="2e34b-119">Lors de la persistance d’une structure **TZDEFINITION** à un flux, un analyseur doit essayer pas d’écrire les informations qu’il ne comprend pas.</span><span class="sxs-lookup"><span data-stu-id="2e34b-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="2e34b-120">Le nombre maximal de règles est 1 024.</span><span class="sxs-lookup"><span data-stu-id="2e34b-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="2e34b-121">Notez que la structure [TZREG](tzreg.md) est conservée ici différemment que lorsqu’elles sont persistantes seul, donc le même code ne peut être utilisé pour analyser.</span><span class="sxs-lookup"><span data-stu-id="2e34b-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e34b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e34b-122">See also</span></span>

- [<span data-ttu-id="2e34b-123">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="2e34b-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="2e34b-124">Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="2e34b-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="2e34b-125">Lire les propriétés de fuseau horaire à partir d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="2e34b-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)


---
title: À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Les propriétés de fuseau horaire, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur et PidLidAppointmentTimeZoneDefinitionStartDisplay sont des propriétés nommées binaires, chacune contenant un flux qui est mapmé sur le format persistant d’une structure TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316974"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="8b9ea-103">À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire</span><span class="sxs-lookup"><span data-stu-id="8b9ea-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="8b9ea-104">Les propriétés de fuseau horaire, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)et [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sont des propriétés nommées binaires, chacune contenant un flux qui est mapmé sur le format persistant d’une structure [TZDEFINITION.](tzdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="8b9ea-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="8b9ea-105">Cette rubrique décrit un petit format endian qui peut être utilisé lors de la persistance de **TZDEFINITION** dans un flux pour valider l’une des trois propriétés binaires.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="8b9ea-106">Utilisez le même format de fin dans un l’interpréteur pour interpréter une valeur de flux obtenue à partir de l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="8b9ea-107">Le numéro de version principal est utilisé pour apporter une modification importante.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="8b9ea-108">Les clients qui ne connaissent pas le numéro de version principal doivent traiter la propriété comme si elle n’y était pas.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="8b9ea-109">Les clients qui écrivent la structure doivent spécifier la **constante TZ_BIN_VERSION_MAJOR**.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="8b9ea-110">Le numéro de version mineure est utilisé pour l’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="8b9ea-111">Les clients qui ne connaissent pas le numéro de version mineure doivent lire les données qu’ils comprennent et ignorer les données qui peuvent être appendues à chaque règle ou au flux global.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="8b9ea-112">Les clients qui écrivent la structure doivent spécifier la **constante TZ_BIN_VERSION_MINOR**.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="8b9ea-113">Si un analyseur ne comprend pas la version principale de l’en-tête, il ne doit pas lire le reste de la structure et se comporter comme si les données étaient manquantes.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="8b9ea-114">Si un parseur ne comprend pas la version mineure de l’en-tête, il doit utiliser **cbHeader** pour ignorer les parties qu’il ne comprend pas et avancer pour lire les parties du flux qu’il comprend.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="8b9ea-115">La valeur de **wFlags est** **toujours TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="8b9ea-116">Le nom de la clé a une taille maximale **de MAX_PATH**.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="8b9ea-117">Si un parseur ne reconnaît pas la version principale d’une règle, le client doit ignorer la règle et utiliser **cbRule** pour passer à la règle suivante.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="8b9ea-118">Si un parseur ne reconnaît pas la version mineure d’une règle, le client doit uniquement l’identifier.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="8b9ea-119">Lors de la persistance d’une structure **TZDEFINITION** dans un flux, un testeur ne doit pas essayer d’écrire des informations qu’il ne comprend pas.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="8b9ea-120">Le nombre maximal de règles est 1 024.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="8b9ea-121">Notez que la structure [TZREG](tzreg.md) est persistante ici différemment de lorsqu’elle est persistante seule, de sorte que le même code ne peut pas être utilisé pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="8b9ea-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b9ea-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b9ea-122">See also</span></span>

- [<span data-ttu-id="8b9ea-123">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="8b9ea-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="8b9ea-124">Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="8b9ea-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="8b9ea-125">Lire les propriétés de fuseau horaire à partir d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="8b9ea-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)


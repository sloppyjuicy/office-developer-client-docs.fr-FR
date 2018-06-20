---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier, y compris toutes les règles de MAJ historiques, actuelles et futures fuseau horaire pour l’heure d’été.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782850"
---
# <a name="tzdefinition"></a><span data-ttu-id="c5dbb-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="c5dbb-103">TZDEFINITION</span></span>

<span data-ttu-id="c5dbb-104">Représente un fuseau horaire entier, y compris toutes les règles de MAJ historiques, actuelles et futures fuseau horaire pour l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c5dbb-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c5dbb-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="c5dbb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c5dbb-106">Members</span></span>

<span data-ttu-id="c5dbb-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="c5dbb-107">_wFlags_</span></span>
  
> <span data-ttu-id="c5dbb-108">Indique que le nom de la clé qui représente le fuseau horaire dans le Registre Windows est valid.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="c5dbb-109">Étant donné que chaque fuseau horaire doit toujours être identifiée par un nom de clé, ce membre doit avoir toujours la valeur **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="c5dbb-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="c5dbb-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="c5dbb-111">Le nom de la clé de ce fuseau horaire dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="c5dbb-112">Ce nom ne doit pas être localisé.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-112">This name must not be localized.</span></span> <span data-ttu-id="c5dbb-113">Il possède une taille maximale de **MAX_PATH**, qui est définie dans le windows.h de fichier d’en-tête Kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="c5dbb-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="c5dbb-114">_cRules_</span></span>
  
> <span data-ttu-id="c5dbb-115">Le nombre de règles de fuseau horaire pour cette définition.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="c5dbb-116">Le nombre maximal de règles est **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="c5dbb-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="c5dbb-117">_rgRules_</span></span>
  
> <span data-ttu-id="c5dbb-118">Tableau des règles qui décrivent le cas d’équipes.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5dbb-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5dbb-119">Remarks</span></span>

<span data-ttu-id="c5dbb-120">Il doit exister au moins une règle dans *rgRules* .</span><span class="sxs-lookup"><span data-stu-id="c5dbb-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="c5dbb-121">La première règle de *rgRules* est considéré comme la règle à utiliser jusqu'à ce que la deuxième règle commence, quel que soit le *stStart* sur la première règle.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="c5dbb-122">Les règles de tri de la plus ancienne à la plus récente.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="c5dbb-123">Ne se chevauchent pas autorisée entre les règles, pour une règle précédente est considéré comme fin au démarrage d’une nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="c5dbb-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5dbb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5dbb-124">See also</span></span>

- [<span data-ttu-id="c5dbb-125">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="c5dbb-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="c5dbb-126">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="c5dbb-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="c5dbb-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="c5dbb-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)


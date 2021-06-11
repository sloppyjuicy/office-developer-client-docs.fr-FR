---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Représente un fuseau horaire entier comprenant toutes les règles de décalage de fuseau horaire historique, actuelle et future pour l’heure d’été.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429340"
---
# <a name="tzdefinition"></a><span data-ttu-id="15135-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="15135-103">TZDEFINITION</span></span>

<span data-ttu-id="15135-104">Représente un fuseau horaire entier comprenant toutes les règles de décalage de fuseau horaire historique, actuelle et future pour l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="15135-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="15135-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="15135-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="15135-106">Membres</span><span class="sxs-lookup"><span data-stu-id="15135-106">Members</span></span>

<span data-ttu-id="15135-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="15135-107">_wFlags_</span></span>
  
> <span data-ttu-id="15135-108">Indique que le nom de clé qui représente le fuseau horaire dans le Windows registre est valide.</span><span class="sxs-lookup"><span data-stu-id="15135-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="15135-109">Étant donné que chaque fuseau horaire doit toujours être identifié par un nom de **clé,** ce membre doit toujours avoir la valeur TZDEFINITION_FLAG_VALID_KEYNAME .</span><span class="sxs-lookup"><span data-stu-id="15135-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="15135-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="15135-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="15135-111">Nom de la clé pour ce fuseau horaire dans le Windows registre.</span><span class="sxs-lookup"><span data-stu-id="15135-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="15135-112">Ce nom ne doit pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="15135-112">This name must not be localized.</span></span> <span data-ttu-id="15135-113">Il a une taille maximale de **MAX_PATH**, qui est définie dans le fichier d’en-tête du Kit de développement logiciel (SDK) Windows windows.h.</span><span class="sxs-lookup"><span data-stu-id="15135-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="15135-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="15135-114">_cRules_</span></span>
  
> <span data-ttu-id="15135-115">Nombre de règles de fuseau horaire pour cette définition.</span><span class="sxs-lookup"><span data-stu-id="15135-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="15135-116">Le nombre maximal de règles est **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="15135-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="15135-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="15135-117">_rgRules_</span></span>
  
> <span data-ttu-id="15135-118">Tableau de règles qui décrivent quand des changements se produisent.</span><span class="sxs-lookup"><span data-stu-id="15135-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15135-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="15135-119">Remarks</span></span>

<span data-ttu-id="15135-120">Il doit y avoir au moins une règle  *dans rgRules*  .</span><span class="sxs-lookup"><span data-stu-id="15135-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="15135-121">La première règle de  *rgRules*  est considérée comme la règle à utiliser jusqu’au démarrage de la deuxième règle, quel que soit le  *stStart*  de la première règle.</span><span class="sxs-lookup"><span data-stu-id="15135-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="15135-122">Les règles doivent être triées du plus ancien au plus récent.</span><span class="sxs-lookup"><span data-stu-id="15135-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="15135-123">Il n’y a pas de chevauchement autorisé entre les règles, de sorte qu’une règle antérieure est considérée comme se terminer au démarrage d’une nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="15135-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15135-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15135-124">See also</span></span>

- [<span data-ttu-id="15135-125">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="15135-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="15135-126">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="15135-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="15135-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="15135-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)


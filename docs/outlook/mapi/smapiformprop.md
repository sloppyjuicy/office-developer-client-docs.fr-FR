---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416698"
---
# <a name="smapiformprop"></a><span data-ttu-id="ea5ff-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="ea5ff-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="ea5ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea5ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea5ff-105">Décrit une propriété nommée utilisée avec un formulaire.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea5ff-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ea5ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea5ff-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="ea5ff-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a><span data-ttu-id="ea5ff-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ea5ff-108">Members</span></span>

 <span data-ttu-id="ea5ff-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-109">**ulFlags**</span></span>
  
> <span data-ttu-id="ea5ff-110">Indicateurs utilisés pour distinguer le format des chaînes dans la structure **SMAPIFormProp.**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="ea5ff-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="ea5ff-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="ea5ff-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ea5ff-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ea5ff-113">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="ea5ff-114">Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ea5ff-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-115">**nPropType**</span></span>
  
> <span data-ttu-id="ea5ff-116">Type de la propriété nommée, avec le mot le plus significatif à zéro.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="ea5ff-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-117">**nmid**</span></span>
  
> <span data-ttu-id="ea5ff-118">Nom de la propriété nommée, qui inclut une structure **GUID** identifiant le jeu de propriétés et une valeur numérique ou de chaîne qui représente un identificateur d’interface et un nom de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="ea5ff-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="ea5ff-120">Pointeur vers le nom complet de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="ea5ff-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="ea5ff-122">Valeur décrivant le type de données incluses dans le **membre u.**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="ea5ff-123">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea5ff-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="ea5ff-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="ea5ff-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="ea5ff-125">Le **membre u** ne contient pas d’éumération.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="ea5ff-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="ea5ff-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="ea5ff-127">Le **membre u** contient une structure qui décrit une éumération.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="ea5ff-128">**u**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-128">**u**</span></span>
  
> <span data-ttu-id="ea5ff-129">Union décrivant l’association entre le nom et le numéro de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="ea5ff-130">À l’aide de certaines propriétés, le **membre u** est vide.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="ea5ff-131">Avec d’autres propriétés, elle est représentée dans une structure composée des membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea5ff-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="ea5ff-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="ea5ff-133">Structure [MAPINAMEID](mapinameid.md) qui contient le jeu de propriétés et l’identificateur de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="ea5ff-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="ea5ff-135">Nombre de structures [SMAPIFormPropEnumVal](smapiformpropenumval.md) dans le tableau pointés par **le membre pfpevAvailable.**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="ea5ff-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="ea5ff-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="ea5ff-137">Pointeur vers un tableau de structures **SMAPIFormPropEnumVal,** chacune d’elles contient une valeur pour la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ea5ff-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea5ff-138">Remarks</span></span>

<span data-ttu-id="ea5ff-139">La structure **SMAPIFormProp** contient des informations sur une propriété de formulaire utilisée dans le cadre des définitions de l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType contient** une balise qui s’applique à l’union **u** qui fait partie de **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="ea5ff-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea5ff-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea5ff-140">See also</span></span>



[<span data-ttu-id="ea5ff-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="ea5ff-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="ea5ff-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="ea5ff-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="ea5ff-143">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="ea5ff-143">MAPI Structures</span></span>](mapi-structures.md)


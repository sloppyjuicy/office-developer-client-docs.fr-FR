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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 73475c5ee4e715796e06642756c05746b271d128
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787192"
---
# <a name="smapiformprop"></a><span data-ttu-id="d6b3d-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="d6b3d-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="d6b3d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6b3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6b3d-105">Décrit une propriété nommée est utilisée avec un formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6b3d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d6b3d-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6b3d-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="d6b3d-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d6b3d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d6b3d-108">Members</span></span>

 <span data-ttu-id="d6b3d-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-109">**ulFlags**</span></span>
  
> <span data-ttu-id="d6b3d-110">Indicateurs permet de distinguer le format des chaînes dans la structure **SMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="d6b3d-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="d6b3d-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="d6b3d-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="d6b3d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6b3d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d6b3d-113">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="d6b3d-114">Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d6b3d-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-115">**nPropType**</span></span>
  
> <span data-ttu-id="d6b3d-116">Type de la propriété nommée, avec le mot plus importante définir sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="d6b3d-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-117">**nmid**</span></span>
  
> <span data-ttu-id="d6b3d-118">Nom de la propriété nommée, qui inclut une structure **GUID** qui identifie la valeur de propriété set et un numérique ou chaîne qui représente un nom de formulaire et d’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="d6b3d-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="d6b3d-120">Pointeur vers le nom complet de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="d6b3d-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="d6b3d-122">Valeur décrivant le type de données inclus dans le membre **u** .</span><span class="sxs-lookup"><span data-stu-id="d6b3d-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="d6b3d-123">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6b3d-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="d6b3d-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="d6b3d-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="d6b3d-125">Le membre **u** ne contient pas une énumération.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="d6b3d-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="d6b3d-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="d6b3d-127">Le membre **u** contient une structure qui décrit une énumération.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="d6b3d-128">**u**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-128">**u**</span></span>
  
> <span data-ttu-id="d6b3d-129">Union décrivant l’association entre le nom et le numéro de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="d6b3d-130">À l’aide de certaines propriétés, le membre **u** est vide.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="d6b3d-131">Avec d’autres propriétés, il est représenté dans une structure composée des membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6b3d-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="d6b3d-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="d6b3d-133">La structure [MAPINAMEID](mapinameid.md) qui contient le jeu de propriétés et l’identificateur de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="d6b3d-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="d6b3d-135">Nombre de structures [SMAPIFormPropEnumVal](smapiformpropenumval.md) dans le tableau indiqué par le membre **pfpevAvailable** .</span><span class="sxs-lookup"><span data-stu-id="d6b3d-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="d6b3d-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="d6b3d-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="d6b3d-137">Pointeur vers un tableau de structures **SMAPIFormPropEnumVal** , chacun d'entre eux conserve une valeur pour la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6b3d-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6b3d-138">Remarks</span></span>

<span data-ttu-id="d6b3d-139">La structure **SMAPIFormProp** contient des informations sur une propriété de formulaire utilisée dans le cadre des définitions de l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contient une balise qui s’applique à l’union **u** qui fait partie de **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="d6b3d-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6b3d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6b3d-140">See also</span></span>



[<span data-ttu-id="d6b3d-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="d6b3d-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="d6b3d-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="d6b3d-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="d6b3d-143">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b3d-143">MAPI Structures</span></span>](mapi-structures.md)


---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357189"
---
# <a name="mapinameid"></a><span data-ttu-id="629b8-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="629b8-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="629b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="629b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="629b8-105">Décrit une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="629b8-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="629b8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="629b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="629b8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="629b8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a><span data-ttu-id="629b8-108">Members</span><span class="sxs-lookup"><span data-stu-id="629b8-108">Members</span></span>

 <span data-ttu-id="629b8-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="629b8-109">**lpguid**</span></span>
  
> <span data-ttu-id="629b8-110">Pointeur vers une structure de [GUID](guid.md) définissant un jeu de propriétés particulier; ce membre ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="629b8-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="629b8-111">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="629b8-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="629b8-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="629b8-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="629b8-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="629b8-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="629b8-114">Valeur définie par le client</span><span class="sxs-lookup"><span data-stu-id="629b8-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="629b8-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="629b8-115">**ulKind**</span></span>
  
> <span data-ttu-id="629b8-116">Valeur décrivant le type de valeur dans le membre **Kind** .</span><span class="sxs-lookup"><span data-stu-id="629b8-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="629b8-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="629b8-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="629b8-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="629b8-118">MNID_ID</span></span> 
  
> <span data-ttu-id="629b8-119">Le membre **Kind** contient une valeur entière qui représente le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="629b8-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="629b8-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="629b8-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="629b8-121">Le membre **Kind** contient une chaîne de caractères Unicode représentant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="629b8-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="629b8-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="629b8-122">**Kind**</span></span>
  
> <span data-ttu-id="629b8-123">Union décrivant le nom de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="629b8-123">Union describing the name of the named property.</span></span> <span data-ttu-id="629b8-124">Le nom peut être soit une valeur entière, stockée sur un **couvercle**, soit une chaîne de caractères Unicode, stockée dans **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="629b8-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="629b8-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="629b8-125">Remarks</span></span>

<span data-ttu-id="629b8-126">La structure **MAPINAMEID** est utilisée pour décrire les propriétés de propriétés nommées qui comportent des identificateurs sur 0x8000.</span><span class="sxs-lookup"><span data-stu-id="629b8-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="629b8-127">Un jeu de propriétés est une partie importante d'une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="629b8-127">A property set is an important part a named property.</span></span> <span data-ttu-id="629b8-128">Par exemple PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE sont des jeux de propriétés définis par MAPI.</span><span class="sxs-lookup"><span data-stu-id="629b8-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="629b8-129">Les propriétés nommées permettent aux clients de définir des propriétés personnalisées dans un espace de noms plus grand que ce qui est disponible dans la plage d'identificateurs de propriété définie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="629b8-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="629b8-130">Les noms de propriétés ne peuvent pas être utilisés pour obtenir directement des valeurs de propriété; elles doivent d'abord être mappées aux identificateurs de propriétés via la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="629b8-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="629b8-131">Pour des objets particuliers comme les messages, MAPI se réserve une plage d'identificateurs de propriétés pour les propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="629b8-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="629b8-132">Par conséquent, pour ces objets, les clients n'ont pas besoin d'utiliser les propriétés nommées et peuvent enregistrer la charge de travail associée.</span><span class="sxs-lookup"><span data-stu-id="629b8-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="629b8-133">Pour plus d'informations sur les propriétés nommées, voir [named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="629b8-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="629b8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="629b8-134">See also</span></span>



[<span data-ttu-id="629b8-135">GUID</span><span class="sxs-lookup"><span data-stu-id="629b8-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="629b8-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="629b8-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="629b8-137">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="629b8-137">MAPI Structures</span></span>](mapi-structures.md)


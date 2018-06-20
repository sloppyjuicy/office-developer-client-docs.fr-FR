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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784744"
---
# <a name="mapinameid"></a><span data-ttu-id="96e97-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="96e97-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="96e97-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96e97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96e97-105">Décrit une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="96e97-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96e97-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="96e97-106">Header file:</span></span>  <br/> |<span data-ttu-id="96e97-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96e97-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="96e97-108">Membres</span><span class="sxs-lookup"><span data-stu-id="96e97-108">Members</span></span>

 <span data-ttu-id="96e97-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="96e97-109">**lpguid**</span></span>
  
> <span data-ttu-id="96e97-110">Pointeur vers une structure [GUID](guid.md) de définition d’une propriété spécifique défini ; Ce membre ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="96e97-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="96e97-111">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="96e97-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="96e97-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="96e97-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="96e97-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="96e97-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="96e97-114">Une valeur définie par le client</span><span class="sxs-lookup"><span data-stu-id="96e97-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="96e97-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="96e97-115">**ulKind**</span></span>
  
> <span data-ttu-id="96e97-116">Valeur décrivant le type de valeur dans le membre de **type** .</span><span class="sxs-lookup"><span data-stu-id="96e97-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="96e97-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="96e97-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="96e97-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="96e97-118">MNID_ID</span></span> 
  
> <span data-ttu-id="96e97-119">Le **type** de membre contient une valeur entière qui représente le nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="96e97-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="96e97-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="96e97-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="96e97-121">Le **type** de membre contient une chaîne de caractères Unicode qui représente le nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="96e97-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="96e97-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="96e97-122">**Kind**</span></span>
  
> <span data-ttu-id="96e97-123">Union décrivant le nom de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="96e97-123">Union describing the name of the named property.</span></span> <span data-ttu-id="96e97-124">Le nom peut être une valeur entière, stockés dans le **capot**, soit une chaîne de caractères Unicode, stockés dans **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="96e97-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96e97-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="96e97-125">Remarks</span></span>

<span data-ttu-id="96e97-126">La structure **MAPINAMEID** est utilisée pour décrire les propriétés nommés qui ont des identificateurs sur 0 x 8000.</span><span class="sxs-lookup"><span data-stu-id="96e97-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="96e97-127">Un jeu de propriétés constitue une part importante une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="96e97-127">A property set is an important part a named property.</span></span> <span data-ttu-id="96e97-128">Par exemple PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE sont des jeux de propriétés définis par MAPI.</span><span class="sxs-lookup"><span data-stu-id="96e97-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="96e97-129">Propriétés nommées permettent aux clients permet de définir des propriétés personnalisées dans un espace de noms plus grand que ce qui est disponible dans la plage d’identificateurs MAPI défini par la propriété.</span><span class="sxs-lookup"><span data-stu-id="96e97-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="96e97-130">Les noms de propriété ne peut être utilisés pour obtenir des valeurs de propriété directement. ils doivent être tout d’abord mappées aux identificateurs de propriété par le biais de la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="96e97-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="96e97-131">Pour des objets spécifiques tels que les messages, MAPI réserve une plage d’identificateurs de propriété pour les propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="96e97-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="96e97-132">Par conséquent, pour ces objets, les clients et n’est pas à utiliser les propriétés nommées peuvent enregistrer les frais généraux.</span><span class="sxs-lookup"><span data-stu-id="96e97-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="96e97-133">Pour plus d’informations sur les propriétés nommées, voir [Propriétés nommées](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="96e97-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96e97-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96e97-134">See also</span></span>



[<span data-ttu-id="96e97-135">GUID</span><span class="sxs-lookup"><span data-stu-id="96e97-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="96e97-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="96e97-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="96e97-137">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="96e97-137">MAPI Structures</span></span>](mapi-structures.md)


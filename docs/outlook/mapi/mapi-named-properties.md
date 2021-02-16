---
title: MAPI des propri�t�s nomm�e
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435046"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="23f75-103">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="23f75-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="23f75-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23f75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23f75-105">MAPI fournit une fonction permettant d’affecter des noms à des propriétés, de ma mappage de ces noms à des identificateurs uniques et de rendre ce mappage persistant.</span><span class="sxs-lookup"><span data-stu-id="23f75-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="23f75-106">Le mappage de nom persistant à identificateur garantit que les noms de propriété restent valides entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="23f75-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="23f75-107">Pour définir une propriété nommée, un client ou un fournisseur de services constitue un nom et le stocke dans une structure [MAPINAMEID.](mapinameid.md)</span><span class="sxs-lookup"><span data-stu-id="23f75-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="23f75-108">Étant donné que les noms sont composés d’un identificateur global unique (GUID) 32 bits et d’une chaîne de caractères Unicode ou d’une valeur numérique, les créateurs de propriétés nommées peuvent créer des noms significatifs sans craindre de duplication.</span><span class="sxs-lookup"><span data-stu-id="23f75-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="23f75-109">Les noms sont uniques et peuvent être utilisés sans prendre en compte la valeur de leurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="23f75-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="23f75-110">Pour prendre en charge les propriétés nommées, un fournisseur de services implémente deux méthodes : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs,](imapiprop-getnamesfromids.md) pour traduire entre les noms et les identificateurs et pour autoriser ses méthodes [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) à récupérer et modifier des propriétés avec des identificateurs dans la plage de propriétés nommée.</span><span class="sxs-lookup"><span data-stu-id="23f75-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="23f75-111">La plage des identificateurs de propriété nommée est 0x8000 et 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="23f75-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="23f75-112">Tout objet qui implémente l’interface **IMAPIProp** peut prendre en charge les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="23f75-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="23f75-113">Les fournisseurs de carnet d’adresses qui permettent la copie d’entrées d’autres fournisseurs dans leurs conteneurs et fournisseurs de magasins de messages qui peuvent être utilisés pour créer des types de messages arbitraires sont requis pour fournir cette prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23f75-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="23f75-114">Il s’agit d’une option pour tous les autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="23f75-114">It is an option for all other service providers.</span></span> <span data-ttu-id="23f75-115">Les fournisseurs qui ne prisent pas en charge les propriétés nommées retournent des MAPI_E_NO_SUPPORT à partir des méthodes **GetIDsFromNames** et **GetNamesFromIDs** et refusent de définir des propriétés avec des identificateurs de 0x8000 ou supérieur, renvoyant les MAPI_E_UNEXPECTED dans **le SPropProblemarray**.</span><span class="sxs-lookup"><span data-stu-id="23f75-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="23f75-116">La création de noms pour les propriétés est un moyen pour les clients de définir de nouvelles propriétés pour des classes de message existantes ou personnalisées.</span><span class="sxs-lookup"><span data-stu-id="23f75-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="23f75-117">Les fournisseurs de services peuvent utiliser des propriétés nommées pour exposer des fonctionnalités uniques de leurs systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="23f75-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="23f75-118">Une autre utilisation des propriétés nommées consiste à fournir une autre façon de faire référence aux propriétés avec des identificateurs sous 0x8000.</span><span class="sxs-lookup"><span data-stu-id="23f75-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="23f75-119">Par exemple, un client peut utiliser du code semblable au code suivant pour récupérer les noms de toutes les propriétés nommées d’un objet :</span><span class="sxs-lookup"><span data-stu-id="23f75-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

<span data-ttu-id="23f75-120">Pour demander tous les noms du jeu PS_PUBLIC_STRINGS propriétés, un client remplace la valeur NULL dans le paramètre du jeu de propriétés PS_PUBLIC_STRINGS comme suit :</span><span class="sxs-lookup"><span data-stu-id="23f75-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a><span data-ttu-id="23f75-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f75-121">See also</span></span>

- [<span data-ttu-id="23f75-122">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="23f75-122">MAPI Property Overview</span></span>](mapi-property-overview.md)


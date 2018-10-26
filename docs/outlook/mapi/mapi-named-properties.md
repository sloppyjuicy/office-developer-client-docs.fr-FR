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
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579542"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="81bc4-103">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="81bc4-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="81bc4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81bc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81bc4-105">MAPI fournit un procédé pour l’affectation de noms aux propriétés, pour le mappage de ces noms à des identificateurs uniques et pour rendre ce mappage permanente.</span><span class="sxs-lookup"><span data-stu-id="81bc4-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="81bc4-106">Nom permanent au mappage de l’identificateur garantit que les noms de propriété valides entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="81bc4-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="81bc4-107">Pour définir une propriété nommée, un client ou fournisseur de services constitue un nom et la stocke dans une structure [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="81bc4-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="81bc4-108">Étant donné que les noms sont composés d’un identificateur global unique 32 bits, ou GUID et soit un caractère numérique ou chaîne valeur Unicode, créateurs de propriétés nommées peuvent créer des noms explicites sans risque de duplication.</span><span class="sxs-lookup"><span data-stu-id="81bc4-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="81bc4-109">Les noms sont uniques et ils peuvent être utilisés, indépendamment de la valeur de leurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="81bc4-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="81bc4-110">Pour prendre en charge des propriétés nommées, un fournisseur de services implémente deux méthodes : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — pour traduire des noms et identificateurs et pour permettre son [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) méthodes pour récupérer et modifier des propriétés avec des identificateurs de la plage de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="81bc4-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="81bc4-111">La plage pour les identificateurs de propriété nommée est comprise entre 0 x 8000 et 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="81bc4-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="81bc4-112">Tout objet qui implémente l’interface **IMAPIProp** peut prendre en charge des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="81bc4-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="81bc4-113">Fournisseurs de carnet d’adresses qui permettent de stockent les entrées à partir d’autres fournisseurs à copier dans leurs conteneurs et le message fournisseurs qui peuvent servir à créer des types de message arbitraires sont requises pour fournir cette prise en charge.</span><span class="sxs-lookup"><span data-stu-id="81bc4-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="81bc4-114">Il est possible pour tous les autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="81bc4-114">It is an option for all other service providers.</span></span> <span data-ttu-id="81bc4-115">Fournisseurs ne prenant pas en charge les propriétés nommées renvoyer MAPI_E_NO_SUPPORT des méthodes **GetIDsFromNames** et **GetNamesFromIDs** et refusent définir des propriétés avec des identificateurs de 0 x 8000 ou supérieur, renvoi MAPI_E_UNEXPECTED dans les \*\* SPropProblemarray\*\*.</span><span class="sxs-lookup"><span data-stu-id="81bc4-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="81bc4-116">Créez des noms de propriétés est un moyen pour les clients à définir de nouvelles propriétés pour les classes de message existant ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="81bc4-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="81bc4-117">Fournisseurs de service peuvent utiliser propriétés nommées pour exposer les fonctionnalités uniques de leurs systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="81bc4-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="81bc4-118">Encore une autre utilisation pour les propriétés nommées est de fournir une autre façon de faire référence à des propriétés avec des identificateurs ci-dessous 0 x 8000.</span><span class="sxs-lookup"><span data-stu-id="81bc4-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="81bc4-119">Par exemple, un client peut utiliser le code similaire au code suivant pour récupérer les noms de tous les propriétés nommées d’un objet :</span><span class="sxs-lookup"><span data-stu-id="81bc4-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="81bc4-120">Pour demander tous les noms de l’ensemble de la propriété PS_PUBLIC_STRINGS, un client remplace la valeur NULL dans le paramètre set propriété PS_PUBLIC_STRINGS comme suit :</span><span class="sxs-lookup"><span data-stu-id="81bc4-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="81bc4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81bc4-121">See also</span></span>

- [<span data-ttu-id="81bc4-122">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="81bc4-122">MAPI Property Overview</span></span>](mapi-property-overview.md)


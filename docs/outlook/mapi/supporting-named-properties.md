---
title: Prise en charge des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9ee41469914e52295af219428f26854662c9e2f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582245"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="03f77-103">Prise en charge des propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="03f77-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="03f77-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03f77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03f77-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="03f77-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="03f77-106">Prise en charge des propriétés nommées est requis pour :</span><span class="sxs-lookup"><span data-stu-id="03f77-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="03f77-107">Fournisseurs de carnet d’adresses qui autorisent les entrées à partir d’autres fournisseurs doivent être copiés dans leurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="03f77-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="03f77-108">Fournisseurs qui peuvent servir à créer des types de message arbitraire de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="03f77-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="03f77-109">Prise en charge de la propriété nommée est facultatif pour tous les autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="03f77-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="03f77-110">Fournisseurs de services qui prennent en charge des propriétés nommées doivent implémenter les méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) mappage à-identificateur de nom.</span><span class="sxs-lookup"><span data-stu-id="03f77-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="03f77-111">Clients appeler **GetNamesFromIDs** pour récupérer les noms correspondants pour un ou plusieurs identificateurs de propriété dans la plage 0 x 8000 plus et **GetIDsFromNames** pour créer ou extraire les identificateurs pour un ou plusieurs noms.</span><span class="sxs-lookup"><span data-stu-id="03f77-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="03f77-112">Fournisseurs de services ne prenant pas en charge les propriétés nommées doivent :</span><span class="sxs-lookup"><span data-stu-id="03f77-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="03f77-113">Échec des appels [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir des propriétés avec des identificateurs supérieure ou égale à 0 x 8000 à retourner MAPI_E_UNEXPECTED_ID dans le tableau de [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="03f77-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="03f77-114">Retourner MAPI_E_NO_SUPPORT des méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="03f77-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    


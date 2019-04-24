---
title: Propriétés nommées de prise en charge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349629"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="d3ca5-103">Propriétés nommées de prise en charge</span><span class="sxs-lookup"><span data-stu-id="d3ca5-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="d3ca5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3ca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3ca5-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="d3ca5-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="d3ca5-106">La prise en charge des propriétés nommées est requise pour:</span><span class="sxs-lookup"><span data-stu-id="d3ca5-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="d3ca5-107">Fournisseurs de carnet d'adresses qui permettent de copier des entrées d'autres fournisseurs dans leurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="d3ca5-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="d3ca5-108">Fournisseurs de banques de messages pouvant être utilisés pour créer des types de message arbitraires.</span><span class="sxs-lookup"><span data-stu-id="d3ca5-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="d3ca5-109">La prise en charge des propriétés nommées est facultative pour tous les autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="d3ca5-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="d3ca5-110">Les fournisseurs de services qui prennent en charge les propriétés nommées doivent implémenter le mappage de nom à identificateur dans les méthodes [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ca5-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="d3ca5-111">Les clients appellent **GetNamesFromIDs** pour récupérer les noms correspondants pour un ou plusieurs identificateurs de propriété dans la plage sur 0X8000 et **GetIDsFromNames** pour créer ou récupérer les identificateurs d'un ou de plusieurs noms.</span><span class="sxs-lookup"><span data-stu-id="d3ca5-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="d3ca5-112">Les fournisseurs de services qui ne prennent pas en charge les propriétés nommées doivent:</span><span class="sxs-lookup"><span data-stu-id="d3ca5-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="d3ca5-113">Échec des appels à [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir les propriétés avec des identificateurs de 0x8000 ou supérieur en renvoyant MAPI_E_UNEXPECTED_ID dans le tableau [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ca5-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="d3ca5-114">Renvoyer MAPI_E_NO_SUPPORT à partir des méthodes [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ca5-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    


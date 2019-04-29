---
title: Objets du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430356"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="be2ad-103">Objets du fournisseur de transport MAPI</span><span class="sxs-lookup"><span data-stu-id="be2ad-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="be2ad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be2ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be2ad-105">En plus du fournisseur standard et des objets d'ouverture de session implémentés par tous les fournisseurs de services, les fournisseurs de transport sont requis pour implémenter un objet d'État.</span><span class="sxs-lookup"><span data-stu-id="be2ad-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="be2ad-106">Pour les autres types de fournisseurs de services, l'implémentation d'un objet Status est facultative.</span><span class="sxs-lookup"><span data-stu-id="be2ad-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="be2ad-107">Toutefois, MAPI l'exige pour les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="be2ad-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="be2ad-108">Les fournisseurs de transport qui prennent en charge le téléchargement des en-têtes de message à partir d'un serveur distant implémentent également un dossier et un tableau.</span><span class="sxs-lookup"><span data-stu-id="be2ad-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="be2ad-109">L'illustration suivante montre chacun des objets que les fournisseurs de transport peuvent implémenter avec leurs interfaces correspondantes.</span><span class="sxs-lookup"><span data-stu-id="be2ad-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="be2ad-110">L'illustration indique également si MAPI ou un client est l'utilisateur de l'objet.</span><span class="sxs-lookup"><span data-stu-id="be2ad-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="be2ad-111">![Objets implémentés par les fournisseurs de transport] (media/amapi_66.gif "Objets implémentés par les fournisseurs de transport")</span><span class="sxs-lookup"><span data-stu-id="be2ad-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be2ad-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be2ad-112">See also</span></span>

- [<span data-ttu-id="be2ad-113">Objets du fournisseur de services MAPI</span><span class="sxs-lookup"><span data-stu-id="be2ad-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)


---
title: Objets du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784722"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="d4e8d-103">Objets du fournisseur de transport MAPI</span><span class="sxs-lookup"><span data-stu-id="d4e8d-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="d4e8d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4e8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4e8d-105">Outre le fournisseur standard et objets d’ouverture de session implémentées par tous les fournisseurs de services, les fournisseurs de transport sont requis pour implémenter un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="d4e8d-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="d4e8d-106">Pour les autres types de fournisseur de service, l’implémentation d’un objet d’état est facultative.</span><span class="sxs-lookup"><span data-stu-id="d4e8d-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="d4e8d-107">Toutefois, MAPI exige des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="d4e8d-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="d4e8d-108">Fournisseurs de transport qui prennent en charge le téléchargement des en-têtes des messages à partir d’un serveur distant également implémentent un dossier et une table.</span><span class="sxs-lookup"><span data-stu-id="d4e8d-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="d4e8d-109">L’illustration suivante montre chacun des objets qui implémentent des fournisseurs de transport peuvent avec leurs interfaces correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d4e8d-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="d4e8d-110">L’illustration indique également si MAPI ou un client est utilisateur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d4e8d-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="d4e8d-111">![Objets qui implémentent des fournisseurs de transport] (media/amapi_66.gif "Objets qui implémentent des fournisseurs de transport")</span><span class="sxs-lookup"><span data-stu-id="d4e8d-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4e8d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4e8d-112">See also</span></span>

- [<span data-ttu-id="d4e8d-113">Objets du fournisseur de services MAPI</span><span class="sxs-lookup"><span data-stu-id="d4e8d-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)


---
title: Objets et architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279786"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="603ae-103">Objets et architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="603ae-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="603ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="603ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="603ae-105">Tous les objets que MAPI définit se transforment en une ou plusieurs couches dans l’architecture MAPI.</span><span class="sxs-lookup"><span data-stu-id="603ae-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="603ae-106">La couche d’interface client contient tous les objets qu’une application cliente, une visionneuse de formulaires ou un serveur de formulaires peut implémenter.</span><span class="sxs-lookup"><span data-stu-id="603ae-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="603ae-107">La couche d’interface du fournisseur de services contient les objets qu’un fournisseur de services de tout type peut implémenter.</span><span class="sxs-lookup"><span data-stu-id="603ae-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="603ae-108">Cette couche comprend des objets implémentés par des carnets d’adresses, des magasins de messages, des fournisseurs de transport et des bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="603ae-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="603ae-109">La couche qui représente le sous-système MAPI est positionnée entre les couches d’interface du client et du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="603ae-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="603ae-110">La couche MAPI contient tous les objets que MAPI implémente pour les clients ou fournisseurs de services à utiliser.</span><span class="sxs-lookup"><span data-stu-id="603ae-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="603ae-111">L’illustration suivante montre où chacun des objets MAPI s’inscrit dans l’architecture MAPI.</span><span class="sxs-lookup"><span data-stu-id="603ae-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="603ae-112">Les objets sont représentés avec les noms de leurs interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="603ae-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="603ae-113">Par exemple, un objet de sink de conseil s’affiche comme [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), l’interface qui dérive de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et que chaque objet de sink de conseil implémente.</span><span class="sxs-lookup"><span data-stu-id="603ae-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="603ae-114">Interfaces utilisées ou implémentées par plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="603ae-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="603ae-115">Bien que la couche MAPI semble séparer les couches client et fournisseur, ce qui signifie que toutes les communications doivent passer par MAPI, ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="603ae-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="603ae-116">Les clients peuvent et communiquent directement avec les objets du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="603ae-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="603ae-117">**Couches d’objets dans MAPI**</span><span class="sxs-lookup"><span data-stu-id="603ae-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="603ae-118">![Couches d’objet dans les couches](media/amapi_38.gif "de l’objet MAPI dans MAPI")</span><span class="sxs-lookup"><span data-stu-id="603ae-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="603ae-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603ae-119">See also</span></span>

- [<span data-ttu-id="603ae-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="603ae-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="603ae-121">Vue d’ensemble de l’interface et de l’objet MAPI</span><span class="sxs-lookup"><span data-stu-id="603ae-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)


---
title: Objets et l’architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391037"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="84dbc-103">Objets et l’architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="84dbc-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="84dbc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84dbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84dbc-105">Tous les objets qui définit MAPI peuvent être classées dans une ou plusieurs couches de l’architecture MAPI.</span><span class="sxs-lookup"><span data-stu-id="84dbc-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="84dbc-106">La couche d’interface client contient tous les objets qu’une application cliente, une visionneuse de formulaire ou un serveur de formulaire peut implémenter.</span><span class="sxs-lookup"><span data-stu-id="84dbc-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="84dbc-107">La couche d’interface de service fournisseur contient les objets qui permettre mettre en œuvre un fournisseur de services d’un type quelconque.</span><span class="sxs-lookup"><span data-stu-id="84dbc-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="84dbc-108">Cette couche inclut des objets implémentés par les carnets d’adresses, les banques de messages, les fournisseurs de transport et bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="84dbc-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="84dbc-109">La couche qui représente le sous-système MAPI est placée entre les couches de l’interface fournisseur client et le service.</span><span class="sxs-lookup"><span data-stu-id="84dbc-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="84dbc-110">La couche MAPI contient tous les objets implémentés par MAPI pour les clients ou fournisseurs de services à utiliser.</span><span class="sxs-lookup"><span data-stu-id="84dbc-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="84dbc-111">L’illustration suivante montre où chacun des objets MAPI correspond à l’architecture MAPI.</span><span class="sxs-lookup"><span data-stu-id="84dbc-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="84dbc-112">Les objets sont représentées par les noms de leurs interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="84dbc-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="84dbc-113">Par exemple, un objet de récepteur advise est signalée comme étant [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), l’interface qui dérive de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et qui implémente tous les objets récepteur advise.</span><span class="sxs-lookup"><span data-stu-id="84dbc-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="84dbc-114">Les interfaces reliant les calques sont utilisés ou implémentées par plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="84dbc-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="84dbc-115">Bien que la couche MAPI s’affiche pour séparer les couches client et le fournisseur, ce qui implique que toutes les communications doivent passer par l’interface MAPI, ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="84dbc-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="84dbc-116">Les clients peuvent et communiquent directement aux objets de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="84dbc-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="84dbc-117">**Couches d’objets dans MAPI**</span><span class="sxs-lookup"><span data-stu-id="84dbc-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="84dbc-118">![Couches d’objets dans MAPI] (media/amapi_38.gif "Couches d’objets dans MAPI")</span><span class="sxs-lookup"><span data-stu-id="84dbc-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84dbc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84dbc-119">See also</span></span>

- [<span data-ttu-id="84dbc-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84dbc-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="84dbc-121">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="84dbc-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)


---
title: Architecture de l’assembly PIA Outlook
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336525"
---
# <a name="architecture-of-the-outlook-pia"></a><span data-ttu-id="fd6ec-102">Architecture de l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6ec-102">Architecture of the Outlook PIA</span></span>

<span data-ttu-id="fd6ec-103">L’assembly PIA (Primary Interop Assembly) Outlook prend entièrement en charge le développement avec le modèle objet Outlook dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-103">The Outlook Primary Interop Assembly (PIA) fully supports developing against the Outlook object model in managed code.</span></span> <span data-ttu-id="fd6ec-104">Toutefois, la première fois que vous observez l'assembly PIA dans un navigateur d'objets, vous risquez d'être surpris par les nombreuses interfaces supplémentaires que contient l'assembly PIA et par le fait que tous les membres (méthodes, propriétés et événements) d'un objet ne soient pas exposés par la même interface d'objet.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-104">However, when you look at the PIA in an object browser for the first time, you may be surprised by the many extra interfaces that the PIA contains, and the fact that not all method, property, and event members of an object are exposed by the same object interface.</span></span> <span data-ttu-id="fd6ec-105">Les rubriques de cette section indiquent comment accéder aux membres d'un objet dans le code et où rechercher de l'aide sur les objets, les méthodes, les propriétés et les événements.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-105">The topics in this section describe guidelines for how to access object members in code, and where to look for help for objects, methods, properties, and events.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fd6ec-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fd6ec-106">In this section</span></span>

|<span data-ttu-id="fd6ec-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="fd6ec-107">Topic</span></span>|<span data-ttu-id="fd6ec-108">Description</span><span class="sxs-lookup"><span data-stu-id="fd6ec-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="fd6ec-109">Mise en rapport de l’assembly PIA Outlook avec le modèle objet</span><span class="sxs-lookup"><span data-stu-id="fd6ec-109">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md) |<span data-ttu-id="fd6ec-110">Décrit comment les objets et les membres du modèle objet Outlook basé sur COM sont mappés aux interfaces et classes managées correspondant dans l’assembly PIA.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-110">Describes how objects and members in the COM-based Outlook object model are mapped to corresponding managed interfaces and classes in the PIA.</span></span>|
|[<span data-ttu-id="fd6ec-111">Objets dans l'assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6ec-111">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md) |<span data-ttu-id="fd6ec-112">Décrit les interfaces, classes et délégués .NET typiques qui sont mappés à un objet COM et décrit comment accéder à un objet dans l'assembly PIA.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-112">Describes the typical .NET interfaces, classes, and delegates that are mapped to a COM object, and describes how to access an object in the PIA.</span></span>|
|[<span data-ttu-id="fd6ec-113">Méthodes et propriétés dans l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6ec-113">Methods and properties in the Outlook PIA</span></span>](methods-and-properties-in-the-outlook-pia.md) |<span data-ttu-id="fd6ec-114">Décrit comment accéder aux méthodes et propriétés d’un objet dans le code managé à l’aide de l’assembly PIA.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-114">Describes how to access methods and properties of an object in managed code by using the PIA.</span></span>|
|[<span data-ttu-id="fd6ec-115">Événements dans l'assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6ec-115">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md) |<span data-ttu-id="fd6ec-116">Décrit les interfaces, les délégués et les classes d’assistance de récepteur liés à un événement dans l’assembly PIA.</span><span class="sxs-lookup"><span data-stu-id="fd6ec-116">Describes event-related interfaces, delegates, and sink helper classes in the PIA.</span></span>|

## <a name="see-also"></a><span data-ttu-id="fd6ec-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd6ec-117">See also</span></span>

- [<span data-ttu-id="fd6ec-118">Configuration pour utiliser l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6ec-118">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="fd6ec-119">Développement de compléments managés Outlook à l’aide de l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6ec-119">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="fd6ec-120">Procédure (Référence PIA Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="fd6ec-120">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)


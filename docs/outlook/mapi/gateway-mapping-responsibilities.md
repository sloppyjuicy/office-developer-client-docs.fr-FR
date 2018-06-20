---
title: Responsabilités de mappage de passerelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ad5f4e896b748dc0d7495c428af093af57bc7cdd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783391"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="6b383-103">Responsabilités de mappage de passerelle</span><span class="sxs-lookup"><span data-stu-id="6b383-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="6b383-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b383-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b383-105">Lorsqu’une passerelle prenant en charge MAPI reçoit un message contenant des propriétés nommées dans un des jeux de propriété spéciale destinée à contenir les propriétés de passerelle-mappables, la passerelle doit être mappé toutes les propriétés du protocole de la destination système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6b383-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="6b383-106">Bien que MAPI recommande que passerelles gérer nommées toutes les propriétés dans les jeux de propriétés spéciales, passerelles doivent gérer deux seulement : adresse et le type d’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6b383-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="6b383-107">Étant donné que l’adresse de messagerie et les propriétés de type adresse affectent directement la transmission de message, il est fondamental que passerelles prennent en charge le mappage de ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="6b383-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="6b383-108">Étant donné que les clés de recherche se composent de type d’adresse et l’adresse d’un utilisateur, ils doivent également être traduits si possible.</span><span class="sxs-lookup"><span data-stu-id="6b383-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="6b383-109">Identificateurs d’entrée ne sont pas censés être traités fréquemment.</span><span class="sxs-lookup"><span data-stu-id="6b383-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="6b383-110">Pour activer le mappage d’un identificateur d’entrée qui provient d’un système de messagerie à un identificateur d’entrée est utilisable par un autre système de messagerie, la passerelle doit être en mesure d’utiliser le format des deux systèmes.</span><span class="sxs-lookup"><span data-stu-id="6b383-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="6b383-111">Étant donné que la plupart des passerelles ne sont pas conscients de formats identificateur d’entrée, la traduction d’identificateurs d’entrée est rare.</span><span class="sxs-lookup"><span data-stu-id="6b383-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="6b383-112">Une autre propriété mappable qui n’est pas censée être traduits fréquemment est le nom complet.</span><span class="sxs-lookup"><span data-stu-id="6b383-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="6b383-113">Passerelles doivent stocker les noms d’affichage et les transmet, mais pas nécessairement les traduire.</span><span class="sxs-lookup"><span data-stu-id="6b383-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  


---
title: Responsabilités de la passerelle en cas de mappage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422753"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="31506-103">Responsabilités de la passerelle en cas de mappage</span><span class="sxs-lookup"><span data-stu-id="31506-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="31506-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31506-105">Lorsqu’une passerelle MAPI reçoit un message contenant des propriétés nommées dans l’un des jeux de propriétés spéciaux désignés pour contenir les propriétés mappables de la passerelle, la passerelle doit maguer toutes les propriétés au protocole du système de messagerie de destination.</span><span class="sxs-lookup"><span data-stu-id="31506-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="31506-106">Bien que MAPI recommande que les passerelles gèrent toutes les propriétés nommées dans les jeux de propriétés spéciaux, les passerelles ne doivent en gérer que deux : l’adresse de messagerie et le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="31506-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="31506-107">Étant donné que les propriétés d’adresse de messagerie et de type d’adresse affectent directement la transmission des messages, il est essentiel que les passerelles prendre en charge le mappage de ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="31506-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="31506-108">Étant donné que les clés de recherche sont constituées du type d’adresse et de l’adresse d’un utilisateur, elles doivent également être traduites si possible.</span><span class="sxs-lookup"><span data-stu-id="31506-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="31506-109">Les identificateurs d’entrée ne sont pas censés être gérés fréquemment.</span><span class="sxs-lookup"><span data-stu-id="31506-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="31506-110">Pour activer le mappage d’un identificateur d’entrée provenant d’un système de messagerie vers un identificateur d’entrée utilisable par un autre système de messagerie, la passerelle doit être en mesure d’utiliser le format des deux systèmes.</span><span class="sxs-lookup"><span data-stu-id="31506-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="31506-111">Étant donné que la plupart des passerelles ne connaissent pas les formats d’identificateur d’entrée, la traduction des identificateurs d’entrée est rare.</span><span class="sxs-lookup"><span data-stu-id="31506-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="31506-112">Une autre propriété mappable qui n’est pas prévue pour être traduite fréquemment est le nom complet.</span><span class="sxs-lookup"><span data-stu-id="31506-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="31506-113">Les passerelles doivent stocker les noms d’affichage et les transmettre, mais pas nécessairement les traduire.</span><span class="sxs-lookup"><span data-stu-id="31506-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  


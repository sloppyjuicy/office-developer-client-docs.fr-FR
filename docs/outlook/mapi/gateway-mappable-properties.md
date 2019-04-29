---
title: Propriétés mappables de la passerelle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430475"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="394b4-103">Propriétés mappables de la passerelle</span><span class="sxs-lookup"><span data-stu-id="394b4-103">Gateway mappable properties</span></span>

<span data-ttu-id="394b4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="394b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="394b4-105">Les propriétés pouvant être mappées par une passerelle sont des propriétés qui peuvent nécessiter une traduction lorsqu'elles sont envoyées d'un domaine de messagerie à un autre.</span><span class="sxs-lookup"><span data-stu-id="394b4-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="394b4-106">Les propriétés pouvant être mappées par la passerelle MAPI permettent aux messages d'inclure des informations qui nécessitent une passerelle pour s'assurer que le système de messagerie de destination l'utilise correctement.</span><span class="sxs-lookup"><span data-stu-id="394b4-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="394b4-107">Bien que les développeurs de passerelles ne soient pas tenus de fournir cette fonctionnalité de traduction, ils doivent envisager des propriétés mappées sur les passerelles pour améliorer la gestion du contenu des messages.</span><span class="sxs-lookup"><span data-stu-id="394b4-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="394b4-108">MAPI spécifie cinq types de propriétés mappées sur la passerelle:</span><span class="sxs-lookup"><span data-stu-id="394b4-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="394b4-109">Nom unique (DN)</span><span class="sxs-lookup"><span data-stu-id="394b4-109">Display name</span></span>
    
- <span data-ttu-id="394b4-110">Nom complet</span><span class="sxs-lookup"><span data-stu-id="394b4-110">Email address</span></span>
    
- <span data-ttu-id="394b4-111">Type de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="394b4-111">Email type</span></span>
    
- <span data-ttu-id="394b4-112">Identificateur d'entrée</span><span class="sxs-lookup"><span data-stu-id="394b4-112">Entry identifier</span></span>
    
- <span data-ttu-id="394b4-113">Clé de recherche</span><span class="sxs-lookup"><span data-stu-id="394b4-113">Search key</span></span>
    
<span data-ttu-id="394b4-114">Il s'agit de l'ensemble des propriétés d'adressage associées aux destinataires, aux expéditeurs, aux destinataires des rapports, ainsi qu'aux expéditeurs et destinataires délégués.</span><span class="sxs-lookup"><span data-stu-id="394b4-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="394b4-115">Pour aider votre client à définir ces propriétés de sorte qu'une passerelle les gère spécialement, MAPI spécifie une convention d'affectation de noms à l'aide de propriétés nommées et de jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="394b4-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="394b4-116">Cinq jeux de propriétés existent pour contenir les propriétés nommées, les propriétés d'adressage qui nécessitent un mappage.</span><span class="sxs-lookup"><span data-stu-id="394b4-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="394b4-117">Il existe un jeu de propriétés pour chaque type de propriété mappable.</span><span class="sxs-lookup"><span data-stu-id="394b4-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="394b4-118">Les jeux de propriétés qui contiendront ces propriétés d'adressage nommées sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="394b4-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="394b4-119">**Jeu de propriétés**</span><span class="sxs-lookup"><span data-stu-id="394b4-119">**Property set**</span></span>|<span data-ttu-id="394b4-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="394b4-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="394b4-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="394b4-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="394b4-122">Contient les propriétés de chaîne utilisées en tant que noms complets.</span><span class="sxs-lookup"><span data-stu-id="394b4-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="394b4-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="394b4-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="394b4-124">Contient les propriétés de chaîne utilisées en tant qu'adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="394b4-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="394b4-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="394b4-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="394b4-126">Contient les propriétés de chaîne utilisées comme types d'adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="394b4-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="394b4-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="394b4-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="394b4-128">Contient les propriétés binaires utilisées en tant qu'identificateurs d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="394b4-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="394b4-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="394b4-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="394b4-130">Contient les propriétés binaires utilisées en tant que clés de recherche.</span><span class="sxs-lookup"><span data-stu-id="394b4-130">Contains binary properties used as search keys.</span></span>  <br/> |
   


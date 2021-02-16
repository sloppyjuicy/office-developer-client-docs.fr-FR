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
# <a name="gateway-mappable-properties"></a><span data-ttu-id="476cc-103">Propriétés mappables de la passerelle</span><span class="sxs-lookup"><span data-stu-id="476cc-103">Gateway mappable properties</span></span>

<span data-ttu-id="476cc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="476cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="476cc-105">Les propriétés de passerelle mappables sont des propriétés qui peuvent nécessiter une traduction lorsqu’elles sont envoyées d’un domaine de messagerie à un autre.</span><span class="sxs-lookup"><span data-stu-id="476cc-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="476cc-106">Les propriétés mappables de passerelle MAPI permettent aux messages d’inclure des informations qui nécessitent une passerelle pour s’assurer que le système de messagerie de destination les utilise correctement.</span><span class="sxs-lookup"><span data-stu-id="476cc-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="476cc-107">Bien que les développeurs de passerelles ne soient pas obligés de fournir cette fonctionnalité de traduction, ils doivent considérer les propriétés de passerelle mappables comme une opportunité d’améliorer la gestion du contenu des messages.</span><span class="sxs-lookup"><span data-stu-id="476cc-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="476cc-108">MAPI spécifie cinq types de propriétés de passerelle mappables :</span><span class="sxs-lookup"><span data-stu-id="476cc-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="476cc-109">Nom unique (DN)</span><span class="sxs-lookup"><span data-stu-id="476cc-109">Display name</span></span>
    
- <span data-ttu-id="476cc-110">Nom complet</span><span class="sxs-lookup"><span data-stu-id="476cc-110">Email address</span></span>
    
- <span data-ttu-id="476cc-111">Type d’e-mail</span><span class="sxs-lookup"><span data-stu-id="476cc-111">Email type</span></span>
    
- <span data-ttu-id="476cc-112">Identificateur d’entrée</span><span class="sxs-lookup"><span data-stu-id="476cc-112">Entry identifier</span></span>
    
- <span data-ttu-id="476cc-113">Clé de recherche</span><span class="sxs-lookup"><span data-stu-id="476cc-113">Search key</span></span>
    
<span data-ttu-id="476cc-114">Il s’agit de l’ensemble des propriétés d’adressan associées aux destinataires, aux expéditeurs, aux destinataires de rapport et aux expéditeurs et destinataires délégués.</span><span class="sxs-lookup"><span data-stu-id="476cc-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="476cc-115">Pour aider votre client à définir ces propriétés afin qu’une passerelle les gère spécialement, MAPI spécifie une convention d’attribution de noms à l’aide de propriétés nommées et de jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="476cc-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="476cc-116">Il existe cinq jeux de propriétés pour contenir des propriétés nommées, les propriétés d’adressamage qui nécessitent un mappage.</span><span class="sxs-lookup"><span data-stu-id="476cc-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="476cc-117">Il existe un jeu de propriétés pour chaque type de propriété mappable.</span><span class="sxs-lookup"><span data-stu-id="476cc-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="476cc-118">Les jeux de propriétés qui vont contenir ces propriétés d’adressamage nommées sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="476cc-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="476cc-119">**Jeu de propriétés**</span><span class="sxs-lookup"><span data-stu-id="476cc-119">**Property set**</span></span>|<span data-ttu-id="476cc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="476cc-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="476cc-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="476cc-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="476cc-122">Contient des propriétés de chaîne utilisées comme noms d’affichage.</span><span class="sxs-lookup"><span data-stu-id="476cc-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="476cc-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="476cc-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="476cc-124">Contient des propriétés de chaîne utilisées comme adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="476cc-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="476cc-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="476cc-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="476cc-126">Contient des propriétés de chaîne utilisées comme types d’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="476cc-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="476cc-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="476cc-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="476cc-128">Contient des propriétés binaires utilisées comme identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="476cc-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="476cc-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="476cc-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="476cc-130">Contient des propriétés binaires utilisées comme clés de recherche.</span><span class="sxs-lookup"><span data-stu-id="476cc-130">Contains binary properties used as search keys.</span></span>  <br/> |
   


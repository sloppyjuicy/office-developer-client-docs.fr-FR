---
title: Propriétés de passerelle mappables
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 07c215511f010741e69c08c184df0ca3ce461e13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583616"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="4cba9-103">Propriétés de passerelle mappables</span><span class="sxs-lookup"><span data-stu-id="4cba9-103">Gateway mappable properties</span></span>

<span data-ttu-id="4cba9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cba9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cba9-105">Passerelle-mappables les propriétés qui peuvent nécessiter traduction lorsque envoyés à partir d’un domaine de messagerie à l’autre.</span><span class="sxs-lookup"><span data-stu-id="4cba9-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="4cba9-106">Propriétés de passerelle-mappables de MAPI autoriser les messages inclure des informations qui requiert une passerelle pour garantir la destination de système de messagerie utilise correctement.</span><span class="sxs-lookup"><span data-stu-id="4cba9-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="4cba9-107">Bien que les développeurs de passerelle ne sont pas tenus de fournir cette fonctionnalité de traduction, ils doivent envisager passerelle-mappables propriétés comme une opportunité pour améliorer la gestion du contenu du message.</span><span class="sxs-lookup"><span data-stu-id="4cba9-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="4cba9-108">MAPI spécifie cinq types de propriétés de passerelle-mappables :</span><span class="sxs-lookup"><span data-stu-id="4cba9-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="4cba9-109">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="4cba9-109">Display name</span></span>
    
- <span data-ttu-id="4cba9-110">Adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="4cba9-110">Email address</span></span>
    
- <span data-ttu-id="4cba9-111">Type de messagerie</span><span class="sxs-lookup"><span data-stu-id="4cba9-111">Email type</span></span>
    
- <span data-ttu-id="4cba9-112">Identificateur d’entrée</span><span class="sxs-lookup"><span data-stu-id="4cba9-112">Entry identifier</span></span>
    
- <span data-ttu-id="4cba9-113">Clé de recherche</span><span class="sxs-lookup"><span data-stu-id="4cba9-113">Search key</span></span>
    
<span data-ttu-id="4cba9-114">Il s’agit de l’ensemble des propriétés qui sont associées à des destinataires, les expéditeurs, destinataires des rapports et déléguées expéditeurs et destinataires d’adressage.</span><span class="sxs-lookup"><span data-stu-id="4cba9-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="4cba9-115">Pour vous aider à votre client de définir ces propriétés afin qu’une passerelle gère les spécialement, MAPI spécifie une convention d’affectation de noms à l’aide des propriétés nommées et les jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="4cba9-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="4cba9-116">Il existe cinq jeux de propriétés pour contenir des propriétés nommées, les propriétés d’adressage qui nécessitent un mappage.</span><span class="sxs-lookup"><span data-stu-id="4cba9-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="4cba9-117">Il existe une propriété définie pour chaque type de propriété mappable.</span><span class="sxs-lookup"><span data-stu-id="4cba9-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="4cba9-118">Les jeux de propriétés qui contiendront ces propriétés adressage sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4cba9-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="4cba9-119">**Jeu de propriétés**</span><span class="sxs-lookup"><span data-stu-id="4cba9-119">**Property set**</span></span>|<span data-ttu-id="4cba9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="4cba9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cba9-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="4cba9-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="4cba9-122">Contient les propriétés de chaîne utilisées comme noms complets.</span><span class="sxs-lookup"><span data-stu-id="4cba9-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="4cba9-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="4cba9-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="4cba9-124">Contient les propriétés de chaîne utilisées comme adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4cba9-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="4cba9-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="4cba9-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="4cba9-126">Contient les propriétés de chaîne utilisées en tant que types d’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4cba9-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="4cba9-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4cba9-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="4cba9-128">Contient des propriétés binaires utilisées comme les identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="4cba9-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="4cba9-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="4cba9-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="4cba9-130">Contient des propriétés binaires utilisées en tant que clés de recherche.</span><span class="sxs-lookup"><span data-stu-id="4cba9-130">Contains binary properties used as search keys.</span></span>  <br/> |
   


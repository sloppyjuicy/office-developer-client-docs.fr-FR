---
title: Types de fournisseurs de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406163"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="c6f9b-103">Types de fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="c6f9b-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="c6f9b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6f9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6f9b-105">Tous les fournisseurs de transport supportent une gamme de fonctionnalités standard, telles que :</span><span class="sxs-lookup"><span data-stu-id="c6f9b-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="c6f9b-106">Assurer une sécurité appropriée pour le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="c6f9b-107">Envoi et réception de messages à partir du système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="c6f9b-108">Exposition des types d’adresses que les fournisseurs de transport prendre en charge afin que lepooler MAPI et les applications clientes peuvent les utiliser correctement.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="c6f9b-109">Accepter la remise pour des destinataires spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="c6f9b-110">En outre, MAPI prend en charge deux types spécialisés de fournisseurs pour des systèmes de messagerie spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="c6f9b-111">**Type de transport**</span><span class="sxs-lookup"><span data-stu-id="c6f9b-111">**Transport type**</span></span>|<span data-ttu-id="c6f9b-112">**Fonctionnalités ajoutées**</span><span class="sxs-lookup"><span data-stu-id="c6f9b-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6f9b-113">Transport à distance</span><span class="sxs-lookup"><span data-stu-id="c6f9b-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="c6f9b-114">Active l’interopérabilité avec les clients connectés à distance.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="c6f9b-115">TNEF Transport</span><span class="sxs-lookup"><span data-stu-id="c6f9b-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="c6f9b-116">Permet de conserver les propriétés MAPI sur les systèmes de messagerie qui ne les prisent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="c6f9b-117">Les transports TNEF sont utilisés pour traduire des messages entre des systèmes de messagerie qui utilisent différents ensembles de propriétés MAPI.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="c6f9b-118">Les transports TNEF utilisent l’interface MAPI [ITnef : IUnknown](itnefiunknown.md) pour convertir les propriétés que le système de destination ne peut pas représenter directement en un flux de données binaires qui peut être joint au message.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="c6f9b-119">Par la suite, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et rendre les propriétés MAPI d’origine disponibles pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="c6f9b-120">En outre, la prise en charge du TNEF est requise si votre transport doit prendre en charge des classes de message personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="c6f9b-121">Pour plus d’informations sur l’implémentation des transports TNEF, voir [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6f9b-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="c6f9b-122">Si votre fournisseur de transport n’est pas de ce type, vous devez l’implémenter avec les fonctions MAPI de base et les fonctions réseau disponibles sur votre plateforme cible.</span><span class="sxs-lookup"><span data-stu-id="c6f9b-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  


---
title: Types de fournisseurs de Transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787390"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="b61cd-103">Types de fournisseurs de Transport</span><span class="sxs-lookup"><span data-stu-id="b61cd-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="b61cd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b61cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b61cd-105">Tous les fournisseurs de transport prennent en charge une variété de fonctionnalités standards, telles que :</span><span class="sxs-lookup"><span data-stu-id="b61cd-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="b61cd-106">Fournir une sécurité appropriée pour le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b61cd-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="b61cd-107">Envoi et réception de messages à partir du système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b61cd-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="b61cd-108">Exposer les types d’adresses les fournisseurs de transport prennent en charge le spouleur MAPI et les applications clientes peuvent les utiliser correctement.</span><span class="sxs-lookup"><span data-stu-id="b61cd-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="b61cd-109">Accepter la livraison pour des destinataires spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b61cd-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="b61cd-110">En outre, MAPI prend en charge deux types de fournisseurs spécialisés pour les systèmes de messagerie spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b61cd-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="b61cd-111">**Type de transport**</span><span class="sxs-lookup"><span data-stu-id="b61cd-111">**Transport type**</span></span>|<span data-ttu-id="b61cd-112">**Ajout de fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="b61cd-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b61cd-113">Transport à distance</span><span class="sxs-lookup"><span data-stu-id="b61cd-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="b61cd-114">Permet l’interopérabilité avec les clients connectés à distance.</span><span class="sxs-lookup"><span data-stu-id="b61cd-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="b61cd-115">Transport TNEF</span><span class="sxs-lookup"><span data-stu-id="b61cd-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="b61cd-116">Permet d’être perdues sur qui ne prennent pas en charge les systèmes de messagerie des propriétés MAPI.</span><span class="sxs-lookup"><span data-stu-id="b61cd-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="b61cd-117">Transports TNEF sont utilisés pour la traduction des messages entre les systèmes de messagerie qui prennent en charge différentes propriétés MAPI.</span><span class="sxs-lookup"><span data-stu-id="b61cd-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="b61cd-118">Transports TNEF utilisent l’interface MAPI [ITnef : IUnknown](itnefiunknown.md) interface pour convertir des propriétés représentant le système de destination ne peut pas directement dans un flux de données binaires qui peut être joint au message.</span><span class="sxs-lookup"><span data-stu-id="b61cd-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="b61cd-119">Ultérieurement, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et de rendre les propriétés MAPI d’origine disponibles pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="b61cd-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="b61cd-120">En outre, la prise en charge TNEF est requis si votre transport doit prendre en charge des classes de message personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b61cd-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="b61cd-121">Pour plus d’informations sur l’implémentation des transports TNEF, voir [développement d’un fournisseur de Transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b61cd-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="b61cd-122">Si votre fournisseur de transport n’est pas un de ces types, vous devrez implémenter avec les fonctions de base MAPI et les fonctions réseau disponibles sur votre plateforme cible.</span><span class="sxs-lookup"><span data-stu-id="b61cd-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  


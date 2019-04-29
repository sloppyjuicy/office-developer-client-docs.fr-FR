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
# <a name="types-of-transport-providers"></a><span data-ttu-id="fe991-103">Types de fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="fe991-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="fe991-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe991-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe991-105">Tous les fournisseurs de transport prennent en charge une gamme de fonctionnalités standard, telles que:</span><span class="sxs-lookup"><span data-stu-id="fe991-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="fe991-106">Assurer une sécurité appropriée pour le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fe991-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="fe991-107">Envoi et réception de messages à partir du système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fe991-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="fe991-108">En exposant les types d'adresses pris en charge par les fournisseurs de transport, le spouleur MAPI et les applications clientes peuvent les utiliser correctement.</span><span class="sxs-lookup"><span data-stu-id="fe991-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="fe991-109">Acceptation de la remise de destinataires spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fe991-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="fe991-110">De plus, MAPI prend en charge deux types de fournisseurs spécialisés pour des systèmes de messagerie spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fe991-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="fe991-111">**Type de transport**</span><span class="sxs-lookup"><span data-stu-id="fe991-111">**Transport type**</span></span>|<span data-ttu-id="fe991-112">**Fonctionnalités ajoutées**</span><span class="sxs-lookup"><span data-stu-id="fe991-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe991-113">Transport à distance</span><span class="sxs-lookup"><span data-stu-id="fe991-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="fe991-114">Permet l'interopérabilité avec les clients connectés à distance.</span><span class="sxs-lookup"><span data-stu-id="fe991-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="fe991-115">Transport TNEF</span><span class="sxs-lookup"><span data-stu-id="fe991-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="fe991-116">Permet de conserver les propriétés MAPI sur les systèmes de messagerie qui ne les prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="fe991-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="fe991-117">Les transports TNEF sont utilisés pour traduire les messages entre les systèmes de messagerie qui prennent en charge différents ensembles de propriétés MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe991-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="fe991-118">Les transports TNEF utilisent l'interface MAPI [ITnef: IUnknown](itnefiunknown.md) pour convertir les propriétés que le système de destination ne peut pas représenter directement dans un flux de données binaire qui peut être attaché au message.</span><span class="sxs-lookup"><span data-stu-id="fe991-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="fe991-119">Par la suite, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et mettre les propriétés MAPI d'origine à la disposition des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="fe991-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="fe991-120">En outre, la prise en charge de TNEF est requise si votre transport doit prendre en charge des classes de message personnalisées.</span><span class="sxs-lookup"><span data-stu-id="fe991-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="fe991-121">Pour plus d'informations sur l'implémentation des transports TNEF, consultez [la rubrique développement d'un fournisseur de transport compatible TNEF](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fe991-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="fe991-122">Si votre fournisseur de transport n'est pas l'un de ces types, vous devrez l'implémenter avec les fonctions MAPI de base et les fonctions réseau disponibles sur votre plateforme cible.</span><span class="sxs-lookup"><span data-stu-id="fe991-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  


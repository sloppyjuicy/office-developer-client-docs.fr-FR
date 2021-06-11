---
title: Vue d’ensemble du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433156"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="21911-103">Vue d’ensemble du fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="21911-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="21911-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21911-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21911-105">Un fournisseur de transport est une bibliothèque de liens dynamiques (DLL) qui agit comme un intermédiaire entre le sous-système MAPI et un ou plusieurs systèmes de messagerie sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="21911-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="21911-106">Un système de messagerie est un mécanisme spécifique par lequel les messages sont envoyés et reçus.</span><span class="sxs-lookup"><span data-stu-id="21911-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="21911-107">Voici quelques exemples de systèmes de messagerie :</span><span class="sxs-lookup"><span data-stu-id="21911-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="21911-108">Un système de fichiers réseau partagé dans qui le fournisseur de transport écrit directement des messages.</span><span class="sxs-lookup"><span data-stu-id="21911-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="21911-109">Interface réseau TCP/IP que le fournisseur de transport utilise pour se connecter à un serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="21911-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="21911-110">Service en ligne à qui les utilisateurs se connectent.</span><span class="sxs-lookup"><span data-stu-id="21911-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="21911-111">Une messagerie basée sur l’hôte ou un système d’automatisation Office.</span><span class="sxs-lookup"><span data-stu-id="21911-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="21911-112">Ensemble d’appels de procédure distante vers un serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="21911-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="21911-113">Tout ce qui peut être utilisé pour transférer des données d’un ordinateur à un autre.</span><span class="sxs-lookup"><span data-stu-id="21911-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="21911-114">Une DLL de fournisseur de transport doit être conforme à l’interface spécifiée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="21911-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="21911-115">En tant que développeur de fournisseurs de transport, vous implémentez cette interface en termes de fonctionnalités présentes dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="21911-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  


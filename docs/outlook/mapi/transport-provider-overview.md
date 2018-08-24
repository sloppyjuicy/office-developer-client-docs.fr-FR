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
ms.openlocfilehash: dbc56b7334d3966696641a84f23a64ce3802e3e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595271"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="e7bd5-103">Vue d’ensemble du fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="e7bd5-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="e7bd5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7bd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7bd5-105">Un fournisseur de transport est une bibliothèque de liens dynamiques (DLL) qui joue le rôle d’intermédiaire entre le sous-système MAPI et un ou plusieurs systèmes de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="e7bd5-106">Un système de messagerie est un mécanisme spécifique à laquelle les messages sont envoyés et reçus.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="e7bd5-107">Quelques exemples de systèmes de messagerie sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e7bd5-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="e7bd5-108">Un système de fichiers réseau partagé que le fournisseur de transport écrit les messages directement.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="e7bd5-109">Une interface réseau TCP/IP par le fournisseur de transport pour se connecter à un serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="e7bd5-110">Un service en ligne que les utilisateurs se connectent à.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="e7bd5-111">Un hôte de messagerie ou office automation système.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="e7bd5-112">Un ensemble d’appels de procédure distante à un serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="e7bd5-113">Tout ce qui peut être utilisé pour transférer des données à partir d’un ordinateur à un autre.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="e7bd5-114">Un DLL du fournisseur de transport doit être conforme à l’interface spécifiée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="e7bd5-115">En tant que développeur de fournisseur de transport, vous allez implémenter cette interface en termes de la fonctionnalité présente dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e7bd5-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  


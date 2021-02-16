---
title: Vue d’ensemble de la programmation MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408340"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="fe0ff-103">Vue d’ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="fe0ff-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="fe0ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe0ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe0ff-105">Cette référence MAPI (Microsoft Outlook Messaging API) est écrite pour les développeurs C et C++ ayant divers besoins et expériences en matière de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="fe0ff-106">Pour les développeurs qui souhaitent utiliser MAPI pour enrichir leurs applications qui disposent de fonctionnalités de messagerie, aucune connaissance préalable spécifique n’est requise.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="fe0ff-107">Vous avez besoin d’une expérience en messagerie et du modèle objet composant (COM) pour utiliser MAPI afin de créer des applications de groupe de travail à grande échelle ou des pilotes pour des services de système de messagerie spécialisés.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="fe0ff-108">Avant de commencer le travail de développement, vous devez prendre en compte les informations suivantes sur l’utilisation de MAPI, le processus d’accès et la façon dont les profils et les services de message sont créés et configurés.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="fe0ff-109">MapI (Messaging Application Program Interface) est un ensemble étendu de fonctions que les développeurs peuvent utiliser pour créer des applications à messagerie.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="fe0ff-110">La bibliothèque de fonctions complète est appelée MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="fe0ff-111">MAPI permet un contrôle total sur le système de messagerie sur l’ordinateur client, la création et la gestion des messages, la gestion de la boîte aux lettres cliente, les fournisseurs de services, etc.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe0ff-112">MapI étendu est identique à MAPI et est simplement appelé MAPI dans la documentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="fe0ff-113">**MAPI simple**</span><span class="sxs-lookup"><span data-stu-id="fe0ff-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="fe0ff-114">MapI simple fournit un ensemble de fonctions qui vous permet d’ajouter un niveau de base de fonctionnalité de messagerie aux applications Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fe0ff-115">La fonction MAPI Simple MAPISendMail est prise en charge par Microsoft Outlook 2013 et Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="fe0ff-116">D’autres fonctions MAPI simples ont été dépréciées dans Windows.</span><span class="sxs-lookup"><span data-stu-id="fe0ff-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  


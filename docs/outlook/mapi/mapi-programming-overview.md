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
ms.openlocfilehash: 177bd84addb001970e52801fd2cddba3a8d81706
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784660"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="d891d-103">Vue d’ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="d891d-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="d891d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d891d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d891d-105">Ce guide de référence de Microsoft Outlook MAPI (Messaging API) est écrit pour C et développeurs C++ avec une variété de besoins et expérience avec la messagerie.</span><span class="sxs-lookup"><span data-stu-id="d891d-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="d891d-106">Pour les développeurs qui souhaitent utiliser MAPI pour améliorer leurs applications qui ont des fonctionnalités de messagerie, sans connaissances préalables spécifique est requis.</span><span class="sxs-lookup"><span data-stu-id="d891d-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="d891d-107">Vous avez besoin d’un arrière-plan dans la messagerie et le composant COM (Object Model) à utiliser MAPI pour créer des applications de groupe de travail à grande échelle ou pilotes pour les services de système de messagerie spécialisés.</span><span class="sxs-lookup"><span data-stu-id="d891d-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="d891d-108">Avant de commencer le travail de développement, vous devez tenir compte les informations suivantes sur l’utilisation de MAPI, le processus d’ouverture de session, et comment les profils et les services de messagerie sont créés et configurés.</span><span class="sxs-lookup"><span data-stu-id="d891d-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="d891d-109">Le programme Interface MAPI (Messaging Application) est un ensemble complet de fonctions qui permet aux développeurs de créer des applications à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="d891d-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="d891d-110">La bibliothèque de fonctions complète est appelée MAPI.</span><span class="sxs-lookup"><span data-stu-id="d891d-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="d891d-111">MAPI permet de contrôler le système de messagerie sur l’ordinateur client, la création et la gestion des messages, de gestion de la boîte aux lettres cliente, fournisseurs de services et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d891d-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d891d-112">Interface MAPI étendue est identique à MAPI et est simplement appelé MAPI dans la documentation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d891d-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="d891d-113">**MAPI simple**</span><span class="sxs-lookup"><span data-stu-id="d891d-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="d891d-114">MAPI simple fournit un jeu de fonctions qui vous permet d’ajouter un niveau de base de la messagerie de fonctionnalités aux applications Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d891d-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d891d-115">La fonction MAPI Simple MAPISendMail est pris en charge par Microsoft Outlook 2013 et Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="d891d-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="d891d-116">Autres fonctions de l’interface Simple MAPI ont été déconseillées dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d891d-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  


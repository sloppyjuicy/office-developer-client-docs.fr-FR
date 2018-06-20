---
title: Vue d’ensemble du fournisseur de Transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784728"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="b6156-103">Vue d’ensemble du fournisseur de Transport MAPI</span><span class="sxs-lookup"><span data-stu-id="b6156-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="b6156-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6156-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6156-105">Fournisseurs de transport gérer la réception et transmission de message et implémentent la sécurité, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b6156-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="b6156-106">Ils s’occupent aussi de prétraitement nécessaires et les tâches de post-traitement.</span><span class="sxs-lookup"><span data-stu-id="b6156-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="b6156-107">Il est généralement un fournisseur de transport pour chaque système de messagerie active.</span><span class="sxs-lookup"><span data-stu-id="b6156-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="b6156-108">Les applications clientes communiquent avec le fournisseur de transport via un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="b6156-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="b6156-109">Fournisseurs de transport inscrire MAPI pour gérer un ou plusieurs types particuliers d’entrées de destinataire.</span><span class="sxs-lookup"><span data-stu-id="b6156-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="b6156-110">Lorsqu’un message est prêt à être envoyé, MAPI doit déterminer le fournisseur de transport doit gérer la transmission.</span><span class="sxs-lookup"><span data-stu-id="b6156-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="b6156-111">Selon le type de destinataire, MAPI peut être appelés même plus d’un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="b6156-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="b6156-112">Si un fournisseur de transport indisponible est le seul qui peut gérer le destinataire, la transmission de message sera différée jusqu'à ce qu’une connexion avec ce fournisseur peut être rétablie.</span><span class="sxs-lookup"><span data-stu-id="b6156-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="b6156-113">Certains systèmes de messagerie sont des systèmes d’informations sécurisé ; tous les utilisateurs potentiels doivent entrer un ensemble d’informations d’identification valides avant de pouvoir accéder.</span><span class="sxs-lookup"><span data-stu-id="b6156-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="b6156-114">MAPI empêche l’accès non autorisé à des systèmes de messagerie sécurisées organisez le fournisseur de transport de valider les informations d’identification au moment de l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b6156-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  


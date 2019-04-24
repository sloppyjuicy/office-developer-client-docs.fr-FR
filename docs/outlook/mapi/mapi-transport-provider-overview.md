---
title: Vue d'ensemble du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357343"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="3a615-103">Vue d'ensemble du fournisseur de transport MAPI</span><span class="sxs-lookup"><span data-stu-id="3a615-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="3a615-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a615-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a615-105">Les fournisseurs de transport gèrent la transmission et la réception des messages et implémentent la sécurité, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3a615-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="3a615-106">Elles prennent également en charge les tâches de prétraitement et de post-traitement nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3a615-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="3a615-107">Il existe généralement un fournisseur de transport pour chaque système de messagerie actif.</span><span class="sxs-lookup"><span data-stu-id="3a615-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="3a615-108">Les applications clientes communiquent avec le fournisseur de transport via un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="3a615-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="3a615-109">Les fournisseurs de transport s'inscrivent à MAPI pour gérer un ou plusieurs types d'entrées de destinataires spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3a615-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="3a615-110">Lorsqu'un message est prêt à être envoyé, MAPI doit déterminer quel fournisseur de transport doit gérer la transmission.</span><span class="sxs-lookup"><span data-stu-id="3a615-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="3a615-111">Selon le type de destinataire, MAPI peut même appeler sur plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="3a615-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="3a615-112">Si un fournisseur de transport non disponible est le seul à pouvoir gérer le destinataire, la transmission des messages est différée jusqu'à ce qu'une connexion avec ce fournisseur puisse être rétablie.</span><span class="sxs-lookup"><span data-stu-id="3a615-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="3a615-113">Certains systèmes de messagerie sont des systèmes sécurisés; tous les utilisateurs potentiels doivent entrer un ensemble d'informations d'identification valides avant d'autoriser l'accès.</span><span class="sxs-lookup"><span data-stu-id="3a615-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="3a615-114">MAPI empêche l'accès non autorisé à ce type de système de messagerie sécurisée en faisant en sorte que le fournisseur de transport valide les informations d'identification au moment de l'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="3a615-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  


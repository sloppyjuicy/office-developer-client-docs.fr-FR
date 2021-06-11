---
title: Outlook Interfaces de fournisseur Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) est une fonctionnalité de Office partagée par les applications clientes Office qui se connecte aux réseaux sociaux et professionnels afin que les utilisateurs restent en contact avec les personnes de leurs réseaux sans quitter Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422809"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="2e9c4-103">Outlook Interfaces de fournisseur Social Connector</span><span class="sxs-lookup"><span data-stu-id="2e9c4-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="2e9c4-104">Outlook Social Connector (OSC) est une fonctionnalité de Office partagée par les applications clientes Office qui se connecte aux réseaux sociaux et professionnels afin que les utilisateurs restent en contact avec les personnes de leurs réseaux sans quitter Office.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="2e9c4-105">Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l’OSC d’accéder aux données de réseau social d’une manière indépendante des API de chaque réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="2e9c4-106">Le tableau suivant répertorie les interfaces dans l’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="2e9c4-107">Un fournisseur OSC doit implémenter quatre des cinq interfaces pour communiquer avec l’OSC : [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)et [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2e9c4-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="2e9c4-108">Si le fournisseur OSC prend en charge la synchronisation des activités, la synchronisation à la demande ou hybride des amis, la mise en cache des informations d’identification de connexion et la connexion à l’aide des informations d’identification mises en cache, ou la possibilité de suivre une personne, le fournisseur doit également implémenter [ISocialSession2.](isocialsession2iunknown.md)</span><span class="sxs-lookup"><span data-stu-id="2e9c4-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="2e9c4-109">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e9c4-109">**Name**</span></span>|<span data-ttu-id="2e9c4-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e9c4-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e9c4-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="2e9c4-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="2e9c4-112">Représente une personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="2e9c4-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="2e9c4-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="2e9c4-114">Représente l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="2e9c4-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="2e9c4-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="2e9c4-116">Représente une instance d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="2e9c4-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="2e9c4-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="2e9c4-118">Représente une connexion à un site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="2e9c4-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="2e9c4-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="2e9c4-120">Prend en charge la synchronisation des activités, l’ajout d’amis, la synchronisation à la demande ou hybride d’amis, ou la connexion au réseau social à l’aide d’informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="2e9c4-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   


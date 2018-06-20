---
title: Interfaces de fournisseur Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: L’Outlook Social Connector (OSC) est une fonctionnalité Office partagée par les applications clientes Office qui se connecte à la mise en réseau et réseaux d’entreprise afin que les utilisateurs peuvent rester en contact avec les personnes figurant dans leurs réseaux sans quitter Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787702"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="fc6cb-103">Interfaces de fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="fc6cb-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="fc6cb-104">L’Outlook Social Connector (OSC) est une fonctionnalité Office partagée par les applications clientes Office qui se connecte à la mise en réseau et réseaux d’entreprise afin que les utilisateurs peuvent rester en contact avec les personnes figurant dans leurs réseaux sans quitter Office.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="fc6cb-105">Un fournisseur OSC est un composant COM (Object Model) DLL qui permet à l’OSC accéder aux données de réseau social de façon indépendante des API de chaque réseau social.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="fc6cb-106">Le tableau suivant répertorie les interfaces de l’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="fc6cb-107">Un fournisseur OSC doit implémenter quatre des cinq interfaces pour communiquer avec l’OSC : [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)et [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="fc6cb-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="fc6cb-108">Si le fournisseur OSC prend en charge les activités de synchronisation, à la demande ou la synchronisation hybride d’amis, la mise en cache des informations d’identification d’ouverture de session et l’ouverture de session à l’aide de mis en cache les informations d’identification, ou la possibilité de suivre une personne, le fournisseur doit implémenter [ISocialSession2 ](isocialsession2iunknown.md), ainsi que.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="fc6cb-109">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fc6cb-109">**Name**</span></span>|<span data-ttu-id="fc6cb-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc6cb-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc6cb-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="fc6cb-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="fc6cb-112">Représente une personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="fc6cb-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="fc6cb-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="fc6cb-114">Représente l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="fc6cb-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="fc6cb-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="fc6cb-116">Représente une instance d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="fc6cb-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="fc6cb-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="fc6cb-118">Représente une connexion à un site de réseau social.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="fc6cb-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="fc6cb-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="fc6cb-120">Prend en charge la synchronisation des activités, ajout de contacts, de la synchronisation de la demande ou hybride d’amis ou ouvrant une session sur le réseau social à l’aide de mises en cache les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc6cb-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   


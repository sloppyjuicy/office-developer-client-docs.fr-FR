---
title: Fournisseur de transport et spouleur MAPI modèle opérationnel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0e6c38091e5b2e10e82012bc470ea41037f57c7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787384"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="3560c-103">Fournisseur de transport et spouleur MAPI modèle opérationnel</span><span class="sxs-lookup"><span data-stu-id="3560c-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="3560c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3560c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3560c-105">Initialisation de fournisseur de transport, démarrage, traitement, l’arrêt et deinitialization sont effectuées par une série d’appels du spouleur MAPI vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="3560c-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="3560c-106">Les appels sont classés comme suit :</span><span class="sxs-lookup"><span data-stu-id="3560c-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="3560c-107">Le spouleur MAPI appelle la fonction [XPProviderInit](xpproviderinit.md) , passe un objet de prise en charge, obtient l’objet de fournisseur et vérifie que le fournisseur de transport et le spouleur MAPI prennent en charge les numéros de version une plage compatible de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3560c-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="3560c-108">Le spouleur MAPI appelle la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de la [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="3560c-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="3560c-109">Une session est établie entre le spouleur MAPI et le fournisseur de transport avec les informations d’identification dans la section du profil actuelle.</span><span class="sxs-lookup"><span data-stu-id="3560c-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="3560c-110">Le fournisseur de transport renvoie un objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="3560c-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="3560c-111">Le spouleur MAPI appelle la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="3560c-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="3560c-112">Le fournisseur de transport renvoie une liste des identificateurs uniques (UID) et des types d’adresse de messagerie qu’il accepte.</span><span class="sxs-lookup"><span data-stu-id="3560c-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="3560c-113">Le fournisseur de transport appelle la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer une ligne dans la table d’état MAPI.</span><span class="sxs-lookup"><span data-stu-id="3560c-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="3560c-114">Le spouleur MAPI appelle la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour activer la réception et transmission de message.</span><span class="sxs-lookup"><span data-stu-id="3560c-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="3560c-115">Si vous avez demandé par le fournisseur de transport dans son retour pour l’appel de **TransportLogon** , le spouleur MAPI appelle régulièrement la méthode [IXPLogon::Idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="3560c-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="3560c-116">Traitement inactif est utile si le fournisseur de transport doit interroger le système de messagerie sous-jacent pour les nouveaux messages ou effectuer d’autres tâches de priorité basse.</span><span class="sxs-lookup"><span data-stu-id="3560c-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="3560c-117">Le spouleur MAPI et le fournisseur de transport envoyer et recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="3560c-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="3560c-118">Pour plus d’informations, voir [Modèle d’envoi de Message](message-submission-model.md) et le [Modèle de réception de messages](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="3560c-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="3560c-119">Le spouleur MAPI de demandes de transport et appelle sur les objets de prise en charge, le message et des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="3560c-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="3560c-120">Le spouleur MAPI appelle la méthode **TransportNotify** pour désactiver la réception et transmission de message.</span><span class="sxs-lookup"><span data-stu-id="3560c-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="3560c-121">Le spouleur MAPI libère les objets d’ouverture de session et le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3560c-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="3560c-122">Pour plus d’informations, voir la méthode [IXPProvider::Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="3560c-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    


---
title: Fournisseur de transport et modèle opérationnel du spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426624"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="0c603-103">Fournisseur de transport et modèle opérationnel du spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="0c603-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="0c603-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c603-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c603-105">L’initialisation, le démarrage, le traitement, l’arrêt et la désinitialisation du fournisseur de transport sont effectués par une série d’appels dupooler MAPI au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="0c603-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="0c603-106">Les appels sont séquencés comme suit :</span><span class="sxs-lookup"><span data-stu-id="0c603-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="0c603-107">Lepooler MAPI appelle la fonction [XPProviderInit,](xpproviderinit.md) transmet un objet de support, obtient l’objet fournisseur et vérifie que le fournisseur de transport et lepooler MAPI prend en charge une plage compatible de numéros de version MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c603-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="0c603-108">Lepooler MAPI appelle la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de l’interface [IXPProvider : IUnknown.](ixpprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0c603-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="0c603-109">Une session est établie entre lepooler MAPI et le fournisseur de transport avec les informations d’identification dans la section actuelle du profil.</span><span class="sxs-lookup"><span data-stu-id="0c603-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="0c603-110">Le fournisseur de transport renvoie un objet d’accès.</span><span class="sxs-lookup"><span data-stu-id="0c603-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="0c603-111">Lepooler MAPI appelle la [méthode IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="0c603-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="0c603-112">Le fournisseur de transport renvoie une liste des identificateurs uniques (IUD) et des types d’adresse de messagerie qu’il acceptera.</span><span class="sxs-lookup"><span data-stu-id="0c603-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="0c603-113">Le fournisseur de transport appelle la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer sa ligne dans la table d’état MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c603-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="0c603-114">Lepooler MAPI appelle la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour activer la transmission et la réception des messages.</span><span class="sxs-lookup"><span data-stu-id="0c603-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="0c603-115">Si le fournisseur de transport le demande dans son retour pour l’appel **TransportLogon,** lepooler MAPI appelle régulièrement la méthode [IXPLogon::Idle.](ixplogon-idle.md)</span><span class="sxs-lookup"><span data-stu-id="0c603-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="0c603-116">Le traitement inactif est utile si le fournisseur de transport doit sondé le système de messagerie sous-jacent à la recherche de nouveaux messages ou effectuer d’autres tâches de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="0c603-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="0c603-117">Le fournisseur de transport et lepooler MAPI envoient et reçoivent des messages.</span><span class="sxs-lookup"><span data-stu-id="0c603-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="0c603-118">Pour plus d’informations, [voir modèle de dépôt de message](message-submission-model.md) et modèle de réception de [message.](message-reception-model.md)</span><span class="sxs-lookup"><span data-stu-id="0c603-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="0c603-119">Lepooler MAPI traite les demandes de transport et les appels sur les objets de support, de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="0c603-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="0c603-120">Lepooler MAPI appelle la **méthode TransportNotify** pour désactiver la transmission et la réception des messages.</span><span class="sxs-lookup"><span data-stu-id="0c603-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="0c603-121">Lepooler MAPI libère les objets d’accès et de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0c603-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="0c603-122">Pour plus d’informations, voir la [méthode IXPProvider::Shutdown.](ixpprovider-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="0c603-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    


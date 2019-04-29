---
title: Fournisseur de transport et modèle opérationnel de spouleur MAPI
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
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="5fbd7-103">Fournisseur de transport et modèle opérationnel de spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="5fbd7-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="5fbd7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fbd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fbd7-105">L'initialisation, le démarrage, le traitement, l'arrêt et la désinitialisation des fournisseurs de transport sont effectués par une série d'appels depuis le spouleur MAPI vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="5fbd7-106">Les appels sont séquencés comme suit:</span><span class="sxs-lookup"><span data-stu-id="5fbd7-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="5fbd7-107">Le spouleur MAPI appelle la fonction [XPProviderInit](xpproviderinit.md) , transmet un objet de prise en charge, obtient l'objet fournisseur et vérifie que le fournisseur de transport et le spouleur MAPI prennent en charge une plage de numéros de version MAPI compatible.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="5fbd7-108">Le spouleur MAPI appelle la méthode [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) de l'interface [IXPProvider: IUnknown](ixpprovideriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbd7-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="5fbd7-109">Une session est établie entre le spouleur MAPI et le fournisseur de transport avec les informations d'identification dans la section actuelle du profil.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="5fbd7-110">Le fournisseur de transport renvoie un objet Logon.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="5fbd7-111">Le spouleur MAPI appelle la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbd7-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="5fbd7-112">Le fournisseur de transport renvoie une liste des identificateurs uniques (UID) et des types d'adresses de messagerie qu'il accepte.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="5fbd7-113">Le fournisseur de transport appelle la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer sa ligne dans la table d'État MAPI.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="5fbd7-114">Le spouleur MAPI appelle la méthode [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) pour activer la transmission et la réception des messages.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="5fbd7-115">Si le fournisseur de transport le demande, le spouleur \*\*\*\* MAPI appelle régulièrement la méthode [IXPLogon:: Idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbd7-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="5fbd7-116">Le traitement inActif est utile si le fournisseur de transport doit interroger le système de messagerie sous-jacent pour les nouveaux messages ou effectuer d'autres tâches de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="5fbd7-117">Le fournisseur de transport et le spouleur MAPI envoient et reçoivent les messages.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="5fbd7-118">Pour plus d'informations, voir modèle d' [envoi de messages](message-submission-model.md) et modèle de [réception des messages](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd7-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="5fbd7-119">Les services de spouleur MAPI transportent les demandes et les appels sur les objets de support, de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="5fbd7-120">Le spouleur MAPI appelle la méthode **TransportNotify** pour désactiver la transmission et la réception des messages.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="5fbd7-121">Le spouleur MAPI libère les objets Logon et Provider.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="5fbd7-122">Pour plus d'informations, reportez-vous à la méthode [IXPProvider:: Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbd7-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    


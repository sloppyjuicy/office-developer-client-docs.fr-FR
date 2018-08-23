---
title: Arrêt d’un fournisseur de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1c7ae4ab6de20d69581a98323c14a2c15f436cad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572822"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="90395-103">Arrêt d’un fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="90395-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="90395-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90395-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90395-105">Si votre fournisseur est un fournisseur de magasin de message, il peut être arrêté d’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="90395-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="90395-106">Lorsqu’un client ou le spouleur MAPI appelle [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="90395-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="90395-107">Arrêt d’un fournisseur de banque de messages avec **StoreLogoff** entraîne l’arrêt se produise de manière ordonnée et mieux contrôlée.</span><span class="sxs-lookup"><span data-stu-id="90395-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="90395-108">Lorsqu’un client appelle [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="90395-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="90395-109">Votre implémentation de **IMsgStore::StoreLogoff** doit commencer en appelant [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) pour informer MAPI qu’il est arrêté, indiquant que tous les fournisseurs de transport associées doivent être déconnectés.</span><span class="sxs-lookup"><span data-stu-id="90395-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="90395-110">**IMsgStore::StoreLogoff** retourne son appelant appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="90395-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="90395-111">Mettre en œuvre cette méthode **version** en appelant la méthode **IUnknown::Release** de l’objet de la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="90395-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="90395-112">MAPI effectue les tâches suivantes dans son implémentation de **IUnknown::Release** pour les magasins de message :</span><span class="sxs-lookup"><span data-stu-id="90395-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="90395-113">Supprime toutes les structures [MAPIUID](mapiuid.md) enregistrés par le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="90395-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="90395-114">Supprime la ligne du fournisseur de banque de messages à partir de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="90395-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="90395-115">Appelle [IMSLogon::Logoff](imslogon-logoff.md) pour libérer tous les objets ouverts, sous-objets et objets d’état.</span><span class="sxs-lookup"><span data-stu-id="90395-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="90395-116">Appelle [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer l’objet de connexion du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="90395-116">Calls [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="90395-117">Certains clients peuvent omettre l’appel à **IMsgStore::StoreLogoff**, l’arrêt de votre fournisseur de magasin de message avec l’appel de méthode de **IUnknown::Release** de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="90395-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="90395-118">Un arrêt dans ces circonstances sans l’appel à **StoreLogoff** est moins ordonnée et mieux contrôlée.</span><span class="sxs-lookup"><span data-stu-id="90395-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="90395-119">Écrire la méthode de **publication** de votre banque de messages pour gérer cette possibilité et de garder une trace des ou non un appel à **IMAPISupport::StoreLogoffTransports** s’est produite.</span><span class="sxs-lookup"><span data-stu-id="90395-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="90395-120">**StoreLogoffTransports** doit être appelée qu’une seule fois pendant le processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="90395-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="90395-121">Si vous détectez dans votre méthode **version** que **StoreLogoffTransports** n’a pas encore été appelée, l’appel avec l’indicateur LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="90395-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90395-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90395-122">See also</span></span>



[<span data-ttu-id="90395-123">Arrêt d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="90395-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)


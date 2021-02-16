---
title: Arrêt d’un fournisseur de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339199"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="9d98b-103">Arrêt d’un fournisseur de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="9d98b-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="9d98b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d98b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d98b-105">Si votre fournisseur est un fournisseur de magasins de messages, il peut être fermé de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d98b-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="9d98b-106">Lorsqu’un client ou lepooler MAPI appelle [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="9d98b-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="9d98b-107">L’arrêt d’un fournisseur de magasins de messages avec **StoreLogoff** entraîne l’arrêt de manière ordonnée et contrôlée.</span><span class="sxs-lookup"><span data-stu-id="9d98b-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="9d98b-108">Lorsqu’un client appelle [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="9d98b-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="9d98b-109">Votre implémentation **d’IMsgStore::StoreLogoff** doit commencer par appeler [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) pour informer MAPI qu’il est en cours d’arrêt, indiquant que tous les fournisseurs de transport associés doivent être déconnectés.</span><span class="sxs-lookup"><span data-stu-id="9d98b-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="9d98b-110">Lorsque **IMsgStore::StoreLogoff** renvoie, son appelant appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de votre magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="9d98b-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="9d98b-111">**Implémentez cette méthode Release** en appelant la méthode **IUnknown::Release** de l’objet de support.</span><span class="sxs-lookup"><span data-stu-id="9d98b-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="9d98b-112">MAPI effectue les tâches suivantes dans son implémentation de **IUnknown::Release** pour les magasins de messages :</span><span class="sxs-lookup"><span data-stu-id="9d98b-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="9d98b-113">Supprime toutes les structures [MAPIUID](mapiuid.md) inscrites par le fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="9d98b-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="9d98b-114">Supprime la ligne du fournisseur de la boutique de messages de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="9d98b-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="9d98b-115">Appelle [IMSLogon::Logoff](imslogon-logoff.md) pour libérer tous les objets ouverts, sous-objets et objets d’état.</span><span class="sxs-lookup"><span data-stu-id="9d98b-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="9d98b-116">Appelle [IUnknown::Release pour](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) libérer l’objet d’ouverture de messagerie du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="9d98b-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="9d98b-117">Certains clients peuvent omettre l’appel à **IMsgStore::StoreLogoff**, en initie l’arrêt de votre fournisseur de magasins de messages avec l’appel à la méthode **IUnknown::Release** de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="9d98b-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="9d98b-118">Un arrêt dans ces circonstances sans l’appel **de StoreLogoff** est moins ordonné et contrôlé.</span><span class="sxs-lookup"><span data-stu-id="9d98b-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="9d98b-119">Écrivez la méthode **Release** de votre magasin de messages pour gérer cette possibilité et savoir si un appel à **IMAPISupport::StoreLogoffTransports** s’est produit ou non.</span><span class="sxs-lookup"><span data-stu-id="9d98b-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="9d98b-120">**StoreLogoffTransports** doit être appelé une seule fois pendant le processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="9d98b-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="9d98b-121">Si vous détectez dans votre méthode **Release** que **StoreLogoffTransports** n’a pas encore été appelé, étiquetez-le avec l’LOGOFF_ABORT de publication.</span><span class="sxs-lookup"><span data-stu-id="9d98b-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d98b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d98b-122">See also</span></span>



[<span data-ttu-id="9d98b-123">Arrêt d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="9d98b-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)


---
title: Chargement des fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307804"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="df70b-103">Chargement des fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="df70b-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="df70b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df70b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df70b-105">Lorsqu'une application cliente ouvre une banque de messages, MAPI charge la DLL du fournisseur de banque de messages dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="df70b-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="df70b-106">Une fois que MAPI a chargé la DLL, une séquence d'appels de méthode très spécifique se produit entre le fournisseur de banque de messages et MAPI.</span><span class="sxs-lookup"><span data-stu-id="df70b-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="df70b-107">Cette séquence d'appels de méthode permet à MAPI d'obtenir des IMSProvider de niveau supérieur [: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)et [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces, et permet au fournisseur de banque de messages d'obtenir un objet de prise en charge MAPI.</span><span class="sxs-lookup"><span data-stu-id="df70b-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="df70b-108">Après la séquence d'appels, le fournisseur de banque de messages doit être prêt à accepter les ouvertures de session des clients.</span><span class="sxs-lookup"><span data-stu-id="df70b-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="df70b-109">La séquence d'appels lorsqu'une DLL de fournisseur de messages est chargée est la suivante:</span><span class="sxs-lookup"><span data-stu-id="df70b-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="df70b-110">Le client appelle [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="df70b-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="df70b-111">Si la Banque de messages n'est pas déjà ouverte, MAPI charge la DLL du fournisseur de magasin et appelle le point d'entrée [MSProviderInit](msproviderinit.md) de la dll.</span><span class="sxs-lookup"><span data-stu-id="df70b-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="df70b-112">Si la Banque de messages est déjà ouverte, MAPI ignore les étapes 2 et 3, puis utilise l'interface [IMSProvider: IUnknown](imsprovideriunknown.md) existante pour effectuer l'étape 4.</span><span class="sxs-lookup"><span data-stu-id="df70b-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="df70b-113">**MSProviderInit** crée et renvoie un objet **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="df70b-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="df70b-114">MAPI appelle [IMSProvider:: Logon](imsprovider-logon.md), en transmettant l'identificateur d'entrée de la Banque de messages de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="df70b-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="df70b-115">**IMSProvider:: Logon** crée et renvoie une interface [IMSLogon: IUnknown](imslogoniunknown.md) et une interface [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) , puis appelle la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) sur son interface [IMAPISupport: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="df70b-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="df70b-116">Si l'identificateur d'entrée de la Banque de messages du client fait référence à une banque de messages qui est déjà ouverte, le fournisseur de banque de messages peut renvoyer des interfaces **IMSLogon** et **IMsgStore** existantes et n'a pas besoin d'appeler **AddRef** sur son objet de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df70b-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="df70b-117">Si le client n'a pas défini l'indicateur MAPI_NO_MAIL lorsqu'il a ouvert une session et qu'il n'a pas défini le MDB_NO_MAIL à l'étape 1, MAPI envoie l'identificateur d'entrée de la Banque de messages au spouleur MAPI afin que le spouleur MAPI puisse se connecter à la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="df70b-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="df70b-118">MAPI renvoie l'interface **IMsgStore** au client.</span><span class="sxs-lookup"><span data-stu-id="df70b-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="df70b-119">Le spouleur MAPI appelle [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="df70b-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="df70b-120">**IMSProvider:: SpoolerLogon** renvoie les mêmes interfaces **IMSLogon** et **IMsgStore** à partir de l'étape 5.</span><span class="sxs-lookup"><span data-stu-id="df70b-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="df70b-121">Si l'appel de connexion au fournisseur de banque de messages échoue car un mot de passe incorrect a été fourni et que le fournisseur de banque de messages ne peut pas afficher une interface pour demander le mot de passe correct, il doit renvoyer MAPI_E_FAILONEPROVIDER à partir de l' \*\*IMSProvider:: Logon. \*\*méthode.</span><span class="sxs-lookup"><span data-stu-id="df70b-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="df70b-122">Cela permet aux clients d'inviter l'utilisateur à entrer un mot de passe pour essayer de se reconnecter au fournisseur de banque de messages au lieu de provoquer l'échec de MAPI pour l'ensemble de la session.</span><span class="sxs-lookup"><span data-stu-id="df70b-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df70b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df70b-123">See also</span></span>



[<span data-ttu-id="df70b-124">Développement d’un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="df70b-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)


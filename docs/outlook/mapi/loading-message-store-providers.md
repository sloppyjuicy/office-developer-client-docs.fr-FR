---
title: Fournisseurs de banque de messages de chargement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 96e2ca38391931508dd9f3f78f3ba69e6f8b9c15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784522"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="84602-103">Fournisseurs de banque de messages de chargement</span><span class="sxs-lookup"><span data-stu-id="84602-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="84602-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84602-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84602-105">Lorsqu’une application cliente ouvre une banque de messages, MAPI charge DLL du fournisseur de banque de messages en mémoire.</span><span class="sxs-lookup"><span data-stu-id="84602-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="84602-106">Une fois que MAPI charge la DLL, une séquence spécifique d’appels de méthode se produit entre le fournisseur de banque de messages et MAPI.</span><span class="sxs-lookup"><span data-stu-id="84602-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="84602-107">Séquence d’appel de cette méthode permet de MAPI obtenir un niveau supérieur [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), et [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces et permet au fournisseur de banque de messages obtenir un objet de prise en charge MAPI.</span><span class="sxs-lookup"><span data-stu-id="84602-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="84602-108">Après la séquence d’appel, le fournisseur de banque de message doit être prêt à accepter les connexions à partir de clients.</span><span class="sxs-lookup"><span data-stu-id="84602-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="84602-109">La séquence d’appel lorsqu’un fournisseur de message que DLL est chargée est la suivante :</span><span class="sxs-lookup"><span data-stu-id="84602-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="84602-110">Le client appelle [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="84602-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="84602-111">Si la banque de messages n’est pas déjà ouverte, MAPI charge la DLL du fournisseur de magasin et appelle le point d’entrée de la DLL [MSProviderInit](msproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="84602-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="84602-112">Si la banque de messages est déjà ouverte, MAPI ignore les étapes 2 et 3, puis utilise l’instruction [IMSProvider : IUnknown](imsprovideriunknown.md) interface à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="84602-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="84602-113">**MSProviderInit** crée et renvoie un objet **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="84602-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="84602-114">Les appels MAPI [IMSProvider::Logon](imsprovider-logon.md), passant l’identificateur d’entrée de l’application cliente message store.</span><span class="sxs-lookup"><span data-stu-id="84602-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="84602-115">**IMSProvider::Logon** crée et renvoie une [IMSLogon : IUnknown](imslogoniunknown.md) interface et un [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) de l’interface et appelle ensuite la méthode [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) sur son [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="84602-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="84602-116">Si le message du client stockage identificateur d’entrée fait référence à une banque de messages est déjà ouverte, le fournisseur de banque de message peut retourner des interfaces **IMSLogon** et **IMsgStore** existants n’a pas besoin d’appeler **AddRef** sur son objet prise en charge.</span><span class="sxs-lookup"><span data-stu-id="84602-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="84602-117">Si le client n’a pas défini l’indicateur MAPI_NO_MAIL lorsqu’il ouvre une session et il n’a pas défini le MDB_NO_MAIL à l’étape 1, MAPI permettant d’identificateur d’entrée de la banque de messages le spouleur MAPI afin que le spouleur MAPI peut se connecter à la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="84602-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="84602-118">MAPI renvoie l’interface **IMsgStore** au client.</span><span class="sxs-lookup"><span data-stu-id="84602-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="84602-119">Le spouleur MAPI appelle [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="84602-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="84602-120">**IMSProvider::SpoolerLogon** renvoie les mêmes interfaces **IMSLogon** et **IMsgStore** à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="84602-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="84602-121">Si l’appel d’ouverture de session au message stocker fournisseur échoue, car un mot de passe incorrect a été fourni et le fournisseur de banque de message ne peut pas afficher une interface pour demander le mot de passe, il doit renvoyer la référence à MAPI_E_FAILONEPROVIDER à partir de la **IMSProvider::Logon **méthode.</span><span class="sxs-lookup"><span data-stu-id="84602-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="84602-122">Cela permettra aux clients d’inviter l’utilisateur à un mot de passe pour essayer de se connecter au fournisseur de magasin de message à nouveau au lieu d’entraînant l’échec du fournisseur pour l’ensemble de la session MAPI.</span><span class="sxs-lookup"><span data-stu-id="84602-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84602-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84602-123">See also</span></span>



[<span data-ttu-id="84602-124">D�veloppement d'un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="84602-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)


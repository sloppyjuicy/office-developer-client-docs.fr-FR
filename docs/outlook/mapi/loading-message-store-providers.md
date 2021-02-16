---
title: Chargement des fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307804"
---
# <a name="loading-message-store-providers"></a>Chargement des fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’une application cliente ouvre une magasin de messages, MAPI charge la DLL du fournisseur de la boutique de messages en mémoire. Une fois que MAPI a chargé la DLL, une séquence très spécifique d’appels de méthode se produit entre le fournisseur de la boutique de messages et MAPI. Cette séquence d’appels de méthode permet à MAPI d’obtenir des interfaces [IMSProvider de](imsprovideriunknown.md)niveau supérieur : IUnknown , [IMSLogon : IUnknown](imslogoniunknown.md)et [IMsgStore : interfaces IMAPIProp,](imsgstoreimapiprop.md) et permet au fournisseur de magasin de messages d’obtenir un objet de support MAPI. Après la séquence d’appels, le fournisseur de magasin de messages doit être prêt à accepter les connexions des clients. 
  
La séquence d’appels lors du chargement d’une DLL de fournisseur de messages est la suivante :
  
1. Le client appelle [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Si la magasin de messages n’est pas déjà ouverte, MAPI charge la DLL du fournisseur de magasins et appelle le point d’entrée [MSProviderInit](msproviderinit.md) de la DLL. Si la magasin de messages est déjà ouverte, MAPI ignore les étapes 2 et 3, puis utilise l’interface [IMSProvider : IUnknown](imsprovideriunknown.md) existante pour effectuer les étapes 4. 
    
3. **MSProviderInit crée** et renvoie un **objet IMSProvider.** 
    
4. MAPI appelle [IMSProvider::Logon](imsprovider-logon.md), en passant l’identificateur d’entrée de magasin de messages de l’application cliente.
    
5. **IMSProvider::Logon** crée et renvoie une interface [IMSLogon : IUnknown](imslogoniunknown.md) et une interface [IMsgStore : IMAPIProp,](imsgstoreimapiprop.md) puis appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) sur son interface [IMAPISupport : IUnknown.](imapisupportiunknown.md) Si l’identificateur d’entrée de la magasin de messages du client fait référence à une magasin de messages déjà ouverte, le fournisseur de magasin de messages peut renvoyer les interfaces **IMSLogon** et **IMsgStore** existantes et n’a pas besoin d’appeler **AddRef** sur son objet de support. 
    
6. Si le client n’a pas définie l’indicateur MAPI_NO_MAIL lorsqu’il s’est connecté et qu’il n’a pas définie le MDB_NO_MAIL à l’étape 1, MAPI fournit l’identificateur d’entrée de la boutique de messages aupooler MAPI afin que lepooler MAPI puisse se connecter à la magasin de messages.
    
7. MAPI renvoie **l’interface IMsgStore** au client. 
    
8. Lepooler MAPI appelle [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** renvoie les mêmes interfaces **IMSLogon** et **IMsgStore** de l’étape 5. 
    
> [!NOTE]
> Si l’appel d’ouverture de conférence au fournisseur de magasins de messages échoue parce qu’un mot de passe incorrect a été fourni et que le fournisseur de la boutique de messages ne peut pas afficher une interface pour demander le mot de passe correct, il doit renvoyer MAPI_E_FAILONEPROVIDER à partir de la méthode **IMSProvider::Logon.** Cela permettra aux clients d’inviter l’utilisateur à obtenir un mot de passe pour essayer de se connecter à nouveau au fournisseur de la boutique de messages au lieu de provoquer l’échec de MAPI pour le fournisseur pendant toute la session. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)


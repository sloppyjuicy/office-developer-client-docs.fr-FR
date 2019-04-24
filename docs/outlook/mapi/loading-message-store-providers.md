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
# <a name="loading-message-store-providers"></a>Chargement des fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'une application cliente ouvre une banque de messages, MAPI charge la DLL du fournisseur de banque de messages dans la mémoire. Une fois que MAPI a chargé la DLL, une séquence d'appels de méthode très spécifique se produit entre le fournisseur de banque de messages et MAPI. Cette séquence d'appels de méthode permet à MAPI d'obtenir des IMSProvider de niveau supérieur [: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)et [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces, et permet au fournisseur de banque de messages d'obtenir un objet de prise en charge MAPI. Après la séquence d'appels, le fournisseur de banque de messages doit être prêt à accepter les ouvertures de session des clients. 
  
La séquence d'appels lorsqu'une DLL de fournisseur de messages est chargée est la suivante:
  
1. Le client appelle [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).
    
2. Si la Banque de messages n'est pas déjà ouverte, MAPI charge la DLL du fournisseur de magasin et appelle le point d'entrée [MSProviderInit](msproviderinit.md) de la dll. Si la Banque de messages est déjà ouverte, MAPI ignore les étapes 2 et 3, puis utilise l'interface [IMSProvider: IUnknown](imsprovideriunknown.md) existante pour effectuer l'étape 4. 
    
3. **MSProviderInit** crée et renvoie un objet **IMSProvider** . 
    
4. MAPI appelle [IMSProvider:: Logon](imsprovider-logon.md), en transmettant l'identificateur d'entrée de la Banque de messages de l'application cliente.
    
5. **IMSProvider:: Logon** crée et renvoie une interface [IMSLogon: IUnknown](imslogoniunknown.md) et une interface [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) , puis appelle la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) sur son interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . Si l'identificateur d'entrée de la Banque de messages du client fait référence à une banque de messages qui est déjà ouverte, le fournisseur de banque de messages peut renvoyer des interfaces **IMSLogon** et **IMsgStore** existantes et n'a pas besoin d'appeler **AddRef** sur son objet de prise en charge. 
    
6. Si le client n'a pas défini l'indicateur MAPI_NO_MAIL lorsqu'il a ouvert une session et qu'il n'a pas défini le MDB_NO_MAIL à l'étape 1, MAPI envoie l'identificateur d'entrée de la Banque de messages au spouleur MAPI afin que le spouleur MAPI puisse se connecter à la Banque de messages.
    
7. MAPI renvoie l'interface **IMsgStore** au client. 
    
8. Le spouleur MAPI appelle [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider:: SpoolerLogon** renvoie les mêmes interfaces **IMSLogon** et **IMsgStore** à partir de l'étape 5. 
    
> [!NOTE]
> Si l'appel de connexion au fournisseur de banque de messages échoue car un mot de passe incorrect a été fourni et que le fournisseur de banque de messages ne peut pas afficher une interface pour demander le mot de passe correct, il doit renvoyer MAPI_E_FAILONEPROVIDER à partir de l' **IMSProvider:: Logon. **méthode. Cela permet aux clients d'inviter l'utilisateur à entrer un mot de passe pour essayer de se reconnecter au fournisseur de banque de messages au lieu de provoquer l'échec de MAPI pour l'ensemble de la session. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)


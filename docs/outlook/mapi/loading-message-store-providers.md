---
title: Chargement de fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398394"
---
# <a name="loading-message-store-providers"></a>Chargement de fournisseurs de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’une application cliente ouvre une banque de messages, MAPI charge DLL du fournisseur de banque de messages en mémoire. Une fois que MAPI charge la DLL, une séquence spécifique d’appels de méthode se produit entre le fournisseur de banque de messages et MAPI. Séquence d’appel de cette méthode permet de MAPI obtenir un niveau supérieur [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), et [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces et permet au fournisseur de banque de messages obtenir un objet de prise en charge MAPI. Après la séquence d’appel, le fournisseur de banque de message doit être prêt à accepter les connexions à partir de clients. 
  
La séquence d’appel lorsqu’un fournisseur de message que DLL est chargée est la suivante :
  
1. Le client appelle [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Si la banque de messages n’est pas déjà ouverte, MAPI charge la DLL du fournisseur de magasin et appelle le point d’entrée de la DLL [MSProviderInit](msproviderinit.md) . Si la banque de messages est déjà ouverte, MAPI ignore les étapes 2 et 3, puis utilise l’instruction [IMSProvider : IUnknown](imsprovideriunknown.md) interface à l’étape 4. 
    
3. **MSProviderInit** crée et renvoie un objet **IMSProvider** . 
    
4. Les appels MAPI [IMSProvider::Logon](imsprovider-logon.md), passant l’identificateur d’entrée de l’application cliente message store.
    
5. **IMSProvider::Logon** crée et renvoie une [IMSLogon : IUnknown](imslogoniunknown.md) interface et un [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) de l’interface et appelle ensuite la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) sur son [IMAPISupport : IUnknown](imapisupportiunknown.md) interface. Si le message du client stockage identificateur d’entrée fait référence à une banque de messages est déjà ouverte, le fournisseur de banque de message peut retourner des interfaces **IMSLogon** et **IMsgStore** existants n’a pas besoin d’appeler **AddRef** sur son objet prise en charge. 
    
6. Si le client n’a pas défini l’indicateur MAPI_NO_MAIL lorsqu’il ouvre une session et il n’a pas défini le MDB_NO_MAIL à l’étape 1, MAPI permettant d’identificateur d’entrée de la banque de messages le spouleur MAPI afin que le spouleur MAPI peut se connecter à la banque de messages.
    
7. MAPI renvoie l’interface **IMsgStore** au client. 
    
8. Le spouleur MAPI appelle [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** renvoie les mêmes interfaces **IMSLogon** et **IMsgStore** à l’étape 5. 
    
> [!NOTE]
> Si l’appel d’ouverture de session au message stocker fournisseur échoue, car un mot de passe incorrect a été fourni et le fournisseur de banque de message ne peut pas afficher une interface pour demander le mot de passe, il doit renvoyer la référence à MAPI_E_FAILONEPROVIDER à partir de la **IMSProvider::Logon **méthode. Cela permettra aux clients d’inviter l’utilisateur à un mot de passe pour essayer de se connecter au fournisseur de magasin de message à nouveau au lieu d’entraînant l’échec du fournisseur pour l’ensemble de la session MAPI. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)


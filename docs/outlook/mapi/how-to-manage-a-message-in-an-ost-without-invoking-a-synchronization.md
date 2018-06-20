---
title: Gérer les messages dans le fichier OST sans appeler une synchronisation en mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contient un exemple de code en langage C++ qui montre comment utiliser IID_IMessageRaw IMsgStore::OpenEntry pour obtenir une interface IMessage qui gère un message dans un fichier de dossiers en mode hors connexion (OST) sans forcer un téléchargement de la totalité du message lorsque le client est dans Exchange mis en cache Mode.
ms.openlocfilehash: e32bf4f64bfb91979133ee983e45481b3d5b9732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783494"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Gérer les messages dans le fichier OST sans appeler une synchronisation en mode Exchange mis en cache

**S’applique à**: Outlook 
  
Cette rubrique contient un exemple de code en langage C++ qui montre comment utiliser `IID_IMessageRaw` dans **[IMsgStore::OpenEntry](imsgstore-openentry.md)** pour obtenir une interface **[IMessage](imessageimapiprop.md)** qui gère un message dans un fichier de dossiers en mode hors connexion (OST) sans forcer un téléchargement de la totalité du message lorsque le client est en Mode Exchange mis en cache. 
  
Lorsqu’un client est en Mode Exchange mis en cache, les messages dans le fichier OST peuvent être l’un des deux états :
  
- Le message entier qui contient l’en-tête et le corps est téléchargé.
    
- Le message avec uniquement l’en-tête est téléchargé.
    
Lorsque vous demandez une interface **IMessage** pour un message dans un fichier OST et le client est en Mode Exchange mis en cache, utilisez `IID_IMessageRaw`. Si vous utilisez `IID_IMessage` pour demander une interface **IMessage** , et si le message comporte uniquement l’en-tête téléchargé dans le fichier OST, vous appelez une synchronisation qui tente de télécharger l’ensemble du message. 
  
Si vous utilisez `IID_IMessageRaw` ou `IID_IMessage` pour demander une interface **IMessage** , les interfaces qui sont retournés sont identiques en cours d’utilisation. L’interface **IMessage** qui a été demandé à l’aide de `IID_IMessageRaw` renvoie un message électronique telle qu’il existe dans le fichier OST, et la synchronisation n’est pas obligée. 
  
L’exemple suivant montre comment appeler la méthode **OpenEntry** , en passant `IID_IMessageRaw` au lieu de `IID_IMessage`.
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

Si la méthode **OpenEntry** renvoie le code d’erreur **MAPI_E_INTERFACE_NOT_SUPPORTED** , il indique que la banque de messages ne prend pas en charge le message en mode brut de l’accès à. Dans ce cas, essayez à nouveau la méthode **OpenEntry** en transmettant `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`pas peuvent être définis dans le fichier d’en-tête téléchargeable dont vous disposez. Dans ce cas, vous pouvez l’ajouter à votre code à l’aide de la définition suivante. Utilisez la macro DEFINE_OLEGUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows pour associer le nom symbolique GUID à sa valeur. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [Accès un magasin sur le Remote Server quand Outlook est en Mode Exchange mis en cache](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Ouvrir un objet Store sur le Remote Server quand Outlook est en Mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)


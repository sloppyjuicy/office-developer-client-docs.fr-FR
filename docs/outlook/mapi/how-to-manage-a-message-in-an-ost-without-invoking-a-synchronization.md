---
title: Gérer les messages dans OST sans l’voquer en mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contient un exemple de code en C++ qui montre comment utiliser IID_IMessageRaw dans IMsgStore::OpenEntry pour obtenir une interface IMessage qui gère un message dans un fichier de dossiers hors connexion (OST) sans forcer le téléchargement de l’intégralité du message lorsque le client est en mode Exchange mis en cache.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418756"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Gérer les messages dans OST sans l’voquer en mode Exchange mis en cache

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en C++ qui montre comment utiliser `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)** pour obtenir une interface **[IMessage](imessageimapiprop.md)** qui gère un message dans un fichier de dossiers hors connexion (OST) sans forcer le téléchargement de l’intégralité du message lorsque le client est en mode Exchange mis en cache. 
  
Lorsqu’un client est en mode Exchange mis en cache, les messages en mode OST peuvent être dans l’un des deux états :
  
- Le message entier qui contient l’en-tête et le corps est téléchargé.
    
- Le message avec uniquement son en-tête est téléchargé.
    
Lorsque vous demandez une interface **IMessage** pour un message dans un OST et que le client est en mode Exchange mis en cache, utilisez  `IID_IMessageRaw` . Si vous demandez une  `IID_IMessage` interface **IMessage** et que seul son en-tête est téléchargé dans le système OST, vous devez appeler une synchronisation qui tente de télécharger l’intégralité du message. 
  
Si vous utilisez  `IID_IMessageRaw` ou demandez une interface  `IID_IMessage` **IMessage,** les interfaces renvoyées sont en cours d’utilisation identiques. **L’interface IMessage** qui a été demandée à l’aide renvoie un message électronique tel qu’il existe dans le OST, et la `IID_IMessageRaw` synchronisation n’est pas forcée. 
  
L’exemple suivant montre comment appeler la **méthode OpenEntry,** en passant  `IID_IMessageRaw` au lieu de  `IID_IMessage` .
  
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

Si la **méthode OpenEntry** renvoie le code **d’MAPI_E_INTERFACE_NOT_SUPPORTED** de message, elle indique que la boutique de messages ne prend pas en charge l’accès au message en mode brut. Dans ce cas, essayez à nouveau **la méthode OpenEntry** en passant  `IID_IMessage` .

> [!IMPORTANT]
>  `IID_IMessageRaw` peut ne pas être défini dans le fichier d’en-tête téléchargeable dont vous disposez actuellement. Dans ce cas, vous pouvez l’ajouter à votre code à l’aide de la définition suivante. Utilisez la macro DEFINE_OLEGUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer le nom symbolique GUID à sa valeur. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)


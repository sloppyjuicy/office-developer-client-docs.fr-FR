---
title: Accéder à une boutique sur le serveur distant lorsque Outlook est en mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 6fb76abf0b4c03f8c7114907ef9a3754c240d971
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556643"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Accéder à une boutique sur le serveur distant lorsque Outlook est en mode Exchange mis en cache
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en C++ qui montre comment utiliser l’indicateur **MAPI_NO_CACHE** pour ouvrir un dossier ou un message dans une magasin de messages sur le serveur distant lorsque Microsoft Office Outlook est en mode Exchange mis en cache. 
  
Le mode Exchange mis en cache permet à Outlook d’utiliser une copie locale de la boîte aux lettres d’un utilisateur tandis que Outlook maintient une connexion en ligne à une copie distante de la boîte aux lettres de l’utilisateur sur le serveur Exchange distant. Lorsque Outlook est en cours d’exécution en mode Exchange mis en cache, par défaut, toutes les solutions MAPI qui se connectent à la même session sont également connectées à la magasin de messages mis en cache. Toutes les données accessibles et les modifications apportées sont apportées à la copie locale de la boîte aux lettres.
  
Un client ou un fournisseur de services peut remplacer la connexion à la magasin de messages locale et ouvrir un message ou un dossier sur la boutique distante en paramétrez le bit pour **MAPI_NO_CACHE** dans le paramètre  *ulFlags*  lors de l’appel de **[IMsgStore::OpenEntry](imsgstore-openentry.md)**. 
  
L’exemple de code suivant montre comment appeler **IMsgStore::OpenEntry** avec l’indicateur **MAPI_NO_CACHE** définie dans le paramètre  *ulFlags*  pour ouvrir le dossier racine dans la boutique de messages distante. 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

Si vous avez ouvert la magasin de messages avec **l’indicateur MDB_ONLINE** sur le serveur distant, vous n’avez pas besoin d’utiliser **l’MAPI_NO_CACHE** de messagerie. 
  
## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)


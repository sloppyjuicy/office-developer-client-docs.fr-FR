---
title: Accéder à un magasin sur le serveur distant lorsque Outlook est en Mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: c7994366000e323cc7d14a9c3a02b5229c5f08e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573312"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Accéder à un magasin sur le serveur distant lorsque Outlook est en Mode Exchange mis en cache
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en langage C++ qui montre comment utiliser l’indicateur **MAPI_NO_CACHE** pour ouvrir un dossier ou un message dans une banque de messages sur le serveur distant lorsque Microsoft Office Outlook est en Mode Exchange mis en cache. 
  
Le Mode Exchange mis en cache permet à Outlook pour utiliser une copie locale de boîte aux lettres d’un utilisateur pendant que Outlook conserve une connexion en ligne à une copie distante de boîte aux lettres de l’utilisateur sur le serveur Exchange distant. Lorsque Outlook s’exécute en Mode Exchange mis en cache, par défaut, les solutions MAPI qui se connectent à la même session sont également connectées à la banque de messages mis en cache. Toutes les données accessibles et les modifications apportées sont effectuées sur la copie locale de la boîte aux lettres.
  
Un client ou fournisseur de services peut remplacer la connexion à la banque de messages local et ouvrir un message ou un dossier sur le magasin distant en définissant le bit pour **MAPI_NO_CACHE** dans le paramètre *ulFlags* lors de l’appel **[IMsgStore::OpenEntry](imsgstore-openentry.md)**. 
  
L’exemple de code suivant montre comment appeler **IMsgStore::OpenEntry** avec l’indicateur **MAPI_NO_CACHE** dans le paramètre *ulFlags* pour ouvrir le dossier racine de la banque de messages à distance. 
  
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

Si vous avez ouvert la banque de messages avec l’indicateur **MDB_ONLINE** sur le serveur distant, vous n’avez pas d’utiliser l’indicateur **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)


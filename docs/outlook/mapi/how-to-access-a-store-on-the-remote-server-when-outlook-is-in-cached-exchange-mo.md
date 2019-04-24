---
title: Accéder à une banque sur le serveur distant lorsqu'Outlook est en mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Dernière modification le: 02 juillet 2012'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299439"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Accéder à une banque sur le serveur distant lorsqu'Outlook est en mode Exchange mis en cache
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en C++ qui montre comment utiliser l'indicateur **MAPI_NO_CACHE** pour ouvrir un dossier ou un message dans une banque de messages sur le serveur distant lorsque Microsoft Office Outlook est en mode Exchange mis en cache. 
  
Le mode Exchange mis en cache permet à Outlook d'utiliser une copie locale de la boîte aux lettres d'un utilisateur pendant qu'Outlook maintient une connexion en ligne à une copie distante de la boîte aux lettres de l'utilisateur sur le serveur Exchange distant. Lorsqu'Outlook est exécuté en mode Exchange mis en cache, par défaut, toutes les solutions MAPI qui se connectent à la même session sont également connectées à la Banque de messages mise en cache. Toutes les données auxquelles un accès est effectué et toutes les modifications apportées sont effectuées par rapport à la copie locale de la boîte aux lettres.
  
Un client ou un fournisseur de services peut remplacer la connexion à la Banque de messages locale et ouvrir un message ou un dossier dans le magasin distant en définissant le bit pour **MAPI_NO_CACHE** dans le paramètre *ulFlags* lors de l'appel de **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**. 
  
L'exemple de code suivant montre comment appeler **IMsgStore:: OpenEntry** avec l'indicateur **MAPI_NO_CACHE** défini dans le paramètre *ulFlags* pour ouvrir le dossier racine sur le magasin de messages distant. 
  
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

Si vous avez ouvert la Banque de messages avec l'indicateur **MDB_ONLINE** sur le serveur distant, il n'est pas nécessaire d'utiliser l'indicateur **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)


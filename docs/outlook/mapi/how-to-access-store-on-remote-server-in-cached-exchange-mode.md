---
title: Accéder à un magasin sur le serveur distant quand Outlook est en mode Exchange mis en cache
description: Cet article explique comment accéder à un magasin sur le serveur distant quand Outlook est en mode cache Exchange.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
ms.openlocfilehash: 9dac2abd4f6b17a73ec802bc730e9fa1136d455d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817507"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Accéder à un magasin sur le serveur distant quand Outlook est en mode Exchange mis en cache
 
**S’applique à** : Outlook 2013 | Outlook 2016
  
Cette rubrique contient un exemple de code en C++ qui montre comment utiliser l’indicateur **MAPI_NO_CACHE** pour ouvrir un dossier ou un message sur un magasin de messages sur le serveur distant lorsque Microsoft Office Outlook est en mode mis en cache Exchange.
  
Le mode Exchange mis en cache permet aux Outlook d’utiliser une copie locale de la boîte aux lettres d’un utilisateur, tandis que Outlook conserve une connexion en ligne à une copie à distance de la boîte aux lettres de l’utilisateur sur le serveur Exchange distant. Lorsque Outlook s’exécute en mode Exchange mis en cache, par défaut, toutes les solutions MAPI qui se connectent à la même session sont également connectées au magasin de messages mis en cache. Toutes les données accessibles et toutes les modifications apportées sont apportées à la copie locale de la boîte aux lettres.
  
Un client ou un fournisseur de services peut remplacer la connexion au magasin de messages local et ouvrir un message ou un dossier sur le magasin distant en définissant le bit pour **MAPI_NO_CACHE** dans le paramètre *ulFlags* lors de l’appel d’IMsgStore **[::OpenEntry](imsgstore-openentry.md)**.
  
L’exemple de code suivant montre comment appeler **IMsgStore::OpenEntry** avec l’indicateur **MAPI_NO_CACHE** défini dans le paramètre *ulFlags* pour ouvrir le dossier racine sur le magasin de messages distant.
  
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

Si vous avez ouvert le magasin de messages avec l’indicateur **MDB_ONLINE** sur le serveur distant, vous n’avez pas à utiliser l’indicateur **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md)
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

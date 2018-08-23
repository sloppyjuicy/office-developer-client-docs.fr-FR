---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a40046a26efe118e48cdca4749d2e99212bb8bfe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579840"
---
# <a name="sync"></a>SYNC

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations de démarrage de la synchronisation entre un magasin local et un serveur. Ces informations sont utilisées lors de l' [état de synchronisation](synchronize-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a>Members

 _ulFlags_
  
- [out] / [in] un masque de bits des indicateurs suivants qui modifie le comportement lors de la synchronisation :
    
- UPS_UPLOAD_ONLY
    
  - [in] Le client effectueront téléchargement uniquement. Outlook ne renvoie que les dossiers modifiés localement.
    
- UPS_DNLOAD_ONLY
    
  - [in] Le client effectueront téléchargement uniquement. Outlook ne doit pas effacer les bits de téléchargement des dossiers.
    
- UPS_THESE_FOLDERS
    
  - [in] Le client sera synchroniser un ensemble spécifié de dossiers avec l’identificateur d’entrée fourni. Cet indicateur peut être combiné avec indicateur le **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** . 
    
- UPS_OK
    
  - [out] La synchronisation a réussi. Le client définit ce après avoir téléchargé ou une synchronisation complète est terminée.
    
- 
    
    > [!NOTE]
    > Même si le client peut télécharger ou synchroniser entièrement (télécharger, puis téléchargez) des dossiers et des éléments avec l’API de réplication, le client spécifie *ulFlags* avec uniquement un sens de la réplication à la fois, **UPS_UPLOAD_ONLY** ou Indicateur **UPS_DNLOAD_ONLY** . Dans le cas d’une synchronisation complète, le client effectue tout d’abord un téléchargement avec l’indicateur **UPS_UPLOAD_ONLY** , puis un téléchargement avec l’indicateur **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- [out] Chemin d’accès dans le magasin local.
    
 _Reserved1_
  
- Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 _Reserved2_
  
- Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 *PEL* 
  
- [in] Il s’agit de la liste des identificateurs d’entrée de dossiers à synchroniser si **UPS_THESE_FOLDERS** a été définie. Voir mapidefs.h pour la définition du type de **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- [in] Il s’agit d’un tableau des options de dossier pour les dossiers correspondants dans *pel* si **UPS_THESE_FOLDERS** a été définie. Ces options de dossier sont utilisées lors du téléchargement de chacun des dossiers répertoriés dans *pel* au cours de l' [état du dossier de téléchargement](upload-folder-state.md). Pour plus d’informations sur les options du dossier, voir **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)


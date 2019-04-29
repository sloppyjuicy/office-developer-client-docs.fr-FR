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
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433807"
---
# <a name="sync"></a>SYNC

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le démarrage de la synchronisation entre un magasin local et un serveur. Ces informations sont utilisées lors de l' [État Synchronize](synchronize-state.md).
  
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

## <a name="members"></a>Membres

 _ulFlags_
  
- [out]/[in] masque de masque des indicateurs suivants qui modifie le comportement lors de la synchronisation:
    
- UPS_UPLOAD_ONLY
    
  - dans Le client effectuera uniquement le chargement. Outlook retourne uniquement les dossiers modifiés localement.
    
- UPS_DNLOAD_ONLY
    
  - dans Le client effectue uniquement un téléchargement. Outlook ne doit pas effacer les bits de téléchargement pour les dossiers.
    
- UPS_THESE_FOLDERS
    
  - dans Le client synchronise un ensemble spécifié de dossiers avec les ID d'entrée fournis. Cet indicateur peut être combiné avec l'indicateur **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** . 
    
- UPS_OK
    
  - remarquer La synchronisation a réussi. Le client définit ceci après le téléchargement ou une synchronisation complète.
    
- 
    
    > [!NOTE]
    > Même si le client peut télécharger des dossiers et des éléments avec l'API de réPlication ou les synchroniser entièrement (télécharger et télécharger), le client spécifie *ulFlags* avec une seule direction de la réplication à la fois, à savoir le **UPS_UPLOAD_ONLY** ou Indicateur **UPS_DNLOAD_ONLY** . Dans le cas d'une synchronisation complète, le client effectue d'abord un chargement avec l'indicateur **UPS_UPLOAD_ONLY** , puis un téléchargement avec l'indicateur **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- remarquer Chemin d'accès au magasin local.
    
 _Reserved1_
  
- Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.
    
 _Reserved2_
  
- Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.
    
 *PEL* 
  
- dans Il s'agit de la liste des identificateurs d'entrée des dossiers à synchroniser si **UPS_THESE_FOLDERS** a été défini. Voir mapidefs. h pour la définition de type de **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- dans Il s'agit d'un tableau d'options de dossier pour les dossiers correspondants dans *PEL* si **UPS_THESE_FOLDERS** a été défini. Ces options de dossiers sont utilisées lors du téléchargement de chaque dossier répertorié dans *PEL* lors de l' [État du dossier de chargement](upload-folder-state.md). Pour plus d'informations sur les options des dossiers, voir **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)


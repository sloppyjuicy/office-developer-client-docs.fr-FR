---
title: SYNC
manager: lindalu
ms.date: 02/22/2022
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: Informations de démarrage de la synchronisation entre un magasin local et un serveur.
ms.openlocfilehash: 905cbbf7c15eca0454548b161efdb87c8b7ba814
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374669"
---
# <a name="sync"></a>SYNC

**S’applique à** : Outlook 2013 | Outlook 2016
  
Informations de démarrage de la synchronisation entre un magasin local et un serveur. Ces informations sont utilisées pendant [l’état de synchronisation](synchronize-state.md).
  
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
  
- [out]/[in] Masque de bits des indicateurs suivants qui modifie le comportement lors de la synchronisation :

- UPS_UPLOAD_ONLY

  - [in] Le client effectue uniquement le chargement. Outlook renvoie uniquement les dossiers modifiés localement.

- UPS_DNLOAD_ONLY

  - [in] Le client effectue uniquement le téléchargement. Outlook ne doit pas effacer les bits de chargement des dossiers.

- UPS_THESE_FOLDERS

  - [in] Le client synchronisera un ensemble spécifié de dossiers avec les ID d’entrée fournis. Cet indicateur peut être combiné avec **l’UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY’indicateur** .

- UPS_OK

  - [out] La synchronisation a réussi. Le client définit cela une fois le téléchargement ou une synchronisation complète terminée.

      > [!NOTE]
      > Même si le client peut charger ou synchroniser entièrement (télécharger puis télécharger) des dossiers et des éléments avec l’API de réplication, le client spécifie les *ulFlags* avec un seul sens de la réplication à la fois ( l’indicateur **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** ). Dans le cas d’une synchronisation complète, le client fait d’abord un chargement avec l’indicateur **UPS_UPLOAD_ONLY** , puis un téléchargement avec **l’UPS_DNLOAD_ONLY’indicateur** . 
  
 _pwzPath_
  
- [out] Chemin d’accès au magasin local.

 _Reserved1_
  
- Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.

 _Reserved2_
  
- Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.

 _pel_
  
- [in] Il s’agit de la liste des ID d’entrée des dossiers à synchroniser si **UPS_THESE_FOLDERS** a été définie. Voir mapidefs.h pour la définition de type **de LPENTRYLIST**.

 _ErrsFolderOptions_
  
- [in] Il s’agit d’un tableau d’options de dossier pour les dossiers correspondants dans _pel_ **si UPS_THESE_FOLDERS** a été définie. Ces options de dossier sont utilisées lors du téléchargement de chacun des dossiers répertoriés dans *pel* pendant [l’état de chargement du dossier](upload-folder-state.md). Pour plus d’informations sur les options de dossier, **[voir UPFLD](upfld.md)**.

## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)  
[Constantes MAPI](mapi-constants.md)

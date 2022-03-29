---
title: Télécharger table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: Cette rubrique décrit ce qui se produit pendant l’état de la table de chargement de la machine à états de réplication.
ms.openlocfilehash: 6cd90a5cdda9c6840192ab8a9faec6ef4ef962ef
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454669"
---
# <a name="upload-table-state"></a>Télécharger table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de la table de chargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Structure de données associée :  <br/> |**[UPTBL](uptbl.md)** <br/> |
|À partir de cet état :  <br/> |[Synchroniser l’état du contenu](synchronize-contents-state.md) <br/> |
|À cet état :  <br/> |[Télécharger’état du message](upload-message-state.md), [télécharger l’état](upload-delete-status-state.md) de suppression d’état, télécharger l’état [de](upload-read-status-state.md) lecture ou synchroniser l’état du contenu  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement du contenu d’un dossier qui a été spécifié dans un état de synchronisation de contenu précédent. Le dossier peut être un dossier de courrier, de calendrier, de contacts, de tâches, de notes ou de journal. Au cours de cet état, Outlook crée une liste d’éléments qui ont été ajoutés, modifiés, déplacés, supprimés ou marqués comme lus, et prépare les informations internes appropriées pour l’état du message de chargement correspondant, l’état de suppression de téléchargement ou l’état de lecture.
  
Lorsque cet état se termine, Outlook le dossier comme ayant son contenu synchronisé, afin que le contenu ne soit pas chargé à nouveau jusqu’à ce qu’une autre modification soit apportée. La boutique locale revient à l’état de synchronisation du contenu.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


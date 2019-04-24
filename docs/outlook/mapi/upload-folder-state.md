---
title: Télécharger l'état du dossier
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348425"
---
# <a name="upload-folder-state"></a>Télécharger l'état du dossier

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état du dossier de chargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Structure de données associée:  <br/> |**[UPFLD](upfld.md)** <br/> |
|À partir de cet État:  <br/> |[Charger l'état de la hiérarchie](upload-hierarchy-state.md) <br/> |
|À cet État:  <br/> |Charger l'état de la hiérarchie  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement d'un dossier dans une hiérarchie qui a été spécifiée dans un état de hiérarchie de téléchargement précédent. Dans cet État, Outlook fournit l'objet Folder (s'il n'a pas été supprimé) et les indicateurs indiquant l'état du dossier (nouveau, déplacé, modifié ou supprimé) dans le cadre de la structure de données **UPFLD** correspondante. Le client télécharge ensuite ces informations sur le serveur. 
  
Si le chargement réussit, le client définit *ulFlags* dans **UPFLD** sur **UPF_OK**. Outlook efface ensuite ses informations internes sur la demande de téléchargement du dossier. 
  
Une fois le téléchargement du dossier terminé, le magasin local revient à l'état de la hiérarchie de téléchargement. En fonction de **[](uphier.md)** la structure de la mise à niveau automatique correspondant à l'état de la hiérarchie de téléchargement précédente, Outlook détermine s'il faut continuer à télécharger le dossier suivant et à préparer l'état du dossier de chargement suivant. 
  
> [!NOTE]
> Si le client a besoin de télécharger un seul dossier, le client peut lancer la réplication via l' [État Synchronize](synchronize-state.md) sans entrer l'état de la hiérarchie de chargement. Le client définit certains membres de la **[synchronisation](sync.md)** ( *ulFlags* à **UPS_UPLOAD_ONLY** et **UPS_ONE_FOLDER** et *FEID* à l'ID du dossier) pour indiquer à Outlook qu'un seul dossier sera chargé. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


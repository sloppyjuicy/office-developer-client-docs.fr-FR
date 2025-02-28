---
title: Télécharger dossier
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: Cette rubrique décrit ce qui se produit pendant l’état du dossier de chargement de la machine à états de réplication.
ms.openlocfilehash: dbee437b1e3e8b1e32684355c72c76f10d2bb2ce
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456209"
---
# <a name="upload-folder-state"></a>Télécharger dossier

**S’applique à** : Outlook 2013 | Outlook 2016
  
 Cette rubrique décrit ce qui se produit pendant l’état du dossier de chargement de la machine à états de réplication.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Structure de données associée :  <br/> |**[UPFLD](upfld.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger hiérarchie](upload-hierarchy-state.md) <br/> |
|À cet état :  <br/> |Télécharger hiérarchie  <br/> |

> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un dossier dans une hiérarchie qui a été spécifiée dans un état de hiérarchie de téléchargement précédent. Pendant cet état, Outlook fournit l’objet dossier (s’il n’a pas été supprimé) et les indicateurs indiquant l’état du dossier (nouveau, déplacé, modifié ou supprimé) dans le cadre de la structure de données **UPFLD** correspondante. Le client charge ensuite ces informations sur le serveur.
  
Si le chargement réussit, le client définit *ulFlags* dans **UPFLD** sur **UPF_OK**. Outlook effacer ensuite ses informations internes sur la demande de téléchargement du dossier.
  
Lorsque le chargement du dossier se termine, la boutique locale revient à l’état de hiérarchie de chargement. En fonction de la structure **[UPHIER](uphier.md)** correspondant à l’état de hiérarchie de chargement précédent, Outlook détermine s’il faut poursuivre le chargement du dossier suivant et préparer l’état du dossier de chargement suivant.
  
> [!NOTE]
> Si le client n’a besoin de télécharger qu’un seul dossier, il peut lancer [](synchronize-state.md) la réplication via l’état de synchronisation sans passer par l’état de hiérarchie de téléchargement. Le client définit certains membres de **[SYNC](sync.md)** (*ulFlags* sur **UPS_UPLOAD_ONLY** et **UPS_ONE_FOLDER** et sur l’ID du dossier) pour indiquer à Outlook qu’un seul dossier sera téléchargé.
  
## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)  
[Constantes MAPI](mapi-constants.md)  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)  
[SYNCSTATE](syncstate.md)

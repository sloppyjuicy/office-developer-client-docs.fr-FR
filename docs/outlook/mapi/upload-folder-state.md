---
title: État du dossier de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787420"
---
# <a name="upload-folder-state"></a>État du dossier de téléchargement

  
  
**S’applique à**: Outlook 
  
 Cette rubrique décrit le déroulement de l’état du dossier de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Structure de données associées :  <br/> |**[UPFLD](upfld.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger l’état de la hiérarchie](upload-hierarchy-state.md) <br/> |
|Avec cet état :  <br/> |Télécharger l’état de la hiérarchie  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un dossier dans une hiérarchie a été spécifié dans un état de hiérarchie de téléchargement précédent. Au cours de cet état, Outlook fournit l’objet folder (si elle n’a pas été supprimée) et les indicateurs indiquant l’état du dossier (nouveau, déplacé, modifié ou supprimé) dans le cadre de la structure de données **UPFLD** correspondante. Le client télécharge ensuite ces informations vers le serveur. 
  
Si le transfert se déroule correctement, le client définit *ulFlags* dans **UPFLD** à **UPF_OK**. Ses informations internes sur la demande pour télécharger le dossier Outlook puis l’efface. 
  
Lorsque le téléchargement du dossier se termine, la banque locale renvoie l’état de la hiérarchie de téléchargement. En fonction de la structure **[UPHIER](uphier.md)** correspondant à l’état de hiérarchie de téléchargement ci-dessus, Outlook détermine s’il afin de passer à télécharger le dossier suivant et en vue de l’état du dossier de téléchargement suivant. 
  
> [!NOTE]
> Si le client doit ne télécharger qu’un seul dossier, le client peut lancer la réplication par le biais de l' [état de synchronisation](synchronize-state.md) sans saisir l’état de la hiérarchie de téléchargement. Le client définit certains membres de **[synchronisation](sync.md)** : *ulFlags* **UPS_UPLOAD_ONLY** **UPS_ONE_FOLDER** et *feid* à l’ID du dossier — pour indiquer à ce qu’un seul dossier Outlook sera téléchargé. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


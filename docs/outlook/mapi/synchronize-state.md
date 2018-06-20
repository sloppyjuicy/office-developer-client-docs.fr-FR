---
title: État de synchronisation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787321"
---
# <a name="synchronize-state"></a>État de synchronisation

  
  
**S’applique à**: Outlook 
  
 Cette rubrique décrit le déroulement de l’état de synchronisation de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC** <br/> |
|Structure de données associées :  <br/> |**[SYNCHRONISATION](sync.md)** <br/> |
|À partir de cet état :  <br/> |[État inactif](idle-state.md) <br/> |
|Avec cet état :  <br/> |[État de la hiérarchie du téléchargement](download-hierarchy-state.md), [synchroniser le contenu d’un état](synchronize-contents-state.md), [Téléchargez l’état de la hiérarchie](upload-hierarchy-state.md)ou inactif  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance la synchronisation. Un magasin local peut passer à un téléchargement ou d’un état de téléchargement à partir d’ici. Par exemple, un magasin local peut passer à l’état de hiérarchie de téléchargement pour télécharger une hiérarchie de dossiers sur le serveur, ou elle peut effectuer une synchronisation complète en premier téléchargement de la hiérarchie, puis la hiérarchie à partir du serveur.
  
Au cours de cet état, Outlook initialise la structure de données de **synchronisation** associée avec le chemin d’accès dans le magasin local, afin qu’Outlook voit les modifications au cours des autres États. 
  
Le client définit le [in] les membres de la **synchronisation**, ce qui indique comment gérer les autres États à Outlook. Par exemple, le client peut définir *ulFlags* **UPS_UPLOAD_ONLY** et **UPS_THESE_FOLDERS** et *pel* à une liste d’identificateurs d’entrée des dossiers pour indiquer à Outlook que seuls ces dossiers sera téléchargé. Lorsque cet état se termine, la banque locale revient à l’état est inactif. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


---
title: Synchroniser l'État
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349510"
---
# <a name="synchronize-state"></a>Synchroniser l'État

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de synchronisation de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC** <br/> |
|Structure de données associée:  <br/> |**[SYNCHRONI](sync.md)** <br/> |
|À partir de cet État:  <br/> |[État inactif](idle-state.md) <br/> |
|À cet État:  <br/> |[Télécharger](download-hierarchy-state.md)l'état de la hiérarchie, synchroniser l'état du [contenu](synchronize-contents-state.md), [charger l'État](upload-hierarchy-state.md)de la hiérarchie ou état inactif  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance la synchronisation. Un magasin local peut effectuer une transition vers un état de téléchargement ou de téléchargement à partir de cet emplacement. Par exemple, un magasin local peut être déplacé vers l'état de la hiérarchie de téléchargement pour charger une hiérarchie de dossiers sur le serveur, ou il peut effectuer une synchronisation complète en téléchargeant d'abord la hiérarchie, puis en téléchargeant la hiérarchie à partir du serveur.
  
Dans cet État, Outlook initialise la structure de données de **synchronisation** associée avec le chemin d'accès au magasin local, afin qu'Outlook détecte les modifications dans les autres États. 
  
Le client définit les membres [in] de la **synchronisation**, ce qui indique à Outlook comment gérer d'autres États. Par exemple, le client peut définir *ulFlags* sur **UPS_UPLOAD_ONLY** et **UPS_THESE_FOLDERS** et *PEL* sur une liste d'identificateurs d'entrée des dossiers pour indiquer à Outlook que seuls ces dossiers seront chargés. Lorsque cet État se termine, le magasin local revient à l'état inactif. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


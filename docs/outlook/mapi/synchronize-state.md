---
title: Synchroniser l’état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: Cette rubrique décrit ce qui se produit pendant l’état de synchronisation de la machine à états de réplication.
ms.openlocfilehash: a706edfe7fd4c63e368faefd227da038b30acc31
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782215"
---
# <a name="synchronize-state"></a>Synchroniser l’état

**S’applique à** : Outlook 2013 | Outlook 2016
  
 Cette rubrique décrit ce qui se produit pendant l’état de synchronisation de la machine à états de réplication.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC** <br/> |
|Structure de données associée :  <br/> |**[SYNC](sync.md)** <br/> |
|À partir de cet état :  <br/> |[État inactif](idle-state.md) <br/> |
|À cet état :  <br/> |[Télécharger l’état de la hiérarchie](download-hierarchy-state.md), [synchroniser l’état du contenu](synchronize-contents-state.md), télécharger [l’état de la](upload-hierarchy-state.md) hiérarchie ou l’état inactif  <br/> |

> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.
  
## <a name="description"></a>Description

Cet état lance la synchronisation. Un magasin local peut passer à un état de chargement ou de téléchargement à partir d’ici. Par exemple, un magasin local peut passer à l’état de hiérarchie de téléchargement pour télécharger une hiérarchie de dossiers sur le serveur, ou il peut effectuer une synchronisation complète en téléchargeant d’abord la hiérarchie, puis en téléchargeant la hiérarchie à partir du serveur.
  
Au cours de cet état, Outlook initialise la structure de données **SYNC** associée avec le chemin d’accès au magasin local, afin que Outlook les modifications pendant d’autres états.
  
Le client définit les membres [in] de **SYNC**, ce qui Outlook comment gérer d’autres états. Par exemple, le client peut définir *ulFlags* sur **UPS_UPLOAD_ONLY** et **UPS_THESE_FOLDERS** et *pel* à une liste d’identificateurs d’entrée des dossiers pour indiquer à Outlook que seuls ces dossiers seront téléchargés. Lorsque cet état se termine, le magasin local revient à l’état inactif.
  
## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)  
[Constantes MAPI](mapi-constants.md)  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)  
[SYNCSTATE](syncstate.md)

---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431994"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des méthodes de synchronisation. Cette interface récupère les informations nécessaires pour répliquer les modifications locales sur le serveur et les modifications apportées au serveur dans le magasin local.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificateur de l'interface:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](iostx-getlasterror.md) <br/> |Obtient des informations étendues sur la dernière erreur.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informe le magasin local que la synchronisation est sur le du début.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prépare le magasin local à la synchronisation dans un état particulier et récupère les informations nécessaires à répliquer.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Termine la synchronisation à l'état actuel et quitte cet État.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Démarre la synchronisation pour un en-tête de message.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Met fin à la synchronisation pour un en-tête de message.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Définit le résultat de la synchronisation.  <br/> |
| *Membre de l'espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu'un client charge ou synchronise des dossiers et du contenu de dossier sur un magasin local, il déplace le magasin local d'un État à un autre, comme illustré dans le diagramme de transition d'État dans [about the Replication State Machine](about-the-replication-state-machine.md). Voici l'ordre des événements pour que le client déplace le magasin local d'un État à l'autre:
  
1. Le client appelle **IOSTX:: InitSync** pour informer le magasin local que la réplication est sur le le début. 
    
2. En fonction de la direction de la réplication et des objets à répliquer, le client appelle **IOSTX:: SyncBeg** pour commencer la réplication dans l'état approprié. Outlook fournit au client les informations nécessaires et le client effectue la réplication. 
    
3. Le client appelle **IOSTX:: SetSyncResult** pour renvoyer le résultat de la réplication. 
    
4. Le client appelle **IOSTX:: SyncEnd,** pour mettre fin à la réplication, fournissant ainsi à Outlook les informations nécessaires à la réplication suivante. 
    
En particulier, lorsque vous téléchargez des éléments de message, le client utilise **IOSTX:: SyncHdrBeg** et **IOSTX:: SyncHdrEnd** pour mettre à jour un élément de message complet avec l'en-tête de message sur le magasin local: 
  
1. Sur **IOSTX:: SyncHdrBeg**, le magasin local passe à l'état d'en-tête du message de téléchargement. Outlook fournit à l'origine le client avec l'en-tête de message actuel sur le magasin local.
    
2. Le client télécharge un élément de message complet avec l'en-tête du message.
    
3. Outlook met à jour l'élément sur le magasin local avec l'élément de message complet.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)


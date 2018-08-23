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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9c9252e83ce212bacf185d0eedb75d30617f9807
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581747"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit des méthodes de synchronisation. Cette interface récupère les informations nécessaires pour répliquer les modifications locales vers le serveur et les modifications de serveur dans le magasin local.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificateur de l’interface :  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Obtient des informations sur la dernière erreur étendues.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Indique le magasin local que la synchronisation est prêt à démarrer.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prépare le magasin local de la synchronisation dans un état particulier et récupère les informations nécessaires pour répliquer.  <br/> |
|[Processus](iostx-syncend.md) <br/> |Met fin à la synchronisation dans l’état actuel et quitte cet état.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Démarre la synchronisation pour un en-tête de message.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Fin de la synchronisation pour un en-tête de message.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Définit le résultat de la synchronisation.  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un client télécharge ou synchronise les dossiers et le contenu du dossier sur un magasin local, il déplace le magasin local d’un état à l’autre comme illustré dans le diagramme de transition d’état de [L’ordinateur d’état de réplication](about-the-replication-state-machine.md). Voici l’ordre des événements pour le client déplacer le magasin local d’un état à un autre :
  
1. Le client appelle **IOSTX::InitSync** pour informer le magasin local que la réplication est prêt à démarrer. 
    
2. En fonction de la direction de la réplication et les objets à répliquer, le client appelle **IOSTX::SyncBeg** pour commencer la réplication dans l’état approprié. Outlook fournit au client les informations nécessaires, et le client effectue la réplication. 
    
3. Le client appelle **IOSTX::SetSyncResult** pour renvoyer le résultat de la réplication. 
    
4. Le client appelle **IOSTX::SyncEnd** pour mettre fin à la réplication, fournissant Outlook les informations nécessaires pour la réplication suivante. 
    
En particulier, lors du téléchargement des éléments de message, le client utilise **IOSTX::SyncHdrBeg** et **IOSTX::SyncHdrEnd** pour mettre à jour un élément de message complète avec l’en-tête du message dans la banque locale : 
  
1. Fonction **IOSTX::SyncHdrBeg**, local stocker les transitions dans l’état d’en-tête de message téléchargement. Outlook fournit à l’origine du client avec l’en-tête du message en cours dans le magasin local.
    
2. Le client télécharge un élément de message complet ainsi que l’en-tête du message.
    
3. Outlook met à jour l’élément dans le magasin local avec l’élément de message complet.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)


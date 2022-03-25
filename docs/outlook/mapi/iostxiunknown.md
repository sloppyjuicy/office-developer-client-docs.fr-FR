---
title: IOSTX  IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: Fournit des méthodes de synchronisation. Cette interface récupère les informations nécessaires pour répliquer les modifications locales apportées au serveur et au magasin local.
ms.openlocfilehash: 70be66ceff9f405af0c674b4d42d7054c143bd29
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405502"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des méthodes de synchronisation. Cette interface récupère les informations nécessaires pour répliquer les modifications locales apportées au serveur et au magasin local.
  
|Propriété |Valeur |
|:-----|:-----|
|Fourni par :  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificateur d’interface :  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Propriété |Valeur |
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Obtient des informations étendues sur la dernière erreur. |
|[InitSync](iostx-initsync.md) <br/> |Informe le magasin local que la synchronisation est sur le point de démarrer. |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prépare le magasin local pour la synchronisation dans un état particulier et récupère les informations nécessaires à répliquer. |
|[SyncEnd](iostx-syncend.md) <br/> |Met fin à la synchronisation dans l’état actuel et quitte cet état. |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Démarre la synchronisation pour un en-tête de message. |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Met fin à la synchronisation d’un en-tête de message. |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Définit le résultat de la synchronisation. |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un client télécharge ou synchronise les dossiers et le contenu d’un dossier sur un magasin local, il déplace la boutique locale d’un état à un autre, comme décrit dans le diagramme de transition d’état dans À propos de la machine à états de [réplication](about-the-replication-state-machine.md). Voici l’ordre des événements pour que le client déplace le magasin local d’un état à un autre :
  
1. Le client appelle **IOSTX::InitSync** pour informer le magasin local que la réplication est sur le point de démarrer. 
    
2. Selon la direction de la réplication et les objets à répliquer, le client appelle **IOSTX::SyncBeg** pour commencer la réplication dans l’état approprié. Outlook fournit au client les informations nécessaires et le client effectue la réplication. 
    
3. Le client appelle **IOSTX::SetSyncResult** pour renvoyer le résultat de la réplication. 
    
4. Le client appelle **IOSTX::SyncEnd** pour mettre fin à la réplication, Outlook les informations nécessaires pour la réplication ultérieure. 
    
En particulier, lors du téléchargement des éléments de message, le client utilise **IOSTX::SyncHdrBeg** et **IOSTX::SyncHdrEnd** pour mettre à jour un élément de message complet avec l’en-tête du message dans la boutique locale : 
  
1. Sur **IOSTX::SyncHdrBeg**, le magasin local passe à l’état d’en-tête du message de téléchargement. Outlook fournit initialement au client l’en-tête de message actuel dans la boutique locale.
    
2. Le client télécharge un élément de message complet avec l’en-tête du message.
    
3. Outlook met à jour l’élément dans la boutique locale avec l’élément de message complet.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)


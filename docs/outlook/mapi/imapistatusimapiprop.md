---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a63b6cb77f4bcbd4919016630c09699ddf961f60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584394"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations d’état sur le sous-système MAPI, le carnet d’adresses intégré et lepooler MAPI. Un fournisseur de services implémente **IMAPIStatus** pour fournir des informations sur son propre état. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de statut  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIStatus  <br/> |
|Type de pointeur :  <br/> |LPMAPISTATUS  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Confirme les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de services.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifie le mot de passe d’un fournisseur de services sans afficher d’interface utilisateur.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Force le téléchargement immédiat de tous les messages en attente d’envoi ou de réception.  <br/> |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Les objets d’état implémentés par MAPI supportent les méthodes suivantes :
  
|**Objet Status**|**Méthodes prise en charge**|
|:-----|:-----|
|Sous-système MAPI  <br/> |**ValidateState** uniquement  <br/> |
|Carnet d’adresses MAPI  <br/> |**ValidateState** uniquement  <br/> |
|Pooler MAPI  <br/> |**ValidateState** et **FlushQueues** <br/> |
   
Les objets d’état implémentés par MAPI doivent avoir une version en lecture seule des méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et prendre en charge la **méthode ValidateState.** Les fournisseurs de transport doivent également prendre **en charge FlushQueues**. Tous les fournisseurs doivent prendre en charge **SettingsDialog**; la prise **en charge de ChangePassword** est facultative. 
  
Les clients utilisent des objets d’état pour effectuer la configuration et pour en savoir plus sur l’état de la session. Ils accèdent à un objet d’état en appelant la méthode **OpenStatusEntry** d’un objet d’ouverture de ouvert de service ou la méthode [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer l’objet d’état. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


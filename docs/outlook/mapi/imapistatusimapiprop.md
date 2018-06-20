---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783965"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**S’applique à**: Outlook 
  
Fournit des informations d’état sur le sous-système MAPI, le carnet d’adresses intégré et le spouleur MAPI. Un fournisseur de services implémente **IMAPIStatus** pour fournir des informations sur son propre état. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets d’état  <br/> |
|Implémentée par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIStatus  <br/> |
|Type de pointeur :  <br/> |LPMAPISTATUS  <br/> |
|Modèle de transaction :  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Vérifie les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services.  <br/> |
|[Dialogue](imapistatus-settingsdialog.md) <br/> |Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de service.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifie le mot de passe d’un fournisseur de services sans afficher l’interface utilisateur.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Force tous les messages en attente d’être envoyés ou reçus pour être immédiatement téléchargé ou téléchargé.  <br/> |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Les objets d’état qui implémente MAPI prennent en charge les méthodes suivantes :
  
|**Objet d’état**|**Méthodes prises en charge**|
|:-----|:-----|
|Sous-système MAPI  <br/> |**ValidateState**  <br/> |
|Carnet d’adresses MAPI  <br/> |**ValidateState**  <br/> |
|Spouleur MAPI  <br/> |**ValidateState** et **FlushQueues** <br/> |
   
Les objets d’état qui implémente MAPI sont requis pour une version en lecture seule des méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et pour prendre en charge la méthode **ValidateState** . Fournisseurs de transport doivent également en charge **FlushQueues**. Tous les fournisseurs doivent prendre en charge de **dialogue**; prise en charge **ChangePassword** est facultative. 
  
Clients utilisent les objets d’état pour effectuer la configuration et en savoir plus sur l’état de la session. Ils accéder à un objet d’état en appelant la méthode **OpenStatusEntry** d’un objet de connexion de fournisseur de service ou la méthode [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer l’objet d’état. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


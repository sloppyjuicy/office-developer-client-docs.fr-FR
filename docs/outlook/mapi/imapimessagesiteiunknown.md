---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45905d24b53561a54385a2f3301e62a116da25ec
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770793"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Manipule les messages et est implémenté par le code de la visionneuse de formulaires (généralement une application cliente) qui répond à cette manipulation.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets de site de message  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIMessageSite  <br/> |
|Type de pointeur :  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Renvoie la session MAPI dans laquelle le message actuel a été créé ou ouvert. |
|[GetStore](imapimessagesite-getstore.md) <br/> |Renvoie la boutique de messages qui contient le message actuel, si une telle magasin existe. |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Renvoie le dossier dans lequel le message actuel a été créé ou ouvert, s’il existe un tel dossier. |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Renvoie le message actuel. |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Renvoie une interface de gestionnaire de formulaires, qu’un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires. |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Crée un message. |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copie le message actuel dans un dossier. |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Déplace le message actuel vers un dossier. |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Supprime le message actuel. |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Demande que le message actuel soit enregistré. |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Demande que le message actuel soit mis en file d’attente pour remise. |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Renvoie des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel. |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de site de message. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


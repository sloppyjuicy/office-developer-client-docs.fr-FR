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
ms.openlocfilehash: 7cc27b5d5ce3b0bbfd2dd407248be60a6baa157b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575910"
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
|[GetSession](imapimessagesite-getsession.md) <br/> |Renvoie la session MAPI dans laquelle le message actuel a été créé ou ouvert.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Renvoie la magasine de messages qui contient le message actuel, si tel est le cas.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Renvoie le dossier dans lequel le message actuel a été créé ou ouvert, s’il existe un tel dossier.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Renvoie le message actuel.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Renvoie une interface de gestionnaire de formulaires, qu’un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Crée un message.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copie le message actuel dans un dossier.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Déplace le message actuel vers un dossier.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Supprime le message actuel.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Demande que le message actuel soit enregistré.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Demande que le message actuel soit mis en file d’attente pour remise.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Renvoie des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de site de message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


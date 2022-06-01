---
title: IMAPIMessageSite IUnknown
description: IMAPIMessageSiteIUnknown manipule les messages et est implémenté par le code de la visionneuse de formulaires (généralement une application cliente) qui répond à cette manipulation.
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
ms.openlocfilehash: 4f2b6dbf1ea2c1f12ba8cc18d3ed4e76e79f7e6f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816310"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Manipule les messages et est implémenté par le code de la visionneuse de formulaires (généralement une application cliente) qui répond à une telle manipulation.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets de site de message  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIMessageSite  <br/> |
|Type de pointeur :  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member | Description |
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Retourne la session MAPI dans laquelle le message actuel a été créé ou ouvert. |
|[GetStore](imapimessagesite-getstore.md) <br/> |Retourne le magasin de messages qui contient le message actuel, s’il existe un tel magasin. |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Retourne le dossier dans lequel le message actuel a été créé ou ouvert, s’il existe un tel dossier. |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Retourne le message actuel. |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Retourne une interface du gestionnaire de formulaires, qu’un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires. |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Crée un message. |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copie le message actuel dans un dossier. |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Déplace le message actuel vers un dossier. |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Supprime le message actuel. |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Demande que le message actuel soit enregistré. |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Demande que le message actuel soit mis en file d’attente pour la remise. |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Retourne des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel. |
|[Getlasterror](imapimessagesite-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de site de message. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


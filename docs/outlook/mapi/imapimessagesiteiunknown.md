---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783861"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**S’applique à**: Outlook 
  
Gère les messages et est implémentée par le code de visionneuse de formulaire (généralement, une application cliente) qui répond à ce manipulation.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets du site  <br/> |
|Implémentée par :  <br/> |Visionneuses de formulaire  <br/> |
|Appelée par :  <br/> |Objets de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIMessageSite  <br/> |
|Type de pointeur :  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Renvoie la session MAPI dans lequel le message en cours a été créé ou ouvert.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Renvoie la banque de messages qui contient le message en cours, si une banque de ce type existe.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Renvoie le dossier dans lequel le message en cours a été créé ou ouvert, si un tel dossier existe.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Renvoie le message en cours.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Renvoie une interface du Gestionnaire de formulaire un serveur de formulaire peut utiliser pour ouvrir un autre serveur du formulaire.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Crée un nouveau message.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copie le message en cours dans un dossier.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Déplace le message en cours dans un dossier.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Supprime le message en cours.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Demandes d’enregistrer le message en cours.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Demande que le message en cours est en attente de remise.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Retourne des informations à partir d’un objet de site message sur le message fonctionnalités du site pour le message en cours.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de site de message en cours.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


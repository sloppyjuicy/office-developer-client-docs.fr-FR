---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e450b8ae02ac783b03d92e85bcf4a95af3792170
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788149"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des méthodes pour encapsuler les propriétés MAPI qui ne sont pas pris en charge par un système de messagerie dans des flux binaires qui peuvent être joints à des messages. Le format utilisé pour cette encapsulation est Transport-Neutral format TNEF (Encapsulation Format). Le fournisseur de transport cible ou l’application cliente MAPI peut ensuite, lors de la réception d’un message incluant une pièce jointe TNEF, récupérer les propriétés de la pièce jointe.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Tnef.h  <br/> |
|Exposé par :  <br/> |Objets TNEF  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de transport, fournisseurs de magasins de messages et passerelles  <br/> |
|Identificateur d’interface :  <br/> |IID_ITNEF  <br/> |
|Type de pointeur :  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Permet au fournisseur de services d’appel ou à la passerelle d’ajouter des propriétés à l’encapsulation d’un message ou d’une pièce jointe. |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrait les propriétés d’une encapsulation TNEF. |
|[Finish](itnef-finish.md) <br/> |Termine le traitement de toutes les opérations TNEF en file d’attente. |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Ouvre une interface de flux sur le texte d’un message encapsulé. |
|[SetProps](itnef-setprops.md) <br/> |Définit la valeur d’une ou de plusieurs propriétés d’un message ou d’une pièce jointe encapsulé sans modifier le message ou la pièce jointe d’origine. |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Code une vue de la table des destinataires d’un message dans le flux de données TNEF du message. |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Traite les composants individuels d’un message un par un dans un flux TNEF. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


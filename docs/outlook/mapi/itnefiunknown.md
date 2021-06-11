---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428514"
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
|[AddProps](itnef-addprops.md) <br/> |Permet au fournisseur de services d’appel ou à la passerelle d’ajouter des propriétés à l’encapsulation d’un message ou d’une pièce jointe.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrait les propriétés d’une encapsulation TNEF.  <br/> |
|[Finish](itnef-finish.md) <br/> |Termine le traitement de toutes les opérations TNEF en file d’attente.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Ouvre une interface de flux sur le texte d’un message encapsulé.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Définit la valeur d’une ou de plusieurs propriétés pour un message ou une pièce jointe encapsulé sans modifier le message ou la pièce jointe d’origine.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Code une vue de la table des destinataires d’un message dans le flux de données TNEF du message.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Traite les composants individuels d’un message un par un dans un flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


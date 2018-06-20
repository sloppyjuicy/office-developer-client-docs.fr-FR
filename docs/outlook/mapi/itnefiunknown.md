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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784504"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**S’applique à**: Outlook 
  
Fournit des méthodes pour encapsuler les propriétés MAPI qui ne sont pas pris en charge par un système de messagerie en flux binaires qui peuvent être joints aux messages. Le format utilisé pour cette encapsulation est le Transport-Neutral Encapsulation Format TNEF (). Le fournisseur de transport cible ou d’une application cliente basée sur MAPI permettre ensuite, reçoit un message contenant une pièce jointe TNEF, récupérer les propriétés de la pièce jointe.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF.h  <br/> |
|Exposés par :  <br/> |Objets TNEF  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de transport, les fournisseurs de banque de message et passerelles  <br/> |
|Identificateur de l’interface :  <br/> |IID_ITNEF  <br/> |
|Type de pointeur :  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Permet à l’appelant fournisseur de services ou la passerelle ajouter des propriétés à l’encapsulation d’un message ou d’une pièce jointe.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrait les propriétés d’une encapsulation TNEF.  <br/> |
|[Terminer](itnef-finish.md) <br/> |Fin de traitement de toutes les opérations TNEF sont en file d’attente et en attente.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Ouvre une interface de flux sur le texte d’un message encapsulé.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Définit la valeur d’une ou plusieurs propriétés d’un message encapsulé ou d’une pièce jointe sans modifier le message d’origine ou une pièce jointe.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Encode un affichage pour la table des destinataires d’un message dans le flux de données TNEF pour le message.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Traite des composants individuels à partir d’un message à la fois dans un objet stream TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)


---
title: Propriété canonique PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3ddde5d206eb4be56ce6a7bae77eb00237f12a0f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584295"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Propriété canonique PidTagRecipientType

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le type de destinataire pour un destinataire du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Identificateur :  <br/> |0x0C15  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le type de destinataire contenu dans cette propriété se compose d’une valeur obligatoire et un indicateur facultatif.
  
Cette propriété doit contenir exactement une des valeurs suivantes :
  
MAPI_TO 
  
> Le destinataire est un serveur principal (destinataire à). Les clients doivent gérer les destinataires principaux. Tous les autres types sont facultatifs.
    
NI 
  
> Le destinataire est un destinataire en copie carbone (CC), un destinataire qui reçoit un message en plus des destinataires principaux.
    
MAPI_BCC 
  
> Le destinataire est un destinataire de copie carbone invisible (Cci). Destinataires principal et de copie carbone connaissent l’existence des destinataires Cci. 
    
MAPI_P1 
  
> Le destinataire s’est pas correctement le message lors de la tentative précédente. Il s’agit d’un renvoi d’une transmission antérieure.
    
En outre, l’indicateur suivant peut être définie :
  
MAPI_SUBMITTED 
  
> Le destinataire a déjà reçu le message et ne doit pas recevoir de nouveau. Il s’agit d’un renvoi d’une transmission antérieure. Cet indicateur est défini en association avec les valeurs **MAPI_TO**, **ni**et **MAPI_BCC** . 
    
La valeur MAPI_P1 et l’indicateur **MAPI_SUBMITTED** est utilisés lors de la retransmission d’un message en raison de non-remise à une ou plusieurs des destinataires. Pour cette retransmission, le client définit **MAPI_SUBMITTED** sur chaque destinataire n'a pas besoin du message, mais doit être affiché dans la liste des destinataires. Pour chaque destinataire n’ayant pas reçu le message précédemment, le client conserve le destinataire d’origine dont la valeur est inchangée **PR_RECIPIENT_TYPE** , mais en outre envoie une copie du destinataire avec MAPI_P1 à la place de la valeur d’origine. Cette copie, qui est ignorée avant remise réelle, force le destinataire dans l’enveloppe P1 et garantit retransmission physique à ce destinataire. La propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) est définie sur FALSE pour MAPI_P1 destinataires.
  
Lorsqu’un client affiche un formulaire de renvoi, seuls les destinataires MAPI_P1 sont visibles. À moins que l’utilisateur entre des destinataires supplémentaires, lorsque le message est remis, la liste des destinataires s’affiche exactement comme lorsque le message a été envoyé pour la première fois. 
  
Le **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) sont liées à un type de destinataire. Lorsqu’un client appelle **IMAPIProp::SaveChanges d’un message** et il existe au moins un destinataire dans la liste des destinataires, le fournisseur de banque de messages définit ces propriétés comme suit : 
  
|**Propriété**|**Description**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |La valeur TRUE si un ou plusieurs destinataires sont **MAPI_TO** destinataires.  <br/> |
|PR_DISPLAY_CC  <br/> |La valeur TRUE si un ou plusieurs destinataires sont **ni** destinataires.  <br/> |
| PR_DISPLAY_BCC  <br/> |La valeur TRUE si un ou plusieurs destinataires sont **MAPI_BCC** destinataires.  <br/> |
   
L’enveloppe P1 ou de remise est X.400, les informations nécessaires pour envoyer un message, y compris les propriétés de l’adresse du destinataire et les indicateurs d’option de contrôle de remise et réponses. L’enveloppe P2 ou affichage est les informations généralement affichées pour chaque destinataire autre que le texte du message. Il inclut généralement l’objet, importance, priorité, sensibilité et heure d’envoi, comme ainsi que les noms des destinataires principaux et copiés. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Propriété canonique PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Propriété canonique PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Propriété canonique PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


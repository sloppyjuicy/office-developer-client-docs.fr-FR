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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355257"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Propriété canonique PidTagRecipientType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le type de destinataire d’un destinataire de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Identificateur :  <br/> |0x0C15  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le type de destinataire contenu dans cette propriété se compose d’une valeur requise et d’un indicateur facultatif.
  
Cette propriété doit contenir exactement l’une des valeurs suivantes :
  
MAPI_TO 
  
> Le destinataire est un destinataire principal (À). Les clients sont tenus de gérer les destinataires principaux. Tous les autres types sont facultatifs.
    
MAPI_CC 
  
> Le destinataire est un destinataire en copie carbone (CC), un destinataire qui reçoit un message en plus des destinataires principaux.
    
MAPI_BCC 
  
> Le destinataire est un destinataire en copie carbone non voyante (Bc). Les destinataires de copie principale et carbone ignorent l’existence de destinataires BcC. 
    
MAPI_P1 
  
> Le destinataire n’a pas reçu le message lors de la tentative précédente. Il s’agit d’un renvoyer d’une transmission antérieure.
    
En outre, l’indicateur suivant peut être définie :
  
MAPI_SUBMITTED 
  
> Le destinataire a déjà reçu le message et n’a pas besoin de le recevoir à nouveau. Il s’agit d’un renvoyer d’une transmission antérieure. Cet indicateur est associé aux valeurs **MAPI_TO,** **MAPI_CC** et **MAPI_BCC** valeurs. 
    
La MAPI_P1 et l’indicateur **MAPI_SUBMITTED** sont utilisés lorsqu’un message est retransmis en raison d’une non-remise à un ou plusieurs des destinataires prévus. Pour cette retransmission, le client définit **MAPI_SUBMITTED** sur chaque destinataire qui n’a pas besoin de nouveau du message, mais qui doit être affiché dans la liste des destinataires. Pour chaque destinataire qui **n’a** pas reçu le message précédemment, le client conserve le destinataire d’origine avec sa valeur PR_RECIPIENT_TYPE inchangée, mais envoie en outre une copie du destinataire avec MAPI_P1 à la place de la valeur d’origine. Cette copie, qui est ignorée avant la remise réelle, force le destinataire dans l’enveloppe P1 et garantit la retransmission physique à ce destinataire. La **propriété PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) est définie sur FALSE pour MAPI_P1 destinataires.
  
Lorsqu’un client affiche un formulaire de renvoyer, seuls les destinataires MAPI_P1 sont visibles. Sauf si l’utilisateur entre des destinataires supplémentaires, lorsque le message est remis, la liste des destinataires s’affiche exactement comme lors de la première envoi du message. 
  
Les **propriétés PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) sont liées au type de destinataire. Lorsqu’un client appelle **IMAPIProp::SaveChanges** d’un message et qu’il y a au moins un destinataire dans la liste des destinataires, le fournisseur de magasin de messages définit ces propriétés comme suit : 
  
|**Propriété**|**Description**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Définissez cette valeur sur TRUE si un ou plusieurs destinataires sont **MAPI_TO** destinataires.  <br/> |
|PR_DISPLAY_CC  <br/> |Définissez cette valeur sur TRUE si un ou plusieurs destinataires sont **MAPI_CC** destinataires.  <br/> |
| PR_DISPLAY_BCC  <br/> |Définissez cette valeur sur TRUE si un ou plusieurs destinataires sont **MAPI_BCC** destinataires.  <br/> |
   
Dans X.400, l’enveloppe P1 ou de remise est les informations nécessaires pour remettre un message, y compris les propriétés d’adresse du destinataire et les indicateurs d’option contrôlant la remise et les réponses. L’enveloppe P2 ou d’affichage est les informations généralement affichées pour chaque destinataire autre que le texte du message lui-même. Il inclut généralement l’objet, l’importance, la priorité, la sensibilité et l’heure d’envoi, ainsi que les noms des destinataires principaux et copiés. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Propriété canonique PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Propriété canonique PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Propriété canonique PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


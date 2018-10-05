---
title: Propriété canonique PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388258"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Propriété canonique PidTagDisplayBcc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste ASCII des noms complets des destinataires message en copie carbone invisible (Cci), séparés par des points-virgules ( ;).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Identificateur :  <br/> |0x0E02  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

La banque de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . La banque de messages gère également ces propriétés pour qu’elle reflète toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Si un message n’a pas de destinataires en copie carbone invisible, la banque de messages doit répondre à un appel de [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour **PR_DISPLAY_BCC**. 
  
En raison de la nécessité de possible pour la localisation, MAPI fournit ces instructions pour tous les noms des destinataires :
  
- Les noms doivent être en mesure d’être localisés. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et propriétés **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Des points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontrée dans cette propriété à un caractère de séparation localisés avant de rendre les informations de la propriété visible dans l’interface utilisateur. 
    
- Lors du transfert des messages, les clients est inutile de traduire les caractères de séparation de la ligne de destinataires en copie carbone invisible. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Décrit le format des messages utilisé pour envoyer des informations relatives au partage de dossiers sur le client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


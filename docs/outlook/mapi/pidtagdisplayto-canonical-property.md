---
title: Propriété canonique PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 79a0307aaf8b91a50485234acc2e1cbdd2314b47
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574166"
---
# <a name="pidtagdisplayto-canonical-property"></a>Propriété canonique PidTagDisplayTo

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une liste des noms complets du principal (à) destinataires du message, séparés par des points-virgules ( ;). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Identificateur :  <br/> |0x0E04  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

La banque de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . La banque de messages gère également ces propriétés pour qu’elle reflète toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Si un message n’a pas de destinataire principales, la banque de messages doit répondre à un appel de [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour **PR_DISPLAY_TO**. 
  
En raison de la nécessité de possible pour la localisation, MAPI fournit ces instructions pour tous les noms des destinataires :
  
- Les noms doivent être en mesure d’être localisés. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_TO** , **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)). Des points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré **PR_DISPLAY_TO** les propriétés associées à un caractère de séparation localisés avant de rendre les informations visibles dans l’interface utilisateur. 
    
- Lors du transfert des messages, les clients est inutile de traduire les caractères de séparation de la ligne de destinataire principale. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
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


---
title: Propriété canonique PidTagDisplayCc
description: Décrit la propriété canonique PidTagDisplayCc, qui contient une liste ASCII des noms d’affichage des destinataires de messages de copie carbone (CC).
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
ms.openlocfilehash: f7ac5a9fc214961b62d16cd7fc7a35ab4e7a654d
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771159"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Propriété canonique PidTagDisplayCc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste ASCII des noms complets des destinataires de messages de copie carbone (CC), séparés par des points-virgules (;). 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Identificateur :  <br/> |0x0E03  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

Le magasin de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . Le magasin de messages conserve également ces propriétés afin qu’elles reflètent toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à [IMAPIProp::SaveChanges](imapiprop-savechanges.md). 
  
Si un message n’a pas de destinataires de copie carbone, le magasin de messages doit répondre à un appel [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour ces propriétés. 
  
En raison du besoin possible de localisation, MAPI fournit ces instructions pour tous les noms de destinataires :
  
- Tous les noms doivent pouvoir être localisés. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** et **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré dans cette propriété en un caractère de séparateur localisé avant de rendre les informations de propriété visibles dans l’interface utilisateur. 
    
- Lors du transfert de messages, les clients n’ont pas besoin de traduire les caractères de séparateur sur la ligne de destinataire de copie carbone. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de courrier électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


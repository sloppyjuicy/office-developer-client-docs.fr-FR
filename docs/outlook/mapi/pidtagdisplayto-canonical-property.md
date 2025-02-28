---
title: PidTagDisplayTo Canonical, propriété
description: Décrit la propriété canonique PidTagDisplayTo, qui contient une liste des noms d’affichage des destinataires du message principal (À).
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
ms.openlocfilehash: e5cf15ee22db9da453479c139eef449981165fa3
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771243"
---
# <a name="pidtagdisplayto-canonical-property"></a>PidTagDisplayTo Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste des noms d’affichage des destinataires de message principaux (À), séparés par des points-virgules (;). 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Identificateur :  <br/> |0x0E04  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

Le magasin de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . Le magasin de messages conserve également ces propriétés afin qu’elles reflètent toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Si un message n’a aucun destinataire principal, le magasin de messages doit répondre à un appel [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour **PR_DISPLAY_TO**. 
  
En raison du besoin possible de localisation, MAPI fournit ces instructions pour tous les noms de destinataires :
  
- Tous les noms doivent pouvoir être localisés. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les **propriétés PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_TO** . Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré dans le **PR_DISPLAY_TO** et les propriétés associées en un caractère de séparateur localisé avant de rendre les informations visibles dans l’interface utilisateur. 
    
- Lors du transfert de messages, les clients n’ont pas besoin de traduire les caractères de séparateur sur la ligne du destinataire principal. 
    
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


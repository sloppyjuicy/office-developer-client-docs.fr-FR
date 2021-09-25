---
title: Propriété canonique PidTagDisplayCc
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3dcdcdcbcc8b6d8ece3cfc0bff31253bfe6f1f20
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600175"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Propriété canonique PidTagDisplayCc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste ASCII des noms d’affichage des destinataires des messages en copie carbone (CC), séparés par des points-virgules (;). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Identificateur :  <br/> |0x0E03  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

La magasin de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) La magasin de messages conserve également ces propriétés afin qu’elle reflète toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à [IMAPIProp::SaveChanges](imapiprop-savechanges.md). 
  
Si un message ne possède aucun destinataire en copie carbone, la boutique de messages doit répondre à un appel [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour ces propriétés. 
  
En raison de la nécessité possible de la localisation, MAPI fournit les instructions suivantes pour tous les noms de destinataires :
  
- Tous les noms doivent pouvoir être localisées. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** et **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré dans cette propriété en caractère séparateur traduit avant de rendre les informations de propriété visibles dans l’interface utilisateur. 
    
- Lors du forwarding de messages, les clients n’ont pas besoin de traduire les caractères de séparation sur la ligne de destinataire en copie carbone. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


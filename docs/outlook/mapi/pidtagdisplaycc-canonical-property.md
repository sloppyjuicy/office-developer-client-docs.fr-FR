---
title: Propriété canonique PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360808"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Propriété canonique PidTagDisplayCc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste ASCII des noms d'affichage des destinataires de messages CC (copie carbone), séparés par des points-virgules (;). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Identificateur :  <br/> |0x0E03  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

La Banque de messages calcule ces propriétés sur les objets de message à l'aide de la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . La Banque de messages gère également ces propriétés de sorte qu'elle reflète toujours le dernier état enregistré d'un message. La valeur est synchronisée au moment de chaque appel à [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). 
  
Si un message n'a pas de destinataires en copie carbone, la Banque de messages doit répondre à un appel [IMAPIProp:: GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour ces propriétés. 
  
En raison de l'éventuel besoin de localisation, MAPI fournit les instructions suivantes pour tous les noms de destinataires:
  
- Tous les noms doivent pouvoir être localisés. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**et **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré dans cette propriété en un caractère de séparation localisé avant de rendre les informations de propriété visibles dans l'interface utilisateur. 
    
- Lors du transfert de messages, les clients n'ont pas besoin de traduire les caractères de séparation sur la ligne du destinataire de la copie carbone. 
    
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


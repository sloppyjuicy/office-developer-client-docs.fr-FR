---
title: Propriété canonique PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d1ae9f1a45e315f2e16a2d6d501534cd1bdae01e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566709"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Propriété canonique PidTagDisplayBcc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste ASCII des noms d’affichage des destinataires de message en copie carbone non voyante (Bc), séparés par des points-virgules (;).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Identificateur :  <br/> |0x0E02  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

La magasin de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) La magasin de messages conserve également ces propriétés afin qu’elle reflète toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à la méthode [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Si un message ne possède aucun destinataire en copie carbone non voyante, la boutique de messages doit répondre à un appel [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour **PR_DISPLAY_BCC**. 
  
En raison de la nécessité possible de la localisation, MAPI fournit les instructions suivantes pour tous les noms de destinataires :
  
- Tous les noms doivent pouvoir être localisées. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms des propriétés **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré dans cette propriété en caractère séparateur traduit avant de rendre les informations de propriété visibles dans l’interface utilisateur. 
    
- Lors du forwarding de messages, les clients n’ont pas besoin de traduire les caractères de séparation sur la ligne de destinataire en copie carbone non voyante. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Décrit le format des messages utilisés pour envoyer des informations relatives au partage de dossiers sur le client.
    
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


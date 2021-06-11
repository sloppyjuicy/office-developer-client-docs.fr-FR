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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360787"
---
# <a name="pidtagdisplayto-canonical-property"></a>Propriété canonique PidTagDisplayTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste des noms d’affichage des destinataires du message principal (À), séparés par des points-virgules (;). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Identificateur :  <br/> |0x0E04  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Remarques

La magasin de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) La magasin de messages conserve également ces propriétés afin qu’elle reflète toujours le dernier état enregistré d’un message. La valeur est synchronisée au moment de chaque appel à la méthode [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Si un message n’a pas de destinataire principal, la boutique de messages doit répondre à un appel [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour **PR_DISPLAY_TO**. 
  
En raison de la nécessité possible de la localisation, MAPI fournit les instructions suivantes pour tous les noms de destinataires :
  
- Tous les noms doivent pouvoir être localisées. 
    
- Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_TO.** Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI. 
    
- Les clients doivent traduire chaque point-virgule rencontré dans le **PR_DISPLAY_TO** et les propriétés associées en caractère séparateur traduit avant de rendre les informations visibles dans l’interface utilisateur. 
    
- Lors du forwarding de messages, les clients n’ont pas besoin de traduire les caractères de séparation sur la ligne du destinataire principal. 
    
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


---
title: Propriété canonique PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 555906386b60c106fbed6d123155574ca3106b23
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455607"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propriété canonique PidTagDisplayType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur utilisée pour associer une icône à une ligne particulière d’un tableau. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificateur :  <br/> |0x3900  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un nombre long qui facilite un traitement spécial de l’entrée de table en fonction de son type. Ce traitement spécial consiste généralement à afficher une icône ou un autre élément d’affichage associé au type d’affichage. 
  
Cette propriété n’est pas utilisée dans les tables de contenu de dossier. Les applications clientes doivent utiliser la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d’un message et l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) appropriée pour obtenir les propriétés **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) pour ce message. 
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
DT_AGENT 
  
> Un agent automatisé, tel qu’un guillemet du jour ou un affichage de graphique météo.
    
DT_DISTLIST 
  
> Liste de distribution.
    
DT_FOLDER 
  
> Affiche l’icône de dossier par défaut en adjacent au dossier.
    
DT_FOLDER_LINK 
  
> Affiche l’icône de lien de dossier par défaut adjacente au dossier plutôt que l’icône de dossier par défaut.
    
DT_FOLDER_SPECIAL 
  
> Icône d’affichage d’un dossier avec une distinction spécifique à l’application, telle qu’un type spécial de dossier public.
    
DT_FORUM 
  
> Forum, tel qu’un service de forum ou un dossier public ou partagé.
    
DT_GLOBAL 
  
> Un carnet d’adresses global.
    
DT_LOCAL 
  
> Carnet d’adresses local que vous partagez avec un petit groupe de travail.
    
DT_MAILUSER 
  
> Un utilisateur de messagerie classique.
    
DT_MODIFIABLE 
  
> Modifiable ; le conteneur doit être noté comme modifiable dans l’interface utilisateur.
    
DT_NOT_SPECIFIC 
  
> Ne correspond à aucun des autres paramètres.
    
DT_ORGANIZATION 
  
> Alias spécial défini pour un grand groupe, tel que le service d’aide, la comptabilité ou le coordinateur de lecteur de sang.
    
DT_PRIVATE_DISTLIST 
  
> Liste de distribution privée, gérée par des personnes.
    
DT_REMOTE_MAILUSER 
  
> Destinataire connu d’un système de messagerie étranger ou distant.
    
DT_WAN 
  
> Un carnet d’adresses réseau large.
    
Les tables de contenu de carnet d’adresses utilisent les valeurs DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST et DT_REMOTE_MAILUSER de carnet d’adresses. Les tables de hiérarchie de carnet d’adresses et les tables DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC et DT_WAN de carnet d’adresses. Les tables de hiérarchie de dossiers utilisent DT_FOLDER, DT_FOLDER_LINK et DT_FOLDER_SPECIAL valeurs. 
  
Si cette propriété n’est pas définie, le client doit supposer le type par défaut approprié pour la table, généralement DT_FOLDER, DT_LOCAL ou DT_MAILUSER. 
  
 **Remarque** Toutes les valeurs non documentées sont réservées à MAPI. Les applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêtes à traiter une valeur nondocumentée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les modèles de carnet d’adresses.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Active l’accès à l’annuaire.
    
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


---
title: Propriété canonique PidTagDisplayType
description: Décrit la propriété canonique PidTagDisplayType, qui contient une valeur utilisée pour associer une icône à une ligne particulière d’une table.
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
ms.openlocfilehash: b34908a2b3b62132442fc107a8f674b0cbdb5bad
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769724"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propriété canonique PidTagDisplayType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur utilisée pour associer une icône à une ligne particulière d’une table. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificateur :  <br/> |0x3900  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un entier long qui facilite le traitement spécial de l’entrée de table en fonction de son type. Ce traitement spécial consiste généralement à afficher une icône ou un autre élément d’affichage associé au type d’affichage. 
  
Cette propriété n’est pas utilisée dans les tables de contenu de dossier. Les applications clientes doivent utiliser la propriété **PR_MESSAGE_CLASS** d’un message ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) et l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) appropriée pour obtenir les propriétés **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) pour ce message. 
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
DT_AGENT 
  
> Agent automatisé, tel que Quote-Of-The-The-Day ou affichage d’un graphique météo.
    
DT_DISTLIST 
  
> Liste de distribution.
    
DT_FOLDER 
  
> Afficher l’icône de dossier par défaut adjacente au dossier.
    
DT_FOLDER_LINK 
  
> Affichez l’icône de lien de dossier par défaut adjacente au dossier plutôt que l’icône de dossier par défaut.
    
DT_FOLDER_SPECIAL 
  
> Icône d’affichage d’un dossier avec une distinction spécifique à l’application, telle qu’un type spécial de dossier public.
    
DT_FORUM 
  
> Un forum, tel qu’un service de tableau d’affichage ou un dossier public ou partagé.
    
DT_GLOBAL 
  
> Carnet d’adresses global.
    
DT_LOCAL 
  
> Carnet d’adresses local que vous partagez avec un petit groupe de travail.
    
DT_MAILUSER 
  
> Utilisateur de messagerie classique.
    
DT_MODIFIABLE 
  
> Modifiable; le conteneur doit être indiqué comme modifiable dans l’interface utilisateur.
    
DT_NOT_SPECIFIC 
  
> Ne correspond à aucun des autres paramètres.
    
DT_ORGANIZATION 
  
> Alias spécial défini pour un grand groupe, tel que le support technique, la comptabilité ou le coordinateur de la prise de sang.
    
DT_PRIVATE_DISTLIST 
  
> Liste de distribution privée, administrée personnellement.
    
DT_REMOTE_MAILUSER 
  
> Destinataire connu pour être issu d’un système de messagerie étranger ou distant.
    
DT_WAN 
  
> Carnet d’adresses réseau étendu.
    
Les tables de contenu du carnet d’adresses utilisent les valeurs DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST et DT_REMOTE_MAILUSER. Les tables de hiérarchie de carnet d’adresses et les tables uniques utilisent les valeurs DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC et DT_WAN. Les tables de hiérarchie de dossiers utilisent les valeurs DT_FOLDER, DT_FOLDER_LINK et DT_FOLDER_SPECIAL. 
  
Si cette propriété n’est pas définie, le client doit supposer le type par défaut approprié pour la table, généralement DT_FOLDER, DT_LOCAL ou DT_MAILUSER. 
  
 **Note** Toutes les valeurs non documentées sont réservées à MAPI. Les applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêtes à traiter une valeur non documentée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les modèles de carnet d’adresses.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Active l’accès au répertoire.
    
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


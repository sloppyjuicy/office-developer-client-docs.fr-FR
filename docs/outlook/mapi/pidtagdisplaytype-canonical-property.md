---
title: Propriété canonique PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360780"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propriété canonique PidTagDisplayType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur utilisée pour associer une icône à une ligne particulière d'un tableau. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificateur :  <br/> |0x3900  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d'adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un entier long qui facilite le traitement spécial de l'entrée de table en fonction de son type. Ce traitement spécial consiste généralement à afficher une icône ou un autre élément d'affichage, associé au type d'affichage. 
  
Cette propriété n'est pas utilisée dans les tableaux de contenu de dossier. Les applications clientes doivent utiliser la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d'un message et l'interface [IMAPIFormInfo](imapiforminfoimapiprop.md) appropriée pour obtenir les **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et **PR_MINI_ICON** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) pour ce message. 
  
Cette propriété peut avoir exactement l'une des valeurs suivantes:
  
DT_AGENT 
  
> Un agent automatisé, tel que «quote-of-the-Day» ou un graphique météo.
    
DT_DISTLIST 
  
> Une liste de distribution.
    
DT_FOLDER 
  
> Affiche l'icône de dossier par défaut en regard du dossier.
    
DT_FOLDER_LINK 
  
> Affichage de l'icône de lien de dossier par défaut en regard du dossier et non de l'icône de dossier par défaut.
    
DT_FOLDER_SPECIAL 
  
> Icône d'affichage pour un dossier avec une distinction propre à l'application, telle qu'un type spécial de dossier public.
    
DT_FORUM 
  
> Un forum, tel qu'un service BBS ou un dossier public ou Shared.
    
DT_GLOBAL 
  
> Un carnet d'adresses global.
    
DT_LOCAL 
  
> Carnet d'adresses local que vous partagez avec un petit groupe de travail.
    
DT_MAILUSER 
  
> Un utilisateur de messagerie classique.
    
DT_MODIFIABLE 
  
> Modifiable; le conteneur doit être désigné comme modifiable dans l'interface utilisateur.
    
DT_NOT_SPECIFIC 
  
> Ne correspond à aucun autre paramètre.
    
DT_ORGANIZATION 
  
> Alias spécial défini pour un grand groupe, tel que le service d'assistance, la comptabilité ou le coordinateur du disque sanguin.
    
DT_PRIVATE_DISTLIST 
  
> Liste de distribution privée personnelle et administrée personnellement.
    
DT_REMOTE_MAILUSER 
  
> Destinataire connu comme provenant d'un système de messagerie étranger ou distant.
    
DT_WAN 
  
> Un carnet d'adresses de réseau étendu.
    
Les tables des matières du carnet d'adresses utilisent les valeurs DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST et DT_REMOTE_MAILUSER. Les tables de hiérarchie des carnets d'adresses et les tables ponctuelles utilisent les valeurs DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC et DT_WAN. Les tables de hiérarchie des dossiers utilisent les valeurs DT_FOLDER, DT_FOLDER_LINK et DT_FOLDER_SPECIAL. 
  
Si cette propriété n'est pas définie, le client doit supposer le type par défaut approprié pour la table, généralement DT_FOLDER, DT_LOCAL ou DT_MAILUSER. 
  
 **Note** Toutes les valeurs qui ne sont pas documentées sont réservées à MAPI. Les applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêtes à traiter une valeur non documentée. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les modèles de carnet d'adresses.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Active l'accès à l'annuaire.
    
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


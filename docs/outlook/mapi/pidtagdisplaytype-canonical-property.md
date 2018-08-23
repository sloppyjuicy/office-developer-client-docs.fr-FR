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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5b067b3bc38df978cd0f4c52beb37579619edc24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583511"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propriété canonique PidTagDisplayType

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une valeur utilisée pour associer une icône à une ligne particulière d’une table. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificateur :  <br/> |0x3900  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un entier long qui facilite le traitement spécial de l’entrée de table en fonction de son type. Ce traitement spécial se compose généralement de l’affichage d’une icône, ou un autre élément d’affichage, associé avec le type d’affichage. 
  
Cette propriété n’est pas utilisée dans les tableaux contenu de dossier. Applications clientes doivent utiliser d’un message propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) et interface [IMAPIFormInfo](imapiforminfoimapiprop.md) appropriée pour obtenir le **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et **PR_MINI_ICON** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) Propriétés pour ce message. 
  
Cette propriété peut avoir exactement une des valeurs suivantes :
  
DT_AGENT 
  
> Un agent automatisé, tel que devis du jour ou un affichage graphique de météo.
    
DT_DISTLIST 
  
> Une liste de distribution.
    
DT_FOLDER 
  
> Affiche l’icône de dossier par défaut adjacent au dossier.
    
DT_FOLDER_LINK 
  
> Afficher l’icône de lien du dossier par défaut adjacent au dossier plutôt que l’icône de dossier par défaut.
    
DT_FOLDER_SPECIAL 
  
> Affiche l’icône d’un dossier avec une distinction spécifiques à l’application, par exemple un type particulier de dossier public.
    
DT_FORUM 
  
> Forum, par exemple un service forum ou un dossier public ou partagé.
    
DT_GLOBAL 
  
> Un carnet d’adresses global.
    
DT_LOCAL 
  
> Carnet d’adresses local que vous partagez avec un petit groupe de travail.
    
DT_MAILUSER 
  
> Un utilisateur de messagerie par défaut.
    
DT_MODIFIABLE 
  
> Modifiable ; le conteneur doit être marquée comme étant modifiable dans l’interface utilisateur.
    
DT_NOT_SPECIFIC 
  
> Ne correspond pas les autres paramètres.
    
DT_ORGANIZATION 
  
> Un alias spéciaux défini pour un grand groupe, comme le support technique, comptabilité ou coordinateur blood-lecteur.
    
DT_PRIVATE_DISTLIST 
  
> Privé, administrés personnellement la liste de distribution.
    
DT_REMOTE_MAILUSER 
  
> Un destinataire connu à partir d’un système de messagerie étranger ou à distance.
    
DT_WAN 
  
> Un carnet d’adresses réseau étendu.
    
Tables de contenu téléchargeable adresse utilisent les valeurs DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST et DT_REMOTE_MAILUSER. Tables de hiérarchie adresse livre et uniques utilisent les valeurs DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC et DT_WAN. Tables de hiérarchie de dossier utilisent les valeurs DT_FOLDER, DT_FOLDER_LINK et DT_FOLDER_SPECIAL. 
  
Si cette propriété n’est pas définie, le client doit utiliser le type par défaut approprié pour la table, généralement DT_FOLDER, DT_LOCAL ou DT_MAILUSER. 
  
 **Remarque** Toutes les valeurs non documentées sont réservés pour MAPI. Applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêts à traiter avec une valeur non documentée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les modèles de carnet d’adresses.
    
[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Permet l’accès à l’annuaire.
    
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


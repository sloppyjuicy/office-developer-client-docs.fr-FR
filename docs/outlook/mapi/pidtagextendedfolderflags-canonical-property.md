---
title: Propriété canonique PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382658"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Propriété canonique PidTagExtendedFolderFlags
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des indicateurs étendues sur un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Identificateur :  <br/> |0x36DA  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est un flux binaire qui contient des propriétés de sous-sites codées pour le dossier. Il est mis en forme comme une série d’articles sub de longueur variable. Les premiers 8 bits de l’élément sub est un champ ID, qui indique le type d’indicateur de l’élément sub représente. Les deuxième 8 bits est le nombre d’octets de données qui suivent.
  
Valeurs d’ID possibles sont les suivantes :
  
- Non valide
    
   N’utilisez pas cette valeur.
    
- ExtendedFlags
    
   Les données sont une valeur de quatre octets au format :
    
   |**Bits**|**Description**|
   |:-----|:-----|
   |0-1  <br/> |Réservé.  <br/> |
   |2  <br/> |La valeur 0 si l’application doit afficher une description de la stratégie.  <br/> |
   |3-5  <br/> |Réservé.  <br/> |
   |6 et 7  <br/> |Contrôle l’affichage du nombre de messages dans le dossier.  <br/> 0 - utilisez le paramètre par défaut  <br/> 1 - utiliser le nombre de messages non lus  <br/> 3 - Utilisez le nombre total de messages  <br/> |
   |8-31  <br/> |Réservé.  <br/> |
   
Articles réservés peuvent être ignorés, mais les valeurs existantes doivent être conservés.
    
- SearchFolderID
    
   Le champ de données est un champ de 16 octets. Lorsque l’application crée un dossier de recherche persistant, elle doit définir ce champ sur le dossier à la même valeur que la **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) une propriété binaire sur le Message de dossier de recherche.
    
- ToDoFolderVersion
    
   Le champ de données est un champ de 4 octets. Lorsque l’application crée le dossier de recherche des tâches, il doit définir la valeur de ce champ dans le dossier à la valeur d’entier primauté de « 0x000c0000 » :
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi

- [Propriétés MAPI](mapi-properties.md)
- [Propriétés canoniques MAPI](mapi-canonical-properties.md)
- [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


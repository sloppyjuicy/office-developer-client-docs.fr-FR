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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316351"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Propriété canonique PidTagExtendedFolderFlags
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des indicateurs étendus sur un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Identificateur :  <br/> |0x36DA  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est un flux binaire qui contient des sous-propriétés codées pour le dossier. Il est formaté comme une série de sous-éléments de longueur variable. Les 8 premiers bits du sous-élément sont un champ ID, qui indique le type d’indicateur que représente le sous-élément. Les 8 deuxièmes bits sont le nombre d’octets de données qui suivent.
  
Les valeurs d’ID possibles sont les suivantes :
  
- Invalid
    
   N’utilisez pas cette valeur
    
- ExtendedFlags
    
   Les données sont une valeur de quatre byte formatées comme :
    
   |**Bits**|**Description**|
   |:-----|:-----|
   |0-1  <br/> |Réservé.  <br/> |
   |2   <br/> |Définir sur 0 si l’application doit afficher une description de stratégie.  <br/> |
   |3-5  <br/> |Réservé.  <br/> |
   |6-7  <br/> |Contrôle l’affichage du nombre de messages dans le dossier.  <br/> 0 : utiliser le paramètre par défaut  <br/> 1 : utiliser le nombre de messages non lus  <br/> 3 : utiliser le nombre total de messages  <br/> |
   |8-31  <br/> |Réservé.  <br/> |
   
Les éléments réservés peuvent être ignorés, mais les valeurs existantes doivent être conservées.
    
- SearchFolderID
    
   Le champ de données est un champ de 16 byte. Lorsque l’application crée un dossier de recherche persistant, elle doit définir ce champ sur le dossier sur la même valeur que la propriété binaire PR_WB_SF_TAG ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)sur le message de dossier de **recherche.**
    
- ToDoFolderVersion
    
   Le champ de données est un champ de 4 byte. Lorsque l’application crée le dossier de recherche à faire, elle doit définir la valeur de ce champ sur le dossier sur la valeur d’un petit nombre de finian « 0x000c0000 » :
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration du client et du serveur, telles que les listes de catégories partagées et les heures de travail.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de manipulation d’une configuration de liste de dossiers de recherche.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi

- [Propriétés MAPI](mapi-properties.md)
- [Propriétés canoniques MAPI](mapi-canonical-properties.md)
- [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


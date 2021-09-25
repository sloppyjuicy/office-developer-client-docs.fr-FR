---
title: Propriété canonique PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f2b06d1e4144335a483a08feedd75210f40f3823
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591352"
---
# <a name="pidtaguserfields-canonical-property"></a>Propriété canonique PidTagUserFields

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom, le type de données et d’autres informations sur un champ défini par l’utilisateur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_USERFIELDS  <br/> |
|Identificateur :  <br/> |0x36E3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Dossier MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant. La **propriété PidLidPropertyDefinitionStream** contient un flux binaire appelé [PropertyDefinition](propertydefinition-stream-structure.md), qui contient les définitions de champ. Pour plus d’informations sur les structures de flux pour les définitions de champ, voir [Stream Structures](stream-structures.md).
  
Pour chaque dossier, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans ce dossier dans la propriété **PidTagUserFields** d’un message associé de la classe de message IPC.MS. REN. USERFIELDS : chaque dossier supposé ne contenir qu’un seul message de cette classe dans la table des matières associée. 
  
> [!NOTE]
> L’ensemble des champs définis par l’utilisateur dans un dossier peut ne pas nécessairement correspondre aux ensembles de champs définis par l’utilisateur dans chacun de ses éléments. 
  
L’ensemble des champs définis par l’utilisateur dans un dossier est affiché à différents endroits dans l’interface utilisateur Outlook, tels que le s’il s’agit du s’il s’agit du dossier. La propriété **PidTagUserFields du** message contient un flux binaire, **FolderUserFields**, qui contient les définitions de champ de dossier. Pour plus d’informations sur les structures de flux pour les définitions de champ de dossier, voir [Structures](folder-fields-stream-structures.md) de flux de champs de dossier et exemple de flux [FolderUserFields.](folderuserfields-stream-sample.md)
  
## <a name="section-heading"></a>Titre de section

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Outlook Éléments et champs](outlook-items-and-fields.md)
  
[Ajouter une définition pour un nouveau champ User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


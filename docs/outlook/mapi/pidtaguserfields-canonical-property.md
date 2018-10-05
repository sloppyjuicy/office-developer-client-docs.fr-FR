---
title: Propriété canonique PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397428"
---
# <a name="pidtaguserfields-canonical-property"></a>Propriété canonique PidTagUserFields

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom du type de données et autres informations sur un champ défini par l’utilisateur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_USERFIELDS  <br/> |
|Identificateur :  <br/> |0x36E3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Dossier MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant. La propriété **PidLidPropertyDefinitionStream** contient un flux binaire appelé [la définition PropertyDefinition](propertydefinition-stream-structure.md), qui contient les définitions de champ. Pour plus d’informations sur les structures de flux de données pour les définitions de champ, voir [Les Structures de flux de données](stream-structures.md).
  
Pour chaque dossier, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans ce dossier dans la propriété **PidTagUserFields** d’un message de la classe de message Outlook.AGINGPROPERTIES associé. REN. CHAMPS - chaque dossier censé contenir pas plus d’un message de cette classe dans sa table des matières associée. 
  
> [!NOTE]
> L’ensemble des champs définis par l’utilisateur dans un dossier correspondent ne peut-être pas nécessairement les jeux de champs définis par l’utilisateur dans chacun de ses éléments. 
  
Le jeu de champs définis par l’utilisateur dans un dossier est affiché à divers emplacements dans l’interface utilisateur Outlook, telles que sélecteur de champs du dossier. La propriété **PidTagUserFields** du message contient un flux binaire, **FolderUserFields**, qui contient les définitions de champ dossier. Pour plus d’informations sur les structures de flux de données pour les définitions de champ dossier voir [Dossier champs Stream Structures](folder-fields-stream-structures.md) et l' [Exemple de flux de données FolderUserFields](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Titre de section

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Champs et éléments Outlook](outlook-items-and-fields.md)
  
[Ajout d’une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

